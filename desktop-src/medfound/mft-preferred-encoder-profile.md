---
description: Contiene las propiedades de configuración de un codificador.
ms.assetid: f9bd8a50-e43e-4668-86a0-c9d5f517f4cf
title: MFT_PREFERRED_ENCODER_PROFILE atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfdc85ead0fe813215b3edaea14833400df5445d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001452"
---
# <a name="mft_preferred_encoder_profile-attribute"></a>\_Atributo de \_ Perfil de codificador preferido de MFT \_

Contiene las propiedades de configuración de un codificador.

## <a name="data-type"></a>Tipo de datos

**[](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) IMFAttributes \** _ almacenado como _*IUnknown \**_

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [_ *IMFAttributes:: GetUnknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Para establecer este atributo, llame a [**IMFAttributes:: setunknown (**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="applies-to"></a>Se aplica a

[**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)

## <a name="remarks"></a>Observaciones

Este atributo se puede establecer en el objeto de activación devuelto por la función [**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) . El atributo solo se aplica cuando el objeto de activación está configurado para crear un codificador. El valor del atributo es un puntero a un almacén de atributos, que a su vez contiene las propiedades que se van a establecer en el codificador.

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

[**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> <dt>

[Atributos de transformación](transform-attributes.md)
</dt> </dl>

 

 




