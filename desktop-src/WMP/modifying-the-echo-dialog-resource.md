---
title: Modificar el recurso del cuadro de diálogo Eco
description: Modificar el recurso del cuadro de diálogo Eco
ms.assetid: 2a371004-82a5-42fb-b19c-ea1928a122a1
keywords:
- Reproductor de Windows Media complementos, páginas de propiedades de ejemplo echo
- complementos, páginas de propiedades de ejemplo de eco
- complementos de procesamiento de señales digitales, páginas de propiedades de ejemplo de eco
- Complementos de DSP, páginas de propiedades de ejemplo de eco
- Ejemplo de complemento DSP de eco, páginas de propiedades
- Ejemplo de complemento DSP de eco, recurso de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d37dc88fe2c1b85dfc08727a00e744f1c5c16a2f25a4c5d429b2ab13898b0fcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996145"
---
# <a name="modifying-the-echo-dialog-resource"></a>Modificar el recurso del cuadro de diálogo Eco

Debe cambiar el recurso de cuadro de diálogo que es la interfaz de usuario para el objeto de página de propiedades. En primer lugar, puede cambiar el cuadro de edición y la etiqueta existentes para que sean útiles para la propiedad delay time y, a continuación, agregar un segundo cuadro de edición y una etiqueta para la propiedad de mezcla con humedad.

Para editar el recurso de cuadro de diálogo en Visual C++:

1.  Haga clic en **la pestaña ResourceView** en el área Project trabajo.
2.  Expanda el árbol de recursos abriendo la carpeta de nivel superior.
3.  Abra la **carpeta Diálogo.**
4.  Haga doble clic en el nombre del recurso de cuadro de diálogo IDD \_ ECHOPROPPAGE. El editor de recursos aparece en el panel derecho.

## <a name="changing-the-existing-resources"></a>Cambiar los recursos existentes

Para cambiar los recursos de la página de propiedades existentes para la propiedad delay time:

1.  En primer lugar, cambie el texto en el control de texto estático existente. Haga clic con el botón derecho en el control y elija **Propiedades.** En el **campo Título,** escriba el nuevo título:
    ```C++
    Delay time (0 to 2000):
    
    ```

    

2.  Cierre el cuadro de diálogo Propiedades del texto .
3.  Ahora, cambie el nombre del control de cuadro de edición. Para ello, haga clic con el botón derecho en el control y elija **Propiedades.** En el **campo Id.,** escriba un nuevo nombre para el control:
    ```C++
    IDC_DELAYTIME
    
    ```

    

4.  Cierre el cuadro de diálogo Editar propiedades .
5.  Guarde el recurso.
6.  Responda **Sí** si se le pide que vuelva a cargar el archivo resource.h.
7.  Haga clic en **la pestaña Vista** de archivo en el área Project trabajo. Abra resource.h.
8.  Busque la \# definición del recurso del cuadro de edición del factor de escala (IDC \_ SCALEFACTOR) y elimínelo. Debe tener el mismo número de identificador que IDC \_ DELAYTIME.

## <a name="adding-the-new-resources"></a>Agregar los nuevos recursos

Para agregar los nuevos recursos de la página de propiedades para la propiedad de mezcla con humedad:

1.  Haga clic **en la pestaña ResourceView** del área Project de trabajo para seleccionarla.
2.  Haga doble clic en el nombre del cuadro de diálogo de la página de propiedades, IDD \_ ECHOPROPPAGE. El editor de recursos aparece en el panel derecho.
3.  Use el cuadro de herramientas para agregar un control de texto estático y un cuadro de edición a la página de propiedades.
4.  Haga clic con el botón derecho en el control de texto estático y elija **Propiedades.**
5.  Escriba un nuevo nombre para el control de texto estático en el **campo ID:**
    ```C++
    IDC_MIXLABEL
    
    ```

    

6.  Escriba un título para la etiqueta:
    ```C++
    Effect level (%):
    
    ```

    

7.  Cierre el cuadro de diálogo Propiedades del texto .
8.  Haga clic con el botón derecho en el cuadro de edición y elija **Propiedades.**
9.  Escriba un nuevo nombre para el cuadro de edición en el **campo Id.:**
    ```C++
    IDC_WETMIX
    
    ```

    

10. Cierre el cuadro de diálogo Editar propiedades .

Al guardar el proyecto, es posible que se le pida que vuelva a cargar resource.h. Haga **clic en Sí** si esto sucede. El editor de recursos del cuadro de diálogo debe agregar los nombres de recursos y los números de identificador a resource.h para los elementos agregados. Si por algún motivo esto no ocurre, debe abrir resource.h y escribir nuevas entradas para el control de etiqueta y cuadro de edición, y asignar a cada uno un número de identificador único.

## <a name="modifying-and-adding-the-string-resources"></a>Modificar y agregar los recursos de cadena

El código de ejemplo del asistente para complementos especifica un recurso de cadena denominado IDS SCALERANGEERROR que contiene un mensaje que se muestra cuando la entrada del usuario está \_ fuera del intervalo. Puede modificar este recurso para que se adapte a sus necesidades para el valor de tiempo de retraso siguiendo estos pasos en Visual C++:

1.  Haga clic en **la pestaña ResourceView.**
2.  Abra la **carpeta Tabla de** cadenas.
3.  Haga doble clic en el **icono Tabla de** cadenas para abrir el editor de recursos.
4.  Haga doble clic en el nombre del recurso que desea editar, en este caso, IDS \_ SCALERANGEERROR. Aparece el cuadro de diálogo Propiedades de cadena.
5.  Cambie el nombre del campo **ID** a IDS \_ DELAYRANGEERROR.
6.  Cambie el texto en el **campo Título:**
    ```C++
    You must enter a delay time between 0 and 2000 milliseconds.
    
    ```

    

7.  Cierre el cuadro de diálogo Propiedades de cadena .

A continuación, agregue un nuevo recurso de cadena para el mensaje de error de la propiedad mix.

1.  Haga doble clic en la línea vacía en la parte inferior del editor de recursos.
2.  Cambie el nombre del campo **ID** a IDS \_ MIXRANGEERROR.
3.  Agregue el texto siguiente al **campo Título:**
    ```C++
    You must enter an effect level between 0 and 100 percent.
    
    ```

    

4.  Cierre el cuadro de diálogo Propiedades de cadena .

Hay otros dos valores que deseará cambiar en la tabla de cadenas. IDS FRIENDLYNAME es el nombre que aparece en la Reproductor de Windows Media \_ de usuario para identificar el complemento. IDS \_ DESCRIPTION le permite decir al usuario sobre el complemento. Ambas cadenas se pasan como parámetros a la función **IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin,** a la que se llama en el método DllRegisterServer de Echodll.cpp.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Modificar la página de propiedades Echo Sample**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




