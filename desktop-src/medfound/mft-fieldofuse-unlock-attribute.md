---
description: Contiene un puntero IMFFieldOfUseMFTUnlock, que se puede usar para desbloquear una transformación de Media Foundation (MFT). La interfaz IMFFieldOfUseMFTUnlock se usa para desbloquear una MFT que tiene restricciones de campo de uso.
ms.assetid: 7f48967e-375a-4019-b14f-2f457b616cc0
title: MFT_FIELDOFUSE_UNLOCK_Attribute atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85f02fbc032f16406a2b4407b197dc6140774001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812602"
---
# <a name="mft_fieldofuse_unlock_attribute-attribute"></a>\_Atributo de \_ atributo Unlock FIELDOFUSE de MFT \_

Contiene un puntero [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , que se puede usar para desbloquear una transformación de Media Foundation (MFT). La interfaz **IMFFieldOfUseMFTUnlock** se usa para desbloquear una MFT que tiene restricciones de campo de uso.

## <a name="data-type"></a>Tipo de datos

**[](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) IMFFieldOfUseMFTUnlock \** _ almacenado como _*IUnknown \**_

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [_ *IMFAttributes:: GetUnknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Para establecer este atributo, llame a [**IMFAttributes:: setunknown (**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Observaciones

Para obtener más información sobre este atributo, vea el [campo de restricciones de uso](field-of-use-restrictions.md).

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Campo de restricciones de uso](field-of-use-restrictions.md)
</dt> <dt>

[**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> </dl>

 

 




