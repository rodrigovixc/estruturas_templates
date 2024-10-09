Layout responsivo em grid

Usando tailwind

Voce pode usar as mesmas screens ou usar do seu jeito e trocando tablet, cellphone para suas chaves no arquivo tailwind.config.js
theme: {
        extend: {
            // Quebras de tela personalizadas
            screens: {
                'cellphone': {'max': '639px'},  // Telas com largura máxima de 639px
                'tablet': {'min': '640px', 'max': '1023px'},  // Telas entre 640px e 1023px
                'laptop': {'min': '1024px', 'max': '1279px'},  // Telas entre 1024px e 1279px
                'desktop': {'min': '1280px'},  // Telas a partir de 1280px
            },
        }
}

# Padrao
Dispositivo default 3 colunas e 2 linhas

Dispositivo celular 1 coluna e 2 linhas

Dispositivo tablet 2 colunas e 2 linhas

#Adapte

Voce pode adaptar as colunas dentro do grid 
Caso queira seguir no layout 3 colunas, adicione apenas o trecho da coluna dentro do layout-grid
Este é o pai -> <div class="grid grid-cols-3 gap-4 tablet:grid-cols-2 cellphone:grid-cols-1">

    Este é o filho -> {{--    Coluna 1 --}}
                        <div class="grid grid-rows-2">

                            {{--    Linha 1 --}}
                            <div class="font-semibold pr-1 text-slate-800 dark:text-navy-100">

                            </div>

                            {{--    Linha 2 --}}
                            <div class="">

                            </div>
                        </div>

Dê um Ctrl C + V no filho dentro do pai que o layout se adapta para os dispositivos. 