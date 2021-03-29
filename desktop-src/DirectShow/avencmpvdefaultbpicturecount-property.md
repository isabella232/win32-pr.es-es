---
description: Especifica el número predeterminado de fotogramas B consecutivos entre los fotogramas I y P.
ms.assetid: d41ed713-0159-4325-bc44-f4a3eea10aa2
title: Propiedad AVEncMPVDefaultBPictureCount (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2026ddcb6a2b4ce813bd8ba2f6144f0c4a32344
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104080033"
---
# <a name="avencmpvdefaultbpicturecount-property"></a>Propiedad AVEncMPVDefaultBPictureCount

Especifica el número predeterminado de fotogramas B consecutivos entre los fotogramas I y P.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncMPVDefaultBPictureCount**

## <a name="property-value"></a>Valor de propiedad

Esta propiedad tiene un intervalo de valores lineal. Para obtener el intervalo admitido, llame a [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Observaciones

Antes de Windows 8, esta propiedad se aplica a los codificadores de vídeo MPEG. A partir de Windows 8, esta propiedad la usan los codificadores de vídeo MPEG, WMV y H. 264.

Si el codificador admite esta propiedad, se puede usar para controlar la estructura del grupo de imágenes (GOP).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]<br/>                     |
| Servidor mínimo compatible<br/> | Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**Interfaz ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




