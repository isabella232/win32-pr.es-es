---
description: Especifica si el IMFTransform desea recibir notificaciones de finalización de MEPolicySet.
title: MFT_POLICY_SET_AWARE (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2effa9eab2b0b126c2849d39ce7ffe3f62d81e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720486"
---
# <a name="mft_policy_set_aware-attribute"></a>\_ \_ Atributo consciente de conjunto de directivas de MFT \_

Si es distinto de cero, indica que **IMFTransform** desea recibir notificaciones de finalización de [MEPolicySet](./mepolicyset.md) .

## <a name="data-type"></a>Tipo de datos

**UINT32** (se trata como **bool**)

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFInputTrustAuthority**](/windows/win32/api/mfidl/nn-mfidl-imfinputtrustauthority)

## <a name="remarks"></a>Observaciones

Este atributo puede ser utilizado por un Decrypter **IMFInputTrustAuthority** . Una implementación de un módulo de descifrado de contenido (CDM) puede incluir una implementación de **IMFInputTrustAuthority**. Se tiene acceso al objeto **IMFInputTrustAuthority** a través de [IMFContentDecryptionModule:: CreateTrustedInput](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmodule-createtrustedinput).


La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Actualización 2020 de abril de Windows 10   <br/>                                        |
| Encabezado<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt>  <dt>

[Atributos de transformación](transform-attributes.md)
</dt> </dl>

 

 
