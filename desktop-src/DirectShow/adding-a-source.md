---
description: Agregar un origen
ms.assetid: 8c5d1050-a696-4a5d-be68-806420d0cd78
title: Agregar un origen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee583cd8971c183f2e03b92f68e2d6ba555c41db
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105659295"
---
# <a name="adding-a-source"></a>Agregar un origen

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Cree un objeto de origen de la misma manera que crea otros objetos Timeline. Sin embargo, antes de insertarlo en la escala de tiempo, debe especificar al menos las siguientes propiedades en el origen.

-   Horas de inicio y detención, con respecto a la escala de tiempo. Llame al método [**IAMTimelineObj:: SetStartStop**](iamtimelineobj-setstartstop.md) .
-   Archivo multimedia que se va a utilizar como origen. Llame al método [**IAMTimelineSrc:: SetMediaName**](iamtimelinesrc-setmedianame.md) con una cadena de caracteres anchos que represente el nombre del archivo.
-   Horas de inicio y detención del medio, que son relativas al archivo original. Llame al método [**IAMTimelineSrc:: SetMediaTimes**](iamtimelinesrc-setmediatimes.md) . Para obtener más información sobre las horas de los medios, consulte [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).

En el ejemplo siguiente, el clip de origen inicia cuatro segundos en el archivo. La duración del medio es de 10 segundos, dos veces la longitud de la duración de la escala de tiempo, lo que significa que el origen se reproducirá a la doble velocidad normal. Las unidades constantes se definen como 10 millones (10 ^ 7) y es igual a un segundo.


```C++
pSourceObj->SetStartStop(0, 50000000)
BSTR bstrFile = SysAllocStringLen(OLESTR("C:\\example.avi"), 15);
pSource->SetMediaName(bstrFile); 
SysFreeString(bstrFile);
pSource->SetMediaTimes(40000000, 140000000);
```



> [!Note]  
> Actualmente, DES no puede representar simultáneamente más de 75 orígenes que se comprimieron con códecs de administrador de compresión de vídeo (VCM). Además, si el proyecto como un conjunto contiene más de 75 tales orígenes, debe usar reconexión dinámica o DES no puede obtener una vista previa del proyecto. Para obtener más información, vea [**IRenderEngine:: SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).

 

Para obtener más información sobre los orígenes, vea [trabajar con orígenes](working-with-sources.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Construir una escala de tiempo](constructing-a-timeline.md)
</dt> </dl>

 

 



