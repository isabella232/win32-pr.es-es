---
description: Agregar un origen
ms.assetid: 8c5d1050-a696-4a5d-be68-806420d0cd78
title: Agregar un origen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab2440ff50bbb4a3a610f9341405538a88dc6bf16ce2153a327f3b4578f3aec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690535"
---
# <a name="adding-a-source"></a>Agregar un origen

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Cree un objeto de origen de la misma manera que crea otros objetos de escala de tiempo. Sin embargo, antes de insertarlo en la escala de tiempo, debe especificar al menos las siguientes propiedades en el origen.

-   Las horas de inicio y de detenerse, en relación con la escala de tiempo. Llame al [**método IAMTimelineObj::SetStartStop.**](iamtimelineobj-setstartstop.md)
-   Archivo multimedia que se usará como origen. Llame al [**método IAMTimelineSrc::SetMediaName**](iamtimelinesrc-setmedianame.md) con una cadena de caracteres anchos que represente el nombre del archivo.
-   Las horas de inicio y de detenerse del medio, que son relativas al archivo original. Llame al [**método IAMTimelineSrc::SetMediaTimes.**](iamtimelinesrc-setmediatimes.md) Para obtener más información sobre los tiempos multimedia, vea [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).

En el ejemplo siguiente, el clip de origen se inicia cuatro segundos en el archivo. La duración del medio es de 10 segundos, el doble de la duración de la escala de tiempo, lo que significa que el origen se reproducirá al doble de velocidad normal. La constante UNITS se define como 10000000 (10^7) y es igual a un segundo.


```C++
pSourceObj->SetStartStop(0, 50000000)
BSTR bstrFile = SysAllocStringLen(OLESTR("C:\\example.avi"), 15);
pSource->SetMediaName(bstrFile); 
SysFreeString(bstrFile);
pSource->SetMediaTimes(40000000, 140000000);
```



> [!Note]  
> Actualmente, DES no puede representar simultáneamente más de 75 orígenes comprimidos con códecs del Administrador de compresión de vídeo (VCM). Además, si el proyecto en su conjunto contiene más de 75 orígenes de este tipo, debe usar la reconexión dinámica o DES no puede obtener una vista previa del proyecto. Para obtener más información, [**vea IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).

 

Para obtener más información sobre los orígenes, vea [Trabajar con orígenes.](working-with-sources.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Construir una escala de tiempo](constructing-a-timeline.md)
</dt> </dl>

 

 



