---
description: Contiene un puntero DE TIPO IMFFieldOfUseMFTUnlock, que se puede usar para desbloquear una Media Foundation transformación (MFT). La interfaz IMFFieldOfUseMFTUnlock se usa para desbloquear un MFT que tiene restricciones de campo de uso.
ms.assetid: 7f48967e-375a-4019-b14f-2f457b616cc0
title: MFT_FIELDOFUSE_UNLOCK_Attribute atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476ae7ffdc6de506b4dbc2f49ec7a6b19b01affafd53f0c9495f9f5c396c5caf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973074"
---
# <a name="mft_fieldofuse_unlock_attribute-attribute"></a>Atributo \_ MFT FIELDOFUSE \_ UNLOCK \_

Contiene un [**puntero DE TIPO IMFFieldOfUseMFTUnlock,**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) que se puede usar para desbloquear una Media Foundation transformación (MFT). La **interfaz IMFFieldOfUseMFTUnlock** se usa para desbloquear un MFT que tiene restricciones de campo de uso.

## <a name="data-type"></a>Tipo de datos

**[**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) \* *_ almacenado como _* Iunknown\***

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Comentarios

Para obtener más información sobre este atributo, vea [Restricciones de campo de uso.](field-of-use-restrictions.md)

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio aplicaciones para \| UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Restricciones de campo de uso](field-of-use-restrictions.md)
</dt> <dt>

[**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> </dl>

 

 




