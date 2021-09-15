---
description: Obtenga información sobre las palabras clave configurables por el usuario en El esquema de impresión para la administración de colores, como PageColorManagement y PageBlackGenerationProcessing.
ms.assetid: 296255b8-fe5c-46dd-b717-487aaae0db80
title: Administración de colores y el esquema de impresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9258d9dcc59ab24f9cfca8e170bf3f3f62841b21
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468541"
---
# <a name="color-management-and-the-print-schema"></a>Administración de colores y el esquema de impresión

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Las palabras clave del elemento configurable por el usuario pueden ser específicas de XPS o no específicas de XPS. En el caso de que no sean específicos de XPS, la palabra clave se puede usar para la impresión heredada basada en GDI. Si una aplicación decide establecer estas palabras clave en printTicket, es el controlador quien determina la acción y el comportamiento adecuados que se deben realizar en función de las definiciones presentadas en el esquema de impresión. Cualquiera de estas palabras clave se puede usar en el contexto de ICM. Para más información, consulte el SDK Windows Vista.



| Palabra clave configurable del usuario del esquema de impresión       | EQUIVALENTE DEVMODE     | Específico de XPS   |
|----------------------------------------------|------------------------|----------------|
| PageColorManagement<br/>               | dmICMMethod<br/> | No<br/>  |
| PageBlackGenerationProcessing<br/>     | None<br/>        | Sí<br/> |
| PageBlendColorSpace<br/>               | None<br/>        | Sí<br/> |
| PageSourceColorProfile<br/>            | Ninguno<br/>        | No<br/>  |
| PageDestinationColorProfile<br/>       | Ninguno<br/>        | No<br/>  |
| PageICMRenderingIntent<br/>            | dmICMIntent<br/> | No<br/>  |
| JobOptimalDestinationColorProfile<br/> | Ninguno<br/>        | No<br/>  |
| PageDeviceColorSpaceUsage<br/>         | None<br/>        | Sí<br/> |



 

## <a name="pagecolormanagement-system-handling"></a>Control del sistema PageColorManagement

Para PageColorManagement, el sistema proporciona el control automático de la conversión PrintTicket a DEVMODE o DEVMODE a PrintTicket si es necesario. Esto depende de la ruta de impresión específica entre la aplicación (Win32 o WPF) y el controlador (basado en GDI o XPSDrv). En el caso de imprimir desde una aplicación Windows Presentation Foundation a un controlador de impresión XPSDrv de Microsoft, una opción pública PageColorManagement de System NO DEBE anunciarse en el documento PrintTicket o PrintCapabilities. En este caso, el sistema no puede controlar automáticamente la administración de colores. La impresión desde una aplicación Win32 a un controlador de impresión XPSDrv de Microsoft puede dar lugar a la administración de colores entre la aplicación y GDI; sin embargo, después de la conversión al formato XPS, no habrá ningún control automático del sistema de administración de colores entre el documento XPS y el controlador o dispositivo, ya que el formato XPS etiqueta cada elemento con información de color completa y es el controlador o el dispositivo los que procesan esta información.



| Opciones públicas de PageColorManagement | Valor DEVMODE                  |
|------------------------------------|--------------------------------|
| None<br/>                    | DMICMMETHOD \_ NONE<br/>   |
| Dispositivo<br/>                  | DMICMMETHOD \_ DEVICE<br/> |
| Controlador<br/>                  | CONTROLADOR DMICMMETHOD \_<br/> |
| Sistema<br/>                  | DMICMMETHOD \_ SYSTEM<br/> |



 

## <a name="pageicmrenderingintent-system-handling"></a>PageICMRenderingIntent System Handling

Para PageICMRenderingIntent, el sistema proporciona el control automático de PrintTicket a DEVMODE o DEVMODE a la conversión PrintTicket si es necesario. Esto depende de la ruta de impresión específica entre la aplicación (Win32 o Windows Presentation Foundation) y el controlador (basado en GDI o XPSDrv).



