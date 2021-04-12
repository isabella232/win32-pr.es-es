---
title: Modificar el recurso de cuadro de diálogo echo
description: Modificar el recurso de cuadro de diálogo echo
ms.assetid: 2a371004-82a5-42fb-b19c-ea1928a122a1
keywords:
- Complementos de Windows Media Player, páginas de propiedades de ejemplo echo
- complementos, páginas de propiedades de ejemplo echo
- Complementos de procesamiento de señal digital, páginas de propiedades de ejemplo de eco
- Complementos DSP, páginas de propiedades de ejemplo echo
- Ejemplo de complemento de DSP de eco, páginas de propiedades
- Ejemplo de complemento de DSP de eco, recurso de cuadro de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09caa800376a7962a11912bc582a091f0de52c16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357405"
---
# <a name="modifying-the-echo-dialog-resource"></a>Modificar el recurso de cuadro de diálogo echo

Debe cambiar el recurso de cuadro de diálogo que es la interfaz de usuario del objeto de página de propiedades. En primer lugar, puede cambiar la etiqueta y el cuadro de edición existente para que sea útil para la propiedad tiempo de retraso y, a continuación, agregar un segundo cuadro de edición y una etiqueta para la propiedad mezcla húmeda.

Para editar el recurso de cuadro de diálogo en Visual C++:

1.  Haga clic en la pestaña **ResourceView** en el área de trabajo del proyecto.
2.  Expanda el árbol recursos abriendo la carpeta de nivel superior.
3.  Abra la carpeta del **cuadro de diálogo** .
4.  Haga doble clic en el nombre del recurso de cuadro de diálogo, IDD \_ ECHOPROPPAGE. El editor de recursos aparece en el panel derecho.

## <a name="changing-the-existing-resources"></a>Cambiar los recursos existentes

Para cambiar los recursos de la página de propiedades existente para la propiedad tiempo de retraso:

1.  En primer lugar, cambie el texto del control de texto estático existente. Haga clic con el botón secundario en el control y seleccione **propiedades**. En el campo **título** , escriba el nuevo título:
    ```C++
    Delay time (0 to 2000):
    
    ```

    

2.  Cierre el cuadro de diálogo Propiedades del texto.
3.  Ahora, cambie el nombre del control del cuadro de edición. Para ello, haga clic con el botón secundario en el control y, a continuación, elija **propiedades**. En el campo **ID** , escriba un nuevo nombre para el control:
    ```C++
    IDC_DELAYTIME
    
    ```

    

4.  Cierre el cuadro de diálogo Editar propiedades.
5.  Guarde el recurso.
6.  Responda **sí** si se le pide que vuelva a cargar el archivo resource. h.
7.  Haga clic en la pestaña **FileView** en el área de trabajo del proyecto. Abra Resource. h
8.  Busque el \# recurso de cuadro de edición definir para el factor de escala (IDC \_ SCALEFACTOR) y elimínelo. Debe tener el mismo número de identificador que IDC \_ DELAYTIME.

## <a name="adding-the-new-resources"></a>Agregar los nuevos recursos

Para agregar los recursos de la nueva página de propiedades para la propiedad Mix húmeda:

1.  Haga clic en la pestaña **ResourceView** en el área de trabajo del proyecto para seleccionarla.
2.  Haga doble clic en el nombre del cuadro de diálogo Página de propiedades, ECHOPROPPAGE de IDD \_ . El editor de recursos aparece en el panel derecho.
3.  Utilice el cuadro de herramientas para agregar un control de texto estático y un cuadro de edición a la página de propiedades.
4.  Haga clic con el botón secundario en el control texto estático y elija **propiedades**.
5.  Escriba un nuevo nombre para el control de texto estático en el campo **ID** :
    ```C++
    IDC_MIXLABEL
    
    ```

    

6.  Escriba un título para la etiqueta:
    ```C++
    Effect level (%):
    
    ```

    

7.  Cierre el cuadro de diálogo Propiedades del texto.
8.  Haga clic con el botón secundario en el cuadro de edición y elija **propiedades**.
9.  Escriba un nuevo nombre para el cuadro de edición en el campo **ID** :
    ```C++
    IDC_WETMIX
    
    ```

    

10. Cierre el cuadro de diálogo Editar propiedades.

Al guardar el proyecto, es posible que se le pida que vuelva a cargar Resource. h. Si esto ocurre, haga clic en **sí** . El editor de recursos del cuadro de diálogo debe agregar los nombres de recursos y los números de identificador a Resource. h para los elementos que agregó. Si por alguna razón esto no sucede, debe abrir Resource. h y escribir nuevas entradas para el control etiqueta y editar cuadro y asignar cada número de identificador único.

## <a name="modifying-and-adding-the-string-resources"></a>Modificar y agregar los recursos de cadena

El código de ejemplo del Asistente para complementos especifica un recurso de cadena denominado IDS \_ SCALERANGEERROR que contiene un mensaje que se muestra cuando la entrada del usuario está fuera del intervalo. Puede modificar este recurso para que se adapte a sus necesidades del valor de tiempo de retraso siguiendo estos pasos en Visual C++:

1.  Haga clic en la pestaña **ResourceView** .
2.  Abra la carpeta de la **tabla de cadenas** .
3.  Haga doble clic en el icono de la **tabla de cadenas** para abrir el editor de recursos.
4.  Haga doble clic en el nombre del recurso que desea editar, en este caso, IDS \_ SCALERANGEERROR. Aparecerá el cuadro de diálogo Propiedades de la cadena.
5.  Cambie el nombre del campo **ID** a ID \_ DELAYRANGEERROR.
6.  Cambie el texto en el campo de **título** :
    ```C++
    You must enter a delay time between 0 and 2000 milliseconds.
    
    ```

    

7.  Cierre el cuadro de diálogo Propiedades de la cadena.

Después, agregue un nuevo recurso de cadena para el mensaje de error de la propiedad Mix húmeda.

1.  Haga doble clic en la línea vacía en la parte inferior del editor de recursos.
2.  Cambie el nombre del campo **ID** a ID \_ MIXRANGEERROR.
3.  Agregue el texto siguiente al campo de **título** :
    ```C++
    You must enter an effect level between 0 and 100 percent.
    
    ```

    

4.  Cierre el cuadro de diálogo Propiedades de la cadena.

Hay otros dos valores que desea cambiar en la tabla de cadenas. ID \_ . FRIENDLYNAME es el nombre que aparece en la interfaz de usuario de Media Player de Windows para identificar el complemento. \_La descripción de IDS le permite indicar al usuario sobre el complemento. Ambas cadenas se pasan como parámetros a la función **IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin** , a la que se llama en el método DllRegisterServer en Echodll. cpp.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Modificar la página de propiedades de ejemplo echo**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




