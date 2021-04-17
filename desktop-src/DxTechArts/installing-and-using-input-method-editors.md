---
title: Instalación y uso de editores de métodos de entrada
description: En este artículo se ofrece un tutorial sobre cómo instalar y usar el editor de métodos de entrada (IME) estándar de Windows.
ms.assetid: 0dc430ce-bed4-8d02-f45e-4eefb0ad0369
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd6018b3a387a12409f9e46d0392bbd60015af29
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670454"
---
# <a name="installing-and-using-input-method-editors"></a>Instalación y uso de editores de métodos de entrada

En este artículo se ofrece un tutorial sobre cómo instalar y usar el editor de métodos de entrada (IME) estándar de Windows.

-   [Instalar un editor de métodos de entrada](#installing-an-input-method-editor)
-   [IME de Chino Simplificado](#simplified-chinese-ime)
-   [IME de chino tradicional](#traditional-chinese-ime)
-   [Japonés IME](#japanese-ime)
-   [Coreano IME](#korean-ime)
-   [Requisitos](#requirements)

## <a name="installing-an-input-method-editor"></a>Instalar un editor de métodos de entrada

En las secciones siguientes se describe cómo instalar y usar editores de métodos de entrada (IME) para escribir caracteres complejos en cuatro idiomas de Asia oriental distintos. Se describen las características únicas de cada lenguaje.

Para implementar la funcionalidad del editor de métodos de entrada (IME) en una aplicación, vea [usar un editor de métodos de entrada en un juego](/windows/desktop/DxTechArts/using-an-input-method-editor-in-a-game).

Un IME no se instala de forma predeterminada en los sistemas de Microsoft Windows XP. Para realizar la instalación, complete los pasos siguientes.

**Para instalar un IME**

1.  En el panel de control, abra Opciones regionales y de idioma.
2.  En la pestaña idiomas, active la casilla instalar archivos para idiomas de Asia oriental.

    ![pestaña idiomas de opciones regionales y de idioma](images/ime-1.png)

    Aparece el cuadro de diálogo instalar compatibilidad con idiomas adicionales que informa de los requisitos de almacenamiento de los archivos de idioma.

    ![cuadro de diálogo instalar compatibilidad con idiomas adicionales](images/ime-install-lang-dialog.png)

3.  Haga clic en Aceptar para cerrar el cuadro de diálogo.
4.  Haga clic en aceptar en la pestaña idiomas.
5.  Aparece otro cuadro de diálogo que solicita un disco de instalación de Windows XP o una ubicación de recurso compartido de red donde se encuentran los archivos de compatibilidad de idioma. Inserte un disco compacto de Windows XP o busque la ubicación de red adecuada y haga clic en Aceptar. Microsoft Windows instala los archivos necesarios y le pide que reinicie el equipo.
6.  Haga clic en sí para reiniciar el equipo.
7.  Después de reiniciar, vuelva a abrir el panel de control configuración regional y de idioma.
8.  En la pestaña idiomas, haga clic en detalles. Aparece la ventana servicios de texto y idiomas de entrada.

    ![ventana servicios ext e idiomas de entrada](images/ime-2.png)

9.  En la pestaña Configuración, haga clic en Agregar. Aparece la ventana Agregar idioma de entrada.

    ![ventana Agregar idioma de entrada](images/ime-3.png)

10. Seleccione chino (Taiwán) como idioma de entrada y Microsoft New Phonetic IME 2002a para la distribución del teclado/IME.
11. Haga clic en Aceptar. Ahora puede agregar idiomas adicionales y IME de manera similar.
12. Haga clic en agregar de nuevo, seleccione chino (PRC) como idioma de entrada y chino (simplificado)-Microsoft pinyin IME 3,0 para la distribución del teclado/IME y, a continuación, haga clic en Aceptar.
13. Haga clic en agregar de nuevo, seleccione japonés para el idioma de entrada y Microsoft IME estándar 2002 ver. 8,1 para la distribución del teclado/IME, haga clic en Aceptar.
14. Haga clic en agregar de nuevo, seleccione Coreano como idioma de entrada y sistema de entrada Coreano (IME 2002) para la distribución de teclado/IME y, a continuación, haga clic en Aceptar. En la ventana servicios de texto e idiomas de entrada, el cuadro de lista servicios instalados ahora debe contener los cuatro IME recién agregados.

    ![cuadro de lista servicios instalados](images/ime-7.png)

15. Haga clic en Aceptar para cerrar la ventana servicios de texto e idiomas de entrada.
16. Haga clic en Aceptar para cerrar el panel de control configuración regional y de idioma. La barra de tareas de Windows debe contener ahora un indicador de configuración regional con un círculo en rojo. La existencia del indicador significa que se ha instalado más de un idioma de entrada en el sistema.

    ![indicador que indica que se ha instalado más de un idioma de entrada en el sistema](images/ime-8.png)

## <a name="simplified-chinese-ime"></a>IME de Chino Simplificado

En esta sección se describe cómo usar el IME de chino simplificado (PinYin) con el Bloc de notas de Microsoft para escribir algunos caracteres chinos.

1.  Inicie el Bloc de notas (disponible en el botón Inicio y seleccione todos los programas y accesorios). Escriba algunos caracteres en el Bloc de notas. Estos caracteres le ayudarán a visualizar mejor la ventana del IME más adelante.

    ![Captura que muestra los caracteres que ayudan a visualizar mejor la ventana I M E más adelante para el chino simplificado.](images/ime-sc1.png)

2.  Con el Bloc de notas como aplicación activa, haga clic en el indicador de configuración regional de entrada y seleccione chino (PRC). La pantalla del indicador cambia a CH para reflejar que el nuevo idioma de entrada es Chino (PRC).

    ![Captura de pantalla que muestra el indicador de configuración regional de entrada para seleccionar chino (P R C).](images/ime-sc2.png)

3.  Coloque el cursor en el Bloc de notas. Presione Inicio en el teclado para que el cursor esté al principio de la línea. En el tipo de teclado "N", "I". En la ilustración siguiente se muestra el aspecto de la pantalla. El pequeño rectángulo horizontal es la ventana de lectura, que muestra la cadena de lectura actual. Actualmente, la cadena de lectura es "ni" como resultado de escribir "N" y "I".

    ![Captura de pantalla que muestra una cadena de lectura con ' n ' e ' i '.](images/ime-sc3.png)

4.  Escriba "3". Ahora el Bloc de notas tiene la siguiente pantalla. Dado que N + I + 3 es una pronunciación completa en pinyin de chino simplificado, el IME tiene suficiente información para prever el carácter que el usuario puede haber diseñado para entrar. La ventana de lectura desaparece porque ha escrito una pronunciación completa. Se muestra un carácter en la parte superior del cursor del Bloc de notas. Este carácter no forma parte del Bloc de notas, sino que se muestra en otra ventana encima del Bloc de notas y oculta los caracteres existentes en el Bloc de notas que están debajo. Esta nueva ventana se denomina ventana de composición y la cadena en ella se denomina cadena de composición. La cadena de composición está subrayada en la pantalla.

    ![Captura de pantalla que muestra una ventana de composición con una cadena de composición de un carácter.](images/ime-sc4.png)

5.  Ahora escriba "H", "A", "O", "3" para escribir otro carácter. Tenga en cuenta que la ventana de lectura aparece cuando se escribe "H" y desaparece cuando se escribe "3". Como se muestra a continuación, la cadena de composición contiene ahora dos caracteres.

    ![Captura de pantalla que muestra una ventana de composición con una cadena de composición de dos caracteres.](images/ime-sc5.png)

6.  Presione la flecha izquierda en el teclado una vez. El cursor de composición mueve un carácter a la izquierda, en el segundo carácter que ha escrito. Aparece una ventana encima del Bloc de notas, como se muestra a continuación. Esta ventana se denomina ventana candidata. Muestra una lista de caracteres o frases que coinciden con la pronunciación que ha escrito. Puede seleccionar la palabra deseada en las entradas de la lista de candidatos. En este ejemplo, hay dos caracteres candidatos disponibles con la misma pronunciación.

    ![dos caracteres candidatos disponibles con la misma pronunciación](images/ime-sc6.png)

7.  Escriba "2" para seleccionar la segunda entrada. La ventana candidata se cierra ahora y la cadena de composición se actualiza con el carácter seleccionado.

    ![Captura de pantalla que muestra una cadena de composición actualizada con el carácter seleccionado.](images/ime-sc7.png)

8.  Presione ENTRAR. Esto indica al IME que se ha completado la composición y que la cadena se debe enviar al bloc de notas de la aplicación en este ejemplo. La ventana de composición se cierra y los dos caracteres se envían al bloc de notas a través de WM \_ Char. El subrayado aparece en la ilustración siguiente, ya que los dos caracteres que se muestran forman parte del texto del Bloc de notas. El texto existente "ABCDEFG" en el Bloc de notas se mueve a la derecha porque se han insertado dos caracteres más. Ahora ha introducido correctamente dos caracteres de chino simplificado mediante un IME.

    ![se introdujeron correctamente dos caracteres de chino simplificado mediante un IME](images/ime-sc8.png)

## <a name="traditional-chinese-ime"></a>IME de chino tradicional

En esta sección se describe cómo usar el IME de chino tradicional (nuevo fonético) con el Bloc de notas para escribir algunos caracteres chinos.

1.  Inicie el Bloc de notas. Escriba algunos caracteres en el Bloc de notas. Estos caracteres le ayudarán a visualizar mejor la ventana del IME más adelante.

    ![Captura de pantalla que muestra los caracteres que ayudan a visualizar mejor la ventana I M E más adelante para el chino tradicional.](images/ime-tc1.png)

2.  Haga clic en el indicador de configuración regional de entrada en la barra de tareas de Windows y seleccione chino (Taiwán). El indicador muestra los cambios en CH para reflejar que el nuevo idioma de entrada es Chino (Taiwán).

    ![indicador de configuración regional de entrada para seleccionar chino (Taiwán)](images/ime-tc2.png)

3.  Coloque el cursor en el Bloc de notas. Presione Inicio en el teclado para que el cursor esté al principio de la línea. En el tipo de teclado "S", "U". En la ilustración siguiente se muestra el aspecto de la pantalla. El pequeño rectángulo vertical es la ventana de lectura, que muestra la cadena de lectura actual. Como se muestra en la ilustración siguiente, la cadena de lectura tiene dos caracteres como resultado de escribir "S" y "U".

    ![Captura de pantalla que muestra una cadena de lectura con dos caracteres.](images/ime-tc3.png)

4.  Escriba "3". Ahora el Bloc de notas tiene la siguiente pantalla. Como S + U + 3 es una pronunciación completa en chino tradicional, el IME tiene suficiente información para prever el carácter que el usuario puede haber diseñado para entrar. La ventana de lectura desaparece porque ha escrito una pronunciación completa. Se muestra un carácter en la parte superior del cursor del Bloc de notas. Este carácter no forma parte del Bloc de notas, sino que se muestra en otra ventana encima del Bloc de notas y oculta los caracteres existentes en el Bloc de notas que están debajo. Esta nueva ventana se denomina ventana de composición y la cadena en ella se denomina cadena de composición. La cadena de composición está subrayada en la pantalla.

    ![Captura de pantalla que muestra una ventana de composición con una cadena de composición subrayada.](images/ime-tc4.png)

5.  Ahora escriba "C", "L" y "3" para escribir otro carácter. Tenga en cuenta que la ventana de lectura aparece cuando "C" se escribe y desaparece cuando se escribe "3". Como se muestra a continuación, la cadena de composición contiene ahora dos caracteres.

    ![Captura de pantalla que muestra una ventana de composición con una cadena de composición y dos caracteres subrayados.](images/ime-tc5.png)

6.  Escriba la flecha hacia abajo en el teclado una vez. Aparece una ventana encima del Bloc de notas, como se muestra a continuación. Esta ventana se denomina ventana candidata. Muestra una lista de caracteres o frases que coinciden con la pronunciación que ha escrito. Puede seleccionar la palabra deseada en las entradas de la lista de candidatos. En este ejemplo, hay tres caracteres candidatos disponibles con la misma pronunciación.

    ![tres caracteres candidatos disponibles con la misma pronunciación](images/ime-tc6.png)

7.  Escriba "2" para seleccionar la segunda entrada. La ventana candidata se cierra ahora y la cadena de composición se actualiza con el carácter seleccionado.

    ![Captura de pantalla que muestra una cadena de composición actualizada con un carácter seleccionado.](images/ime-tc7.png)

8.  Presione ENTRAR. Esto indica al IME que se ha completado la composición y que la cadena se debe enviar al bloc de notas de la aplicación en este ejemplo. La ventana de composición se cierra y los dos caracteres se envían al bloc de notas a través de [**WM \_ Char**](/windows/desktop/inputdev/wm-char). El subrayado aparece en la ilustración siguiente, ya que los dos caracteres que se muestran forman parte del texto del Bloc de notas. El texto existente "ABCDEFG" en el Bloc de notas se mueve a la derecha porque se han insertado dos caracteres más. Ahora ha introducido correctamente dos caracteres de chino tradicional con un IME.

    ![se introdujeron correctamente dos caracteres de chino tradicional con un IME](images/ime-tc8.png)

## <a name="japanese-ime"></a>Japonés IME

Esta sección es un tutorial sobre el uso del IME japonés con el Bloc de notas para escribir algunos caracteres japoneses.

1.  Inicie el Bloc de notas. Escriba algunos caracteres en el Bloc de notas. Estos caracteres le ayudarán a visualizar mejor la ventana del IME más adelante.

    ![Captura de pantalla que muestra los caracteres que ayudan a visualizar la ventana I M E más adelante en japonés.](images/ime-j1.png)

2.  Con el Bloc de notas como aplicación activa, haga clic en el indicador de configuración regional de entrada y seleccione japonés. El indicador muestra los cambios en JP para reflejar que el nuevo idioma de entrada es el japonés.

    ![indicador de configuración regional de entrada para seleccionar japonés](images/ime-j2.png)

3.  Coloque el cursor en el Bloc de notas. Presione Inicio en el teclado para que el cursor esté al principio de la línea. En el tipo de teclado "N", "I". En la ilustración siguiente se muestra el aspecto de la pantalla. Como N + I es una pronunciación completa en japonés, el IME tiene información suficiente para prever el carácter que el usuario puede haber diseñado para entrar. Se muestra un carácter en la parte superior del cursor del Bloc de notas. Este carácter no forma parte del Bloc de notas, sino que se muestra en otra ventana encima del Bloc de notas y oculta los caracteres existentes en el Bloc de notas que están debajo. Esta nueva ventana se denomina ventana de composición y la cadena en ella se denomina cadena de composición. La cadena de composición está subrayada en la pantalla.

    ![Captura de pantalla que muestra una cadena de composición con un carácter japonés subrayado.](images/ime-j3.png)

4.  Ahora escriba "H", "O", "N", "G" y "O" para escribir dos caracteres más. La cadena de composición contiene ahora cuatro caracteres, como se muestra a continuación.

    ![Captura de pantalla que muestra una cadena de composición con cuatro caracteres japoneses subrayados.](images/ime-j4.png)

5.  Presione la barra espaciadora. Esto indica al IME que convierta el texto escrito en cláusulas. En la ilustración siguiente, el IME convierte la pronunciación "Nihongo" en una cláusula escrita en kanji que significa "idioma japonés".

    ![IME convierte la pronunciación japonesa](images/ime-j5.png)

6.  Presione la flecha abajo del teclado una vez. Aparece una ventana encima del Bloc de notas, como se muestra a continuación. Esta ventana se denomina ventana candidata. Muestra una lista de cláusulas que coinciden con la pronunciación que ha escrito. Puede seleccionar la palabra deseada en la lista de candidatos. En este ejemplo, hay tres caracteres candidatos disponibles con la misma pronunciación. Tenga en cuenta que la segunda entrada está resaltada y cambia la cadena de composición. Esto se debe a que se escribe la flecha hacia abajo, que indica al IME que seleccione la entrada después de la que se mostró anteriormente.

    ![Captura de pantalla que muestra la ventana candidato.](images/ime-j6.png)

7.  Escriba "2" para seleccionar la segunda entrada. La ventana candidata se cierra ahora y la cadena de composición se actualiza con el carácter seleccionado.

    ![Captura de pantalla que muestra la cadena de composición actualizada con el carácter japonés seleccionado.](images/ime-j7.png)

8.  Presione ENTRAR. Esto indica al IME que se ha completado la composición y que la cadena se debe enviar al bloc de notas de la aplicación en este ejemplo. La ventana de composición se cierra y los dos caracteres se envían al bloc de notas a través de [**WM \_ Char**](/windows/desktop/inputdev/wm-char). El subrayado aparece en la ilustración siguiente, ya que los dos caracteres que se muestran forman parte del texto del Bloc de notas. El texto existente "ABCDEFG" en el Bloc de notas se mueve a la derecha porque se han insertado dos caracteres más. Ahora ha escrito correctamente algunos caracteres japoneses con un IME.

    ![se escribieron correctamente algunos caracteres japoneses con un IME](images/ime-j8.png)

## <a name="korean-ime"></a>Coreano IME

En esta sección se describe cómo usar el IME coreano con el Bloc de notas para escribir algunos caracteres coreanos.

1.  Inicie el Bloc de notas. Escriba algunos caracteres en el Bloc de notas. Estos caracteres le ayudarán a visualizar mejor la ventana del IME más adelante.

    ![caracteres que ayudan a visualizar la ventana del IME mejor más adelante](images/ime-k1.png)

2.  Con el Bloc de notas como aplicación activa, haga clic en el indicador de configuración regional de entrada y seleccione Coreano. El indicador muestra los cambios en KO para reflejar que el nuevo idioma de entrada es Coreano.

    ![indicador de configuración regional de entrada para seleccionar Coreano](images/ime-k2.png)

3.  Coloque el cursor en el Bloc de notas. Presione Inicio en el teclado para que el cursor esté al principio de la línea y, a continuación, escriba "G". En la ilustración siguiente se muestra el aspecto de la pantalla. El elemento fonético correspondiente a "G" aparece en el Bloc de notas y se resalta con un cursor de bloque. Este carácter resaltado se denomina cadena de composición. Tenga en cuenta que, a diferencia del IME para otros lenguajes, la cadena de composición se envía al bloc de notas y se inserta a la izquierda del texto existente en cuanto el usuario escribe un único elemento fonético.

    ![Captura de pantalla que muestra una cadena de composición con un carácter insertado a la izquierda del texto existente.](images/ime-k3.png)

4.  En este momento, la cadena de composición consta de un carácter provisional porque cualquier elemento fonético adicional especificado por el usuario cambia la cadena de composición en su lugar. Ahora escriba "K" y luego "S". Tenga en cuenta que el carácter provisional cambia con cada pulsación de tecla.

    ![cadena de composición](images/ime-k4.png)

5.  Ahora, presione la tecla CTRL derecha. Aparece una ventana candidata que muestra los caracteres Hanja que puede seleccionar para la pronunciación introducida, G + K + S.

    ![Captura de pantalla que muestra una ventana candidata con una lista de caracteres Hanja que puede seleccionar en la parte inferior de la ventana.](images/ime-k5.png)

6.  Escriba el número "1" para seleccionar la primera entrada de la lista. La ventana candidata se cierra y la cadena de composición se actualiza con el carácter seleccionado.

    ![cadena de composición actualizada con el carácter seleccionado](images/ime-k6.png)

7.  Escriba "R", "N" y "R". A continuación, presione la tecla CTRL derecha para escribir otro carácter.

    ![ventana candidata](images/ime-k7.png)

8.  Escriba "1" para seleccionar la primera entrada. Ahora ha introducido correctamente dos caracteres coreanos mediante un IME. Los caracteres coreanos ya forman parte de la cadena de texto en el Bloc de notas.

    ![se introdujeron correctamente dos caracteres coreanos con un IME](images/ime-k8.png)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| **Sistema operativo**                | Windows XP                                                                                                 |
| **Espacio disponible en el disco duro**       | Al menos 230 MB                                                                                            |
| **Ubicaciones de archivos de idioma externo** | Disco compacto de instalación de Windows XP o ubicación de red con los archivos de instalación de Windows XP                |
| **Time**                            | Unos diez minutos para instalar archivos de idiomas externos; unos diez minutos cada uno para revisar cuatro IME diferentes. |



 

 

 
