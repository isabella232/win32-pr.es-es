---
description: Especifica si el llamador asignará las texturas utilizadas para la salida.
ms.assetid: CAB41B22-AD96-4932-9686-66474CB26C38
title: MF_XVP_CALLER_ALLOCATES_OUTPUT atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: def1b1d138c031393e1a1b1a3832c1ad6d066306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543219"
---
# <a name="mf_xvp_caller_allocates_output-attribute"></a>El \_ autor de la llamada MF XVP \_ asigna el atributo de \_ \_ salida

Especifica si el llamador asignará las texturas utilizadas para la salida.

## <a name="data-type"></a>Tipo de datos

**Bool** almacenado como **UINT32**

## <a name="remarks"></a>Observaciones

Si este atributo es **true**, el procesador de vídeo espera que el autor de la llamada asigne las texturas de salida, incluso cuando se trabaja en modo de aceleración de vídeo de DirectX (DXVA). Si este atributo es **false**, el procesador de vídeo asignará las texturas de salida al operar en modo DXVA y se producirá un error si se proporcionan las texturas de salida proporcionadas por el autor de la llamada.

Para establecer este atributo:

1.  Llame a [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) en el procesador de vídeo.
2.  Llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

Establezca el atributo antes de que comience la transmisión por secuencias.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Mfidl. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




