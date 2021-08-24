---
description: Ejemplo de DVApp
ms.assetid: 80375170-d0d6-4371-abe3-078703e158b1
title: Ejemplo de DVApp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72067c04e108354c1706690bc71e8b339ad5af071c46cc0e4102ae10e9a3643f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148728"
---
# <a name="dvapp-sample"></a>Ejemplo de DVApp

## <a name="description"></a>Descripción

Aplicación de captura de Vídeo digital (DV).

En este ejemplo se muestra cómo crear varios tipos de gráficos de filtro para controlar las cámaras DV. También se muestra cómo realizar la captura, vista previa, transmisión y control de dispositivos con una cámara dv.

### <a name="usage"></a>Uso

La aplicación DVApp admite los siguientes modos:

-   Versión preliminar: representa DV desde la cámara de vídeo en una ventana de vídeo.
-   DV a archivo de tipo 1: captura los datos de DV de la cámara en un archivo DV de tipo 1.
-   Archivo de tipo 1 a DV: transmite datos de un archivo DV de tipo 1 a la cámara de vídeo.
-   Dv a archivo de tipo 2: captura los datos de DV de la cámara en un archivo DV de tipo 2.
-   Archivo de tipo 2 a DV: transmite datos de un archivo DV de tipo 2 a la cámara de vídeo.

Los modos de captura y transmisión también realizan la versión preliminar. Cada uno de esos modos también tiene una **opción Sin** vista previa, que deshabilita la vista previa. La captura sin versión preliminar es más eficaz y puede reducir el número de fotogramas descartados.

La aplicación se inicia en modo de vista previa. Para seleccionar otro modo, elija un modo en el **menú Graph modo** automático. Para cada modo, DVApp crea un gráfico de filtro que admite la funcionalidad de ese modo. Para guardar el gráfico como un archivo GraphEdit (.grf), seleccione Guardar Graph **en** archivo en el **menú** Archivo. Salga de DVApp antes de abrir el archivo en GraphEdit.

Para capturar en un archivo:

1.  En el **menú Archivo,** elija **Establecer archivo de salida** y escriba un nombre de archivo.
2.  En el **Graph modo** de acceso, seleccione *un dv* a modo de archivo (tipo 1 o 2, con o sin vista previa).
3.  Haga clic **en Grabar**.
4.  Si la cámara está en modo VTR, haga clic en **Reproducir**.
5.  Para detener la captura, haga clic **en Detener**.

Para transmitir desde un archivo a la cámara de vídeo:

1.  En el **menú Archivo,** haga clic **en Establecer archivo de entrada** y seleccione un archivo DV. El archivo debe coincidir con el modo seleccionado (tipo 1 o tipo 2).
2.  En el **menú Graph,** seleccione un modo Archivo a *DV* (tipo 1 o tipo 2, con o sin vista previa).
3.  Haga clic en **Reproducir**.
4.  Para grabar los datos en cinta, haga clic en **Grabar.**
5.  Para detener la transmisión, haga clic **en Detener**.

Si la cámara está en modo VTR, el usuario puede controlar el mecanismo de transporte a través de los botones de estilo VCR de la aplicación. Para buscar la cinta, escriba el código de tiempo de destino y haga clic en el botón Buscar.

Para limitar la cantidad de datos que captura la aplicación, elija **Tamaño de captura** en el **menú** Archivo.

Para comprobar el formato de cinta ( TAPE o PAL), elija **Comprobar cinta** en el **menú** Opciones.

Para cambiar el tamaño de la ventana de vista previa, elija **Cambiar tamaño de descodificación** en el **menú** Opciones.

### <a name="programming-notes"></a>Notas de programación

El propósito principal de esta aplicación es mostrar cómo crear varios gráficos de captura y transmisión de DV.

### <a name="device-arrival-and-removal"></a>Llegada y eliminación de dispositivos

La aplicación controla la llegada y eliminación del dispositivo mediante dos técnicas diferentes. Para la llegada del dispositivo, el bucle de mensajes de la aplicación responde a los mensajes DE WM \_ DEVICECHANGE. Para la eliminación de dispositivos, la aplicación responde a eventos [**EC \_ DEVICE \_ LOST**](ec-device-lost.md) desde el administrador de gráficos de filtros. Cualquier enfoque funciona, aunque el evento EC \_ DEVICE LOST depende de la existencia del dispositivo en el gráfico de \_ filtros.

La aplicación solo controla un dispositivo a la vez. Si se quita el dispositivo actual, la aplicación busca otro dispositivo DV en el sistema.

En algunas cámaras DV, el usuario debe apagar el dispositivo al cambiarlo entre el modo de cámara y el modo VTR, lo que desencadena un mensaje perdido por el dispositivo. La aplicación responde habilitando o deshabilitando los comandos de menú adecuados. Sin embargo, si el usuario alterna rápidamente entre modos, es posible que la cámara de vídeo no genere un mensaje perdido por el dispositivo. Para forzar la actualización de los menús, elija **Modo de actualización** en el **menú** Opciones. Algunas cámaras de vídeo DV pueden alternar modos sin apagarse, pero enviar un mensaje perdido por el dispositivo solo cuando cambian al modo VTR.

### <a name="device-control"></a>Control de dispositivos

La funcionalidad del botón **Reproducir** **y grabar** depende del modo actual:

-   Versión preliminar: el gráfico de filtros se ejecuta automáticamente. El **botón Reproducir** inicia el transporte.
-   Capturar en archivo: el **botón Grabar** ejecuta el gráfico y el **botón Reproducir** inicia el transporte.
-   Transmitir al dispositivo: el **botón Reproducir** ejecuta el gráfico y el **botón Grabar** inicia el transporte.

La aplicación de ejemplo no realiza la captura precisa de fotogramas. En varios puntos, la aplicación llama a la **función Sleep** para esperar a que el dispositivo responda. Las cámaras dv más recientes envían una notificación cuando cambia el estado del dispositivo. Es posible que los dispositivos más antiguos no admitan notificaciones; Para los fines de un ejemplo, llamar a **Sleep** es una solución más sencilla.

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Para descargar los ejemplos DirectShow SDK, instale la versión más reciente del [SDK Windows SDK.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

Este ejemplo se instala en la siguiente ruta de acceso: *\[ SDK \] Root* Samples Multimedia DirectShow Capture \\ \\ \\ \\ \\ DVApp.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de una cámara dv](controlling-a-dv-camcorder.md)
</dt> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[DirectShow Muestras](directshow-samples.md)
</dt> </dl>

 

 



