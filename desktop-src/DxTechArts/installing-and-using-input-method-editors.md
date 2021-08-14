---
title: Instalación y uso de editores de métodos de entrada
description: En este artículo se ofrece un tutorial sobre cómo instalar y usar el editor Windows métodos de entrada (IME) estándar.
ms.assetid: 0dc430ce-bed4-8d02-f45e-4eefb0ad0369
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b45a0da52d0e917186831de8c84f39ecee3d2583ac4a267fa2501c643e2f75f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118153665"
---
# <a name="installing-and-using-input-method-editors"></a>Instalación y uso de editores de métodos de entrada

En este artículo se ofrece un tutorial sobre cómo instalar y usar el editor Windows métodos de entrada (IME) estándar.

-   [Instalación de un editor de métodos de entrada](#installing-an-input-method-editor)
-   [IME chino simplificado](#simplified-chinese-ime)
-   [IME chino tradicional](#traditional-chinese-ime)
-   [Japonés IME](#japanese-ime)
-   [Coreano IME](#korean-ime)
-   [Requisitos](#requirements)

## <a name="installing-an-input-method-editor"></a>Instalación de un editor de métodos de entrada

En las secciones siguientes se describe cómo instalar y usar editores de métodos de entrada (IME) para escribir caracteres complejos en cuatro idiomas de Asia Oriental diferentes. Se analizan las características únicas de cada lenguaje.

Para implementar la funcionalidad del Editor de métodos de entrada (IME) en una aplicación, consulte [Uso de un editor de métodos de entrada en un juego.](/windows/desktop/DxTechArts/using-an-input-method-editor-in-a-game)

Un IME no está instalado en microsoft Windows XP de forma predeterminada. Para realizar la instalación, complete los pasos siguientes.

**Para instalar un IME**

1.  En la Panel de control, abra Opciones regionales y de idioma.
2.  En la pestaña Idiomas, active la casilla Instalar archivos para idiomas de Asia Oriental.

    ![pestaña idiomas de las opciones regionales y de idioma](images/ime-1.png)

    Aparece un cuadro de diálogo Instalar compatibilidad complementaria de idioma que le informa de los requisitos de almacenamiento de los archivos de idioma.

    ![instalar compatibilidad con idiomas complementarios, cuadro de diálogo](images/ime-install-lang-dialog.png)

3.  Haga clic en Aceptar para cerrar el cuadro de diálogo.
4.  Haga clic en Aceptar en la pestaña Idiomas.
5.  Aparece otro cuadro de diálogo que solicita un disco Windows XP o una ubicación de recurso compartido de red donde se encuentran los archivos de compatibilidad de idioma. Inserte un disco Windows XP compact o vaya a la ubicación de red adecuada y haga clic en Aceptar. Microsoft Windows instala los archivos necesarios y le pide que reinicie el equipo.
6.  Haga clic en Sí para reiniciar el equipo.
7.  Después de reiniciar, vuelva a abrir el panel de control Opciones regionales y de idioma.
8.  En la pestaña Idiomas, haga clic en Detalles. Aparece la ventana Text Services and Input Languages (Servicios de texto e idiomas de entrada).

    ![Ext services and input languages window (Ventana de servicios ext e idiomas de entrada)](images/ime-2.png)

9.  En la pestaña Configuración, haga clic en Agregar. Aparece la ventana Agregar idioma de entrada.

    ![ventana agregar idioma de entrada](images/ime-3.png)

10. Seleccione Chino (Taiwán) como idioma de entrada y Microsoft New Phonetic IME 2002a for keyboard layout/IME (Nuevo IME fonético 2002a para diseño de teclado/IME).
11. Haga clic en Aceptar. Ahora puede agregar idiomas e IME adicionales de forma similar.
12. Haga clic en Agregar de nuevo, seleccione Chino (PRC) para idioma de entrada y Chino (simplificado): Microsoft Pinyin IME 3.0 para el diseño de teclado/IME y, a continuación, haga clic en Aceptar.
13. Haga clic en Agregar de nuevo, seleccione Japonés para el idioma de entrada y Microsoft IME Standard 2002 ver. 8.1 para el diseño de teclado/IME y, a continuación, haga clic en Aceptar.
14. Haga clic en Agregar de nuevo, seleccione Coreano para idioma de entrada y Sistema de entrada coreano (IME 2002) para el diseño de teclado/IME y, a continuación, haga clic en Aceptar. En la ventana Servicios de texto e idiomas de entrada, el cuadro de lista Servicios instalados ahora debe contener los cuatro IME recién agregados.

    ![cuadro de lista de servicios instalados](images/ime-7.png)

15. Haga clic en Aceptar para cerrar la ventana Servicios de texto e idiomas de entrada.
16. Haga clic en Aceptar para cerrar el panel de control Opciones regionales y de idioma. La Windows de tareas debe contener ahora un indicador de configuración regional de entrada con un círculo rojo. La existencia del indicador significa que se ha instalado más de un idioma de entrada en el sistema.

    ![indicador que indica que se ha instalado más de un idioma de entrada en el sistema](images/ime-8.png)

## <a name="simplified-chinese-ime"></a>IME chino simplificado

En esta sección se describe cómo usar el IME chino simplificado (PinYin) con Microsoft Bloc de notas escribir algunos caracteres en chino.

1.  Inicie Bloc de notas (disponible en la botón Inicio y, a continuación, seleccione Todos los programas y accesorios). Escriba algunos caracteres en Bloc de notas. Estos caracteres le ayudarán a visualizar mejor la ventana de IME más adelante.

    ![Screnshot que muestra los caracteres que ayudan a visualizar mejor la ventana de I M E más adelante para chino simplificado.](images/ime-sc1.png)

2.  Con Bloc de notas como aplicación activa, haga clic en el indicador de configuración regional de entrada y seleccione Chino (PRC). El indicador muestra los cambios en CH para reflejar que el nuevo idioma de entrada es chino (PRC).

    ![Captura de pantalla que muestra el indicador de configuración regional de entrada para seleccionar chino (P R C).](images/ime-sc2.png)

3.  Coloque el cursor en Bloc de notas. Presione INICIO en el teclado para que el cursor esté al principio de la línea. En el teclado, escriba "N", a continuación, "I". En la ilustración siguiente se muestra la apariencia de la pantalla. El pequeño rectángulo horizontal es la ventana de lectura, que muestra la cadena de lectura actual. Actualmente, la cadena de lectura es "ni" como resultado de escribir "N" e "I".

    ![Captura de pantalla que muestra una cadena de lectura con "n" e "i".](images/ime-sc3.png)

4.  Escriba "3". Ahora Bloc de notas muestra lo siguiente. Dado que N+I+3 es una pronunciación completa en Pinyin chino simplificado, el IME tiene suficiente información para prever el carácter que el usuario puede haber pensado escribir. La ventana de lectura desaparece porque ha escrito una pronunciación completa. Se muestra un carácter en la parte superior del cursor Bloc de notas cursor. Este carácter no forma parte de Bloc de notas, sino que se muestra en otra ventana encima de Bloc de notas y oculta los caracteres existentes en Bloc de notas que están debajo. Esta nueva ventana se denomina ventana de composición y la cadena en ella se denomina cadena de composición. La cadena de composición se subraya en la pantalla.

    ![Captura de pantalla que muestra una ventana de composición con una cadena de composición de un carácter.](images/ime-sc4.png)

5.  Ahora escriba "H", "A", "O", "3" para escribir otro carácter. Tenga en cuenta que la ventana de lectura se muestra cuando se escribe "H" y desaparece cuando se escribe "3". Como se muestra a continuación, la cadena de composición ahora contiene dos caracteres.

    ![Captura de pantalla que muestra una ventana de composición con una cadena de composición de dos caracteres.](images/ime-sc5.png)

6.  Presione una vez la flecha izquierda en el teclado. El cursor de composición mueve un carácter a la izquierda, en el segundo carácter que ha especificado. Aparece una ventana en la parte superior Bloc de notas como se muestra a continuación. Esta ventana se denomina ventana candidata. Muestra una lista de caracteres o frases que coinciden con la pronunciación que ha especificado. Puede seleccionar la palabra deseada entre las entradas de la lista de candidatos. En este ejemplo, hay dos caracteres candidatos disponibles con la misma pronunciación.

    ![dos caracteres candidatos disponibles con la misma pronunciación](images/ime-sc6.png)

7.  Escriba "2" para seleccionar la segunda entrada. Ahora se cierra la ventana candidata y la cadena de composición se actualiza con el carácter seleccionado.

    ![Captura de pantalla que muestra una cadena de composición actualizada con el carácter seleccionado.](images/ime-sc7.png)

8.  Presione ENTRAR. Esto indica al IME que la composición está completa y que la cadena se debe enviar a la aplicación, Bloc de notas en este ejemplo. La ventana de composición se cierra y los dos caracteres se envían a Bloc de notas a través de WM \_ CHAR. El subrayado ha desaparecido en la ilustración siguiente porque los dos caracteres mostrados forman parte del texto de Bloc de notas. El texto existente "ABCDEFG" en Bloc de notas se mueve a la derecha porque se han insertado dos caracteres más. Ahora ha escrito correctamente dos caracteres de chino simplificado mediante un IME.

    ![escribió correctamente dos caracteres chino simplificados mediante un ime.](images/ime-sc8.png)

## <a name="traditional-chinese-ime"></a>IME chino tradicional

En esta sección se describe cómo usar el IME chino tradicional (nuevo fonético) con Bloc de notas escribir algunos caracteres en chino.

1.  Inicie el Bloc de notas. Escriba algunos caracteres en Bloc de notas. Estos caracteres le ayudarán a visualizar mejor la ventana de IME más adelante.

    ![Captura de pantalla que muestra los caracteres que ayudan a visualizar mejor la ventana de I M E más adelante para chino tradicional.](images/ime-tc1.png)

2.  Haga clic en el indicador de configuración regional de entrada Windows la barra de tareas y seleccione Chino (Taiwán). El indicador muestra los cambios en CH para reflejar que el nuevo idioma de entrada es chino (Taiwán).

    ![indicador de configuración regional de entrada para seleccionar chino (Taiwán)](images/ime-tc2.png)

3.  Coloque el cursor en Bloc de notas. Presione INICIO en el teclado para que el cursor esté al principio de la línea. En el teclado, escriba "S", a continuación, "U". En la ilustración siguiente se muestra la apariencia de la pantalla. El pequeño rectángulo vertical es la ventana de lectura, que muestra la cadena de lectura actual. Como se muestra en la ilustración siguiente, la cadena de lectura tiene dos caracteres como resultado de escribir "S" y "U".

    ![Captura de pantalla que muestra una cadena de lectura con dos caracteres.](images/ime-tc3.png)

4.  Escriba "3". Ahora Bloc de notas muestra lo siguiente. Dado que S+U+3 es una pronunciación completa en chino tradicional, el IME tiene suficiente información para prever el carácter que el usuario podría haber pensado escribir. La ventana de lectura desaparece porque ha escrito una pronunciación completa. Se muestra un carácter en la parte superior del cursor Bloc de notas cursor. Este carácter no forma parte de Bloc de notas, sino que se muestra en otra ventana encima de Bloc de notas y oculta los caracteres existentes en Bloc de notas que están debajo. Esta nueva ventana se denomina ventana de composición y la cadena en ella se denomina cadena de composición. La cadena de composición se subraya en la pantalla.

    ![Captura de pantalla que muestra una ventana de composición con una cadena de composición subrayada.](images/ime-tc4.png)

5.  Ahora escriba "C", "L" y "3" para escribir otro carácter. Tenga en cuenta que la ventana de lectura se muestra cuando se escribe "C" y desaparece cuando se escribe "3". Como se muestra a continuación, la cadena de composición ahora contiene dos caracteres.

    ![Captura de pantalla que muestra una ventana de composición con una cadena de composición y dos caracteres subrayados.](images/ime-tc5.png)

6.  Escriba una vez la flecha abajo en el teclado. Aparece una ventana en la parte superior Bloc de notas como se muestra a continuación. Esta ventana se denomina ventana candidata. Muestra una lista de caracteres o frases que coinciden con la pronunciación que ha especificado. Puede seleccionar la palabra deseada entre las entradas de la lista de candidatos. En este ejemplo, hay tres caracteres candidatos disponibles con la misma pronunciación.

    ![tres caracteres candidatos disponibles con la misma pronunciación](images/ime-tc6.png)

7.  Escriba "2" para seleccionar la segunda entrada. Ahora se cierra la ventana candidata y la cadena de composición se actualiza con el carácter seleccionado.

    ![Captura de pantalla que muestra una cadena de composición actualizada con un carácter seleccionado.](images/ime-tc7.png)

8.  Presione ENTRAR. Esto indica al IME que la composición está completa y que la cadena se debe enviar a la aplicación, Bloc de notas en este ejemplo. La ventana de composición se cierra y los dos caracteres se envían a Bloc de notas a través de [**WM \_ CHAR**](/windows/desktop/inputdev/wm-char). El subrayado ha desaparecido en la ilustración siguiente porque los dos caracteres mostrados forman parte del texto de Bloc de notas. El texto existente "ABCDEFG" en Bloc de notas se mueve a la derecha porque se han insertado dos caracteres más. Ahora ha escrito correctamente dos caracteres de chino tradicional mediante un IME.

    ![escribió correctamente dos caracteres chino tradicionales mediante un ime](images/ime-tc8.png)

## <a name="japanese-ime"></a>Japonés IME

Esta sección es un recorrido por el uso del IME japonés Bloc de notas escribir algunos caracteres japoneses.

1.  Inicie el Bloc de notas. Escriba algunos caracteres en Bloc de notas. Estos caracteres le ayudarán a visualizar mejor la ventana de IME más adelante.

    ![Captura de pantalla que muestra los caracteres que ayudan a visualizar mejor la ventana de E/S más adelante para japonés.](images/ime-j1.png)

2.  Con Bloc de notas la aplicación activa, haga clic en el indicador de configuración regional de entrada y seleccione Japonés. El indicador muestra los cambios en JP para reflejar que el nuevo idioma de entrada es japonés.

    ![indicador de configuración regional de entrada para seleccionar japonés](images/ime-j2.png)

3.  Coloque el cursor en Bloc de notas. Presione INICIO en el teclado para que el cursor esté al principio de la línea. En el teclado, escriba "N", a continuación, "I". En la ilustración siguiente se muestra la apariencia de la pantalla. Dado que N+I es una pronunciación completa en japonés, el IME tiene suficiente información para prever el carácter que el usuario puede haber pensado escribir. Se muestra un carácter en la parte superior del cursor Bloc de notas cursor. Este carácter no forma parte de Bloc de notas, sino que se muestra en otra ventana encima de Bloc de notas y oculta los caracteres existentes en Bloc de notas que están debajo. Esta nueva ventana se denomina ventana de composición y la cadena en ella se denomina cadena de composición. La cadena de composición se subraya en la pantalla.

    ![Captura de pantalla que muestra una cadena de composición con un carácter japonés subrayado.](images/ime-j3.png)

4.  Ahora escriba "H", "O", "N", "G" y "O" para escribir dos caracteres más. La cadena de composición ahora contiene cuatro caracteres, como se muestra a continuación.

    ![Captura de pantalla que muestra una cadena de composición con cuatro caracteres japoneses subrayados.](images/ime-j4.png)

5.  Presione la barra espaciador. Esto indica al IME que convierta el texto especificado en cláusulas. En la ilustración siguiente, el IME convierte la pronunciación "Nihongo" en una cláusula escrita en Kanji que significa "japonés".

    ![ime convierte la pronunciación japonesa](images/ime-j5.png)

6.  Presione la flecha abajo en el teclado una vez. Aparece una ventana en la parte superior Bloc de notas como se muestra a continuación. Esta ventana se denomina ventana candidata. Muestra una lista de cláusulas que coinciden con la pronunciación que ha especificado. Puede seleccionar la palabra deseada en la lista de candidatos. En este ejemplo, hay tres caracteres candidatos disponibles con la misma pronunciación. Tenga en cuenta que la segunda entrada está resaltada y cambia la cadena de composición. Esto se debe a que se escribe la flecha abajo, que indica al IME que seleccione la entrada después de la que se mostró anteriormente.

    ![Captura de pantalla que muestra la ventana candidata.](images/ime-j6.png)

7.  Escriba "2" para seleccionar la segunda entrada. Ahora se cierra la ventana candidata y la cadena de composición se actualiza con el carácter seleccionado.

    ![Captura de pantalla que muestra la cadena de composición actualizada con el carácter japonés seleccionado.](images/ime-j7.png)

8.  Presione ENTRAR. Esto indica al IME que la composición está completa y que la cadena se debe enviar a la aplicación, Bloc de notas en este ejemplo. La ventana de composición se cierra y los dos caracteres se envían a Bloc de notas a través de [**WM \_ CHAR**](/windows/desktop/inputdev/wm-char). El subrayado ha desaparecido en la ilustración siguiente porque los dos caracteres mostrados forman parte del texto de Bloc de notas. El texto existente "ABCDEFG" en Bloc de notas se mueve a la derecha porque se han insertado dos caracteres más. Ahora ha escrito correctamente algunos caracteres japoneses mediante un IME.

    ![escribió correctamente algunos caracteres japoneses con un ime.](images/ime-j8.png)

## <a name="korean-ime"></a>Coreano IME

En esta sección se describe cómo usar el IME coreano Bloc de notas escribir algunos caracteres coreanos.

1.  Inicie el Bloc de notas. Escriba algunos caracteres en Bloc de notas. Estos caracteres le ayudarán a visualizar mejor la ventana de IME más adelante.

    ![caracteres que ayudan a visualizar mejor la ventana de ime más adelante](images/ime-k1.png)

2.  Con Bloc de notas la aplicación activa, haga clic en el indicador de configuración regional de entrada y seleccione Coreano. El indicador muestra los cambios en ko para reflejar que el nuevo idioma de entrada es coreano.

    ![indicador de configuración regional de entrada para seleccionar coreano](images/ime-k2.png)

3.  Coloque el cursor en Bloc de notas. Presione INICIO en el teclado para que el cursor esté al principio de la línea y, a continuación, escriba "G". En la ilustración siguiente se muestra la apariencia de la pantalla. El elemento fonético correspondiente a "G" aparece en Bloc de notas y se resalta con un cursor de bloque. Este carácter resaltado se denomina cadena de composición. Tenga en cuenta que, a diferencia del IME para otros idiomas, la cadena de composición se envía a Bloc de notas y se inserta a la izquierda del texto existente en cuanto el usuario escribe un único elemento fonético.

    ![Captura de pantalla que muestra una cadena de composición con un carácter insertado a la izquierda del texto existente.](images/ime-k3.png)

4.  En este momento, la cadena de composición consta de un carácter provisional porque los elementos fonéticos adicionales especificados por el usuario cambian la cadena de composición en su lugar. Ahora escriba "K" y, a continuación, "S". Tenga en cuenta que el carácter provisional cambia con cada pulsación de tecla.

    ![cadena de composición](images/ime-k4.png)

5.  Ahora presione la tecla CTRL derecha. Aparece una ventana candidata que muestra los caracteres hanja que puede seleccionar para la pronunciación especificada, G+K+S.

    ![Captura de pantalla que muestra una ventana candidata con una lista de caracteres hanja que puede seleccionar en la parte inferior de la ventana.](images/ime-k5.png)

6.  Escriba el número "1" para seleccionar la primera entrada de la lista. Se cierra la ventana candidata y la cadena de composición se actualiza con el carácter seleccionado.

    ![cadena de composición actualizada con el carácter seleccionado](images/ime-k6.png)

7.  Escriba "R", "N" y "R". A continuación, presione la tecla CTRL derecha para escribir otro carácter.

    ![ventana candidata](images/ime-k7.png)

8.  Escriba "1" para seleccionar la primera entrada. Ahora ha escrito correctamente dos caracteres coreanos mediante un IME. Los caracteres coreanos ya forman parte de la cadena de texto en Bloc de notas.

    ![escribió correctamente dos caracteres coreanos con un ime](images/ime-k8.png)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| **Sistema operativo**                | Windows XP                                                                                                 |
| **Espacio disponible en disco duro**       | Al menos 230 MB                                                                                            |
| **Ubicaciones de archivos de idioma externo** | Windows Xp installation compact disk or network location with Windows XP installation files (Xp installation disk or network location with Windows XP installation files                |
| **Time**                            | Unos diez minutos para instalar archivos de idioma externo; unos diez minutos cada uno para revisar cuatro IME diferentes. |



 

 

 
