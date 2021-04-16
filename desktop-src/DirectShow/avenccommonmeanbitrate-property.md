---
description: Especifica la velocidad media de bits codificada, en bits por segundo. Esta propiedad solo se aplica a los modos de codificación de velocidad de bits constante (CBR) y de velocidad de bits variable (VBR).
ms.assetid: 8519685a-4f5b-44af-ad46-09eba7a198c6
title: Propiedad AVEncCommonMeanBitRate (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4eaec7fc6578e6e69a45616ee6de059bb7a378b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538007"
---
# <a name="avenccommonmeanbitrate-property"></a>Propiedad AVEncCommonMeanBitRate

Especifica la velocidad media de bits codificada, en bits por segundo. Esta propiedad solo se aplica a los modos de codificación de velocidad de bits constante (CBR) y de velocidad de bits variable (VBR).

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncCommonMeanBitRate**

## <a name="property-value"></a>Valor de propiedad

Los codificadores pueden implementar esta propiedad como un conjunto enumerado o como un intervalo lineal.

## <a name="remarks"></a>Observaciones

Esta propiedad también se usa con [codificadores de cámara H. 264 UVC 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).

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

 

