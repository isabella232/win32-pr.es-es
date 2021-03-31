---
description: Establece el umbral en el que el codificador considera que un campo de vídeo es redundante.
ms.assetid: db6c2f0e-f451-4d2d-984f-b507083e8358
title: Propiedad AVEncVideoInverseTelecineThreshold (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3427a8ff1491277c2e36640560acf728c0ef7208
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805395"
---
# <a name="avencvideoinversetelecinethreshold-property"></a>Propiedad AVEncVideoInverseTelecineThreshold

Establece el umbral en el que el codificador considera que un campo de vídeo es redundante.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoInverseTelecineThreshold**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad tiene el siguiente intervalo.



| Value | Descripción                                                    |
|-------|----------------------------------------------------------------|
| 0     | Es menos probable que el codificador tenga en cuenta los campos de vídeo redundantes. |
| 100   | Es más probable que el codificador tenga en cuenta los campos de vídeo redundantes. |



 

## <a name="remarks"></a>Observaciones

Establezca esta propiedad si el codificador está realizando telecine inversa con un origen de vídeo analógico.

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

 

 




