---
description: El filtro del codificador AC-3 de Microsoft codifica el audio PCM estéreo en un fragmentada Dolby digital.
ms.assetid: 59d46ee2-d45f-4492-938d-39c55a7368e1
title: Codificador AC-3 de Microsoft (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 160b020e07bb3ba4e4dc5636b58dd0e66f581a6f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152335"
---
# <a name="microsoft-ac-3-encoder"></a>Codificador AC-3 de Microsoft

El filtro del codificador AC-3 de Microsoft codifica el audio PCM estéreo en un fragmentada Dolby digital.

> [!Note]  
> La implementación de Microsoft de la tecnología Dolby Digital está restringida en términos del programa de licencias Dolby digital que usarán las aplicaciones de Microsoft.

 

> [!Note]  
> Este filtro no se admite en las plataformas basadas en IA-64.

 



Información de filtro

Interfaces de filtro

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/>

Tipos de medios de anclaje de entrada

**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ PCM**<br/> El tipo de entrada debe ser estéreo de 48 kHz, 16 bits por muestra.<br/>

Interfaces de PIN de entrada

[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Tipos de medios de anclaje de salida

**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ Dolby \_ AC3**<br/> **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ Dolby \_ AC3**<br/>

Interfaces de clavija de salida

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Identificador CLSID

**CLSID \_ de CMSAC3Enc** (declarado en wmcodecdsp. h)

Executable

msac3enc.dll

[Fundament](merit.md)

**MÉRITO \_ \_ no se \_ usa**

[Categoría de filtro](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

## <a name="remarks"></a>Observaciones

Este filtro no está disponible para aplicaciones de terceros.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ solo aplicaciones de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 




