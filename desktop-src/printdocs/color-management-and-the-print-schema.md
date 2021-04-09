---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 296255b8-fe5c-46dd-b717-487aaae0db80
title: Administración del color y el esquema de impresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 134a598466fd52c66d632a28c750840d4123f529
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "103914270"
---
# <a name="color-management-and-the-print-schema"></a>Administración del color y el esquema de impresión

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Las palabras clave de elementos configurables por el usuario pueden ser específicas de XPS o no específicas del XPS. En el caso de que no sean específicos de XPS, la palabra clave se puede usar para la impresión basada en GDI heredada. Si una aplicación decide establecer estas palabras clave en un PrintTicket, depende del controlador determinar la acción y el comportamiento correctos que se deben tomar en función de las definiciones presentadas en el esquema de impresión. Cualquiera de estas palabras clave se puede usar en el contexto de ICM. Para obtener más información, consulte el SDK de Windows Vista.



| Print Schema User configurable (palabra clave)       | Equivalente en DEVMODE     | Específico de XPS   |
|----------------------------------------------|------------------------|----------------|
| PageColorManagement<br/>               | dmICMMethod<br/> | No<br/>  |
| PageBlackGenerationProcessing<br/>     | None<br/>        | Sí<br/> |
| PageBlendColorSpace<br/>               | None<br/>        | Sí<br/> |
| PageSourceColorProfile<br/>            | None<br/>        | No<br/>  |
| PageDestinationColorProfile<br/>       | None<br/>        | No<br/>  |
| PageICMRenderingIntent<br/>            | dmICMIntent<br/> | No<br/>  |
| JobOptimalDestinationColorProfile<br/> | None<br/>        | No<br/>  |
| PageDeviceColorSpaceUsage<br/>         | None<br/>        | Sí<br/> |



 

## <a name="pagecolormanagement-system-handling"></a>Control del sistema PageColorManagement

En el caso de PageColorManagement, el sistema proporciona el control automático de PrintTicket a DEVMODE o DEVMODE a la conversión de PrintTicket si es necesario. Esto depende de la ruta de impresión específica entre la aplicación (Win32 o WPF) y el controlador (basado en GDI o XPSDrv). En el caso de la impresión desde una aplicación Windows Presentation Foundation a un controlador de impresión XPSDrv de Microsoft, no se debe anunciar una opción pública de PageColorManagement del sistema en el documento PrintTicket o PrintCapabilities; en este caso, el sistema no puede controlar automáticamente la administración del color. La impresión desde una aplicación Win32 a un controlador de impresión de Microsoft XPSDrv puede dar lugar a la administración del color entre la aplicación y la GDI. sin embargo, después de la conversión a XPS-Format, no habrá ningún control automático del sistema de administración del color entre el documento XPS y el controlador o dispositivo, porque el formato XPS etiqueta cada elemento con información de color completa y depende del controlador o del dispositivo para procesar esta información.



| Opciones públicas de PageColorManagement | Valor DEVMODE                  |
|------------------------------------|--------------------------------|
| None<br/>                    | DMICMMETHOD \_ ninguno<br/>   |
| Dispositivo<br/>                  | \_dispositivo DMICMMETHOD<br/> |
| Controlador<br/>                  | \_controlador DMICMMETHOD<br/> |
| System<br/>                  | \_sistema DMICMMETHOD<br/> |



 

## <a name="pageicmrenderingintent-system-handling"></a>Control del sistema PageICMRenderingIntent

En el caso de PageICMRenderingIntent, el sistema proporciona el control automático de PrintTicket a DEVMODE o DEVMODE a la conversión de PrintTicket si es necesario. Esto depende de la ruta de impresión específica entre la aplicación (Win32 o Windows Presentation Foundation) y el controlador (basado en GDI o XPSDrv).



