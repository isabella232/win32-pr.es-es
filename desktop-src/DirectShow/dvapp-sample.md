---
description: Ejemplo de DVApp
ms.assetid: 80375170-d0d6-4371-abe3-078703e158b1
title: Ejemplo de DVApp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86653781d08921bf638e7798fb34f3a86e8d34a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152438"
---
# <a name="dvapp-sample"></a>Ejemplo de DVApp

## <a name="description"></a>Descripción

Aplicación de captura de vídeo digital (DV).

Este ejemplo muestra cómo crear varios tipos de gráficos de filtro para controlar las videocámaras DV. También muestra cómo realizar la captura, la vista previa, la transmisión y el control de dispositivos con una videocámara DV.

### <a name="usage"></a>Uso

La aplicación DVApp admite los siguientes modos:

-   Versión preliminar: representa el DV del camascopio en una ventana de vídeo.
-   DV to Type-1 file: captura datos de DV del camascopio en un archivo DV de tipo 1.
-   Archivo de tipo 1 a DV: transmite datos de un archivo DV de tipo 1 a la videocámara.
-   DV to Type-2 File: captura los datos de DV del camascopio en un archivo DV de tipo 2.
-   Escriba-2 archivo en DV: transmite datos de un archivo DV de tipo 2 a la videocámara.

Los modos de captura y transmisión también realizan la vista previa. Cada uno de esos modos tiene también una opción **no vista previa** , lo que deshabilita la vista previa. La captura sin vista previa es más eficaz y puede reducir el número de fotogramas quitados.

La aplicación se inicia en modo de vista previa. Para seleccionar otro modo, elija un modo en el menú **modo de gráfico** . En cada modo, DVApp crea un gráfico de filtros que admite la funcionalidad de ese modo. Para guardar el gráfico como un archivo GraphEdit (. GRF), seleccione **guardar el gráfico en el archivo** en el menú **archivo** . Salga de DVApp antes de abrir el archivo en GraphEdit.

Para capturar en un archivo:

1.  En el menú **archivo** , elija **establecer archivo de salida** y escriba un nombre de archivo.
2.  En el menú **modo de gráfico** , seleccione un modo de *DV a archivo* (tipo 1 o 2, con o sin vista previa).
3.  Haga clic en **registro**.
4.  Si el camascopio está en modo VTR, haga clic en **reproducir**.
5.  Para detener la captura, haga clic en **detener**.

Para transmitir desde un archivo al camascopio:

1.  En el menú **archivo** , haga clic en **establecer archivo de entrada** y seleccione un archivo DV. El archivo debe coincidir con el modo seleccionado (tipo 1 o tipo 2).
2.  En el menú **modo de gráfico** , seleccione un *archivo en modo DV* (tipo 1 o tipo 2, con o sin vista previa).
3.  Haga clic en **Reproducir**.
4.  Para grabar los datos en cinta, haga clic en **grabar**.
5.  Para detener la transmisión, haga clic en **detener**.

Si el camascopio está en modo VTR, el usuario puede controlar el mecanismo de transporte a través de los botones de estilo VCR de la aplicación. Para buscar la cinta, escriba el código de acceso de destino y haga clic en el botón Buscar.

Para limitar la cantidad de datos que captura la aplicación, elija **capturar tamaño** en el menú **archivo** .

Para comprobar el formato de cinta (NTSC o PAL), seleccione **comprobar cinta** en el menú de **Opciones** .

Para cambiar el tamaño de la ventana de vista previa, elija **cambiar el tamaño de descodificación** en el menú **Opciones** .

### <a name="programming-notes"></a>Notas de programación

El propósito principal de esta aplicación es mostrar cómo crear varios gráficos de captura y transmisión de DV.

### <a name="device-arrival-and-removal"></a>Llegada y eliminación de dispositivos

La aplicación controla la llegada y eliminación de dispositivos, con dos técnicas diferentes. En el caso de la llegada del dispositivo, el bucle de mensajes de la aplicación responde a \_ los mensajes de WM DEVICECHANGE. Para la eliminación del dispositivo, la aplicación responde a los eventos [**\_ \_ perdidos del dispositivo EC**](ec-device-lost.md) desde el administrador de gráficos de filtro. Cualquier enfoque funciona, aunque el \_ evento de dispositivo EC \_ perdido depende de la existencia del dispositivo en el gráfico de filtros.

La aplicación solo controla un dispositivo cada vez. Si se quita el dispositivo actual, la aplicación busca otro dispositivo DV en el sistema.

En algunas videocámaras DV, el usuario debe apagar el dispositivo cuando lo cambie entre el modo de cámara y el modo VTR, lo que desencadena un mensaje perdido del dispositivo. La aplicación responde habilitando o deshabilitando los comandos de menú correspondientes. Sin embargo, si el usuario alterna rápidamente entre los modos, es posible que la videocámara no genere un mensaje perdido por el dispositivo. Puede forzar la actualización de los menús eligiendo el **modo de actualización** en el menú **Opciones** . Algunas videocámaras DV pueden alternar entre modos sin apagar, pero solo se envía un mensaje de pérdida del dispositivo cuando cambian al modo VTR.

### <a name="device-control"></a>Control de dispositivos

La funcionalidad del botón **reproducir** y **grabar** depende del modo actual:

-   Versión preliminar: el gráfico de filtros se ejecuta automáticamente. El botón de **reproducción** inicia el transporte.
-   Capturar en archivo: el botón **grabar** ejecuta el gráfico y el botón de **reproducción** inicia el transporte.
-   Transmitir al dispositivo: el botón **reproducir** ejecuta el gráfico y el botón **grabar** inicia el transporte.

La aplicación de ejemplo no realiza la captura con precisión de fotogramas. En varios puntos, la aplicación llama a la función **Sleep** para esperar a que el dispositivo responda. Las camcorders DV más recientes envían una notificación cuando cambia el estado del dispositivo. Es posible que los dispositivos más antiguos no admitan notificaciones; para los fines de un ejemplo, llamar a **Sleep** es una solución más sencilla.

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Para descargar los ejemplos del SDK de DirectShow, instale la versión más reciente de la [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Este ejemplo se instala en la siguiente ruta de acceso: ejemplos *\[ raíz \] del SDK* \\ \\ multimedia \\ DirectShow \\ Capture \\ DVApp.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de una videocámara DV](controlling-a-dv-camcorder.md)
</dt> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Ejemplos de DirectShow](directshow-samples.md)
</dt> </dl>

 

 



