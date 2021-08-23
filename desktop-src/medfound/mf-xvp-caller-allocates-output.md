---
description: Especifica si el autor de la llamada asignará las texturas usadas para la salida.
ms.assetid: CAB41B22-AD96-4932-9686-66474CB26C38
title: MF_XVP_CALLER_ALLOCATES_OUTPUT atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31da89bec9c9573d9d968077e51d413e1861bca28cb606667d402fab5a408f96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119599975"
---
# <a name="mf_xvp_caller_allocates_output-attribute"></a>MF \_ XVP \_ CALLER \_ ALLOCATES OUTPUT \_ attribute

Especifica si el autor de la llamada asignará las texturas usadas para la salida.

## <a name="data-type"></a>Tipo de datos

**BOOL almacenado** como **UINT32**

## <a name="remarks"></a>Comentarios

Si este atributo es **TRUE,** el procesador de vídeo espera que el autor de la llamada asigne texturas de salida, incluso cuando se opera en el modo de aceleración de vídeo directX (DXVA). Si este atributo es **FALSE,** el procesador de vídeo asignará las texturas de salida cuando se trabaja en modo DXVA y producirá un error si se proporcionan texturas de salida proporcionadas por el autor de la llamada.

Para establecer este atributo:

1.  Llame [**a IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) en el procesador de vídeo.
2.  Llame [**a IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

Establezca el atributo antes de que comience el streaming.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                          |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Mfidl.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