| Opciones públicas de PageICMRenderingIntent | Valor DEVMODE                       |
|---------------------------------------|-------------------------------------|
| AbsoluteColorimetric<br/>       | \_COLORIMETRIC de ABS de DMICM \_<br/> |
| RelativeColorimetric<br/>       | COLORIMETRIC de DMICM \_<br/>      |
| Fotografías<br/>                | CONTRASTE DE DMICM \_<br/>          |
| BusinessGraphics<br/>           | SATURACIÓN DE DMICM \_<br/>          |



 

Todas las demás palabras clave relacionadas con administración de colores (además de PageColorManagement o PageICMRenderingIntent) no tienen este control automático.

## <a name="joboptimaldestinationcolorprofile-and-pagedestinationcolorprofile-usage"></a>Uso de JobOptimalDestinationColorProfile y PageDestinationColorProfile

Una aplicación PUEDE decidir consultar el documento PrintCapabilities para JobOptimalDestinationColorProfile. Esto podría proporcionar a una aplicación el perfil de color óptimo dada la configuración actual del dispositivo, tal como se define en el documento PrintCapabilities. Si la aplicación decide que desea que el controlador realice la administración de colores en el perfil de color de destino especificado por JobOptimalDestinationColorProfile, PageColorManagement y PageDestinationColorProfile se establecerán en Driver y DriverConfiguration en PrintTicket respectivamente. Si la aplicación no desea usar JobOptionalDestinationColorProfile y elige usar su propio elemento, DEBE establecer PageColorManagement en None y también establecer PageDestinationColorProfile en Application en PrintTicket para transmitir que la aplicación ya ha realizado la administración de colores a su perfil de color de destino especificado. Otro escenario puede producirse cuando la aplicación elige usar el perfil de color de destino óptimo devuelto por los controladores PrintCapabilities, pero decide realizar la administración de colores por sí misma. En este caso, PageColorManagement se establecería en None y PageDestinationColorProfile se establecería en Application.

## <a name="pagesourcecolorprofile-usage"></a>Uso de PageSourceColorProfile

Para PageSourceColorProfile, una aplicación PUEDE especificar un perfil de color de origen para cada página de PrintTicket, independientemente de la opción seleccionada para PageColorManagement. Tanto si está presente como si no, es el controlador quien decide el comportamiento de cada caso en función de las definiciones presentadas en el esquema de impresión. Por ejemplo, una aplicación puede establecer PageColorManagement en None y, a continuación, no establecer PageSourceColorProfile en PrintTicket. También es posible que una aplicación establezca PageColorManagement en Driver y, a continuación, establezca PageSourceColorProfile en PrintTicket; El controlador en este caso es responsable de determinar el comportamiento dentro de las directrices de PrintSchema.

## <a name="pagedevicecolorspaceusage"></a>PageDeviceColorSpaceUsage

PageDeviceColorSpaceUsage es un elemento específico configurable por el usuario XPS que establece la aplicación. Proporciona instrucciones para el dispositivo estableciendo la opción adecuada en PrintTicket para el control de perfiles de espacio de color asociado en un documento XPS. La aplicación o printTicket existente PUEDE especificar esta palabra clave en un PrintTicket enviado al dispositivo. Tanto si está presente como si no, es el controlador quien decide el comportamiento de cada caso, en función de las definiciones presentadas en el esquema de impresión.

## <a name="print-schema-color-management-example-flow"></a>Ejemplo de administración de colores del esquema de impresión Flow

En el diagrama siguiente se muestra el flujo de los escenarios más probables para usar administración de colores y el esquema de impresión. Para simplificar y mejorar la legibilidad, solo se usaron las siguientes palabras clave de esquema de impresión configurables por el usuario para demostrar su uso: PageColorManagement, JobOptimalDestinaionColorProfile, PageSourceColorProfile y PageDestinationColorProfile. Una línea sólida representa una acción que DEBERÍA producirse y una línea discontinua representa una acción que puede producirse. El escenario siguiente no es la interacción garantizada que se producirá entre la aplicación, el controlador y el sistema; sin embargo, representa el caso de uso más común que se producirá.

![un diagrama que muestra cómo se procesa la configuración de administración de colores](images/local-1992284846-colormanagementtest3.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




