---
description: El filtro Microsoft AC-3 Encoder codifica el audio PCM estéreo en una secuencia de bits Dolby Digital.
ms.assetid: 59d46ee2-d45f-4492-938d-39c55a7368e1
title: Microsoft AC-3 Encoder (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 160b020e07bb3ba4e4dc5636b58dd0e66f581a6f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072160"
---
# <a name="microsoft-ac-3-encoder"></a>Codificador Ac-3 de Microsoft

El filtro Microsoft AC-3 Encoder codifica el audio PCM estéreo en una secuencia de bits Dolby Digital.

> [!Note]  
> La implementación de Microsoft de la tecnología Dolby Digital está restringida en términos del programa de licencias Dolby Digital para que las usen las aplicaciones de Microsoft.

 

> [!Note]  
> Este filtro no se admite en plataformas basadas en IA-64.

 



Filtrar información

Interfaces de filtro

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/>

Tipos de medios de pin de entrada

**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ PCM**<br/> El tipo de entrada debe ser estéreo de 48 kHz, 16 bits por muestra.<br/>

Interfaces de pin de entrada

[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Tipos de medios de pin de salida

**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ DOLBY \_ AC3**<br/> **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ DOLBY \_ AC3**<br/>

Interfaces de pin de salida

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Filtrar CLSID

**CLSID \_ CMSAC3Enc** (declarado en wmcodecdsp.h)

Executable

msac3enc.dll

[Mérito](merit.md)

**NO USE LA OPCIÓN DE \_ \_ NO \_ USAR.**

[Categoría de filtro](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

## <a name="remarks"></a>Observaciones

Este filtro no está disponible para su uso por parte de aplicaciones de terceros.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ desktop apps only\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 