| Opciones públicas de PageICMRenderingIntent | Valor DEVMODE                       |
|---------------------------------------|-------------------------------------|
| AbsoluteColorimetric<br/>       | DMICM \_ ABS \_ colorimétrica<br/> |
| RelativeColorimetric<br/>       | DMICM \_ colorimétrica<br/>      |
| Fotografías<br/>                | \_contraste DMICM<br/>          |
| BusinessGraphics<br/>           | DMICM \_ saturado<br/>          |



 

Todas las demás palabras clave relacionadas con la administración del color (además de PageColorManagement o PageICMRenderingIntent) no tienen este control automático.

## <a name="joboptimaldestinationcolorprofile-and-pagedestinationcolorprofile-usage"></a>Uso de JobOptimalDestinationColorProfile y PageDestinationColorProfile

Una aplicación puede decidir consultar el documento de PrintCapabilities para JobOptimalDestinationColorProfile. Esto podría dar a una aplicación el perfil de color óptimo según la configuración actual del dispositivo, tal como se define en el documento de PrintCapabilities. Si la aplicación decide que quiere que el controlador realice la administración del color en el perfil de color de destino especificado por JobOptimalDestinationColorProfile, PageColorManagement y PageDestinationColorProfile se establecerán en driver y DriverConfiguration en PrintTicket, respectivamente. Si la aplicación no quiere usar el JobOptionalDestinationColorProfile y elige usar el suyo propio, debe establecer PageColorManagement en None y también establecer PageDestinationColorProfile en Application en PrintTicket para indicar que la aplicación ya ha realizado la administración del color en su perfil de color de destino especificado. Se puede producir otro escenario cuando la aplicación elige usar el perfil de color de destino óptimo devuelto por la PrintCapabilities de los controladores, pero decide hacer la administración del color por sí misma. En este caso, PageColorManagement se establecería en None y PageDestinationColorProfile se establecería en Application.

## <a name="pagesourcecolorprofile-usage"></a>Uso de PageSourceColorProfile

En el caso de PageSourceColorProfile, una aplicación puede especificar un perfil de color de origen para cada página del PrintTicket, independientemente de la opción seleccionada para PageColorManagement. Tanto si está presente como si no, depende del controlador decidir el comportamiento de cada caso en función de las definiciones presentadas en el esquema de impresión. Por ejemplo, una aplicación puede establecer PageColorManagement en None y, después, no establecer PageSourceColorProfile en PrintTicket. También es posible que una aplicación establezca PageColorManagement en controlador y, a continuación, establezca PageSourceColorProfile en PrintTicket; en este caso, el controlador es responsable de determinar el comportamiento dentro de las instrucciones de PrintSchema.

## <a name="pagedevicecolorspaceusage"></a>PageDeviceColorSpaceUsage

PageDeviceColorSpaceUsage es un elemento configurable por el usuario específico de XPS establecido por la aplicación. Proporciona instrucciones para el dispositivo mediante el establecimiento de la opción adecuada en el PrintTicket, para el control del perfil de espacio de color asociado a un documento XPS. La aplicación o el PrintTicket existente pueden especificar esta palabra clave en un PrintTicket que se envía al dispositivo. Tanto si está presente como si no, depende del controlador decidir el comportamiento de cada caso, en función de las definiciones presentadas en el esquema de impresión.

## <a name="print-schema-color-management-example-flow"></a>Flujo de ejemplo de administración del color de impresión

En el diagrama siguiente se ilustra el flujo de los escenarios más probables para usar la administración del color y el esquema de impresión. Para simplificar y mejorar la legibilidad, solo se usaron las siguientes palabras clave de esquema de impresión configurables por el usuario para mostrar su uso: PageColorManagement, JobOptimalDestinaionColorProfile, PageSourceColorProfile y PageDestinationColorProfile. Una línea sólida representa una acción que debe producirse y una línea discontinua representa una acción que se puede producir. El siguiente escenario no es la interacción garantizada que resultará entre la aplicación, el controlador y el sistema; sin embargo, representa el caso de uso más común que se producirá.

![diagrama que muestra cómo se procesa la configuración de la administración del color](images/local-1992284846-colormanagementtest3.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




