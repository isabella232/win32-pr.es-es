---
description: Especifica si una transformación Media Foundation (MFT) admite cambios de formato dinámicos.
ms.assetid: 64d32c78-8bee-4d3c-a770-5a097cb71b13
title: MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8224e9b7f0f05f430afac464e61900c7ce879fd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363746"
---
# <a name="mft_support_dynamic_format_change-attribute"></a>Atributo DYNAMIC \_ \_ FORMAT \_ \_ CHANGE de MFT SUPPORT

Especifica si una transformación Media Foundation (MFT) admite cambios de formato dinámicos.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Tratar como un valor booleano.

## <a name="remarks"></a>Observaciones

Este atributo puede tener los siguientes valores.



| Value     | Descripción                                                            |
|-----------|------------------------------------------------------------------------|
| **TRUE**  | El cliente puede cambiar el formato de entrada durante el streaming.               |
| **FALSE** | El MFT debe purgarse para que el cliente pueda cambiar el formato de entrada. |



 

Para obtener este atributo, primero llame [**a ALTRANSFORMTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para obtener el almacén de atributos global para el MFT. A [**continuación, llame aATTRIBUTEAttributes::GetUINT32 para**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) obtener el valor del atributo.

Si Se produce un error en [**GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) o el atributo no está presente, el valor predeterminado es **FALSE.**

[Las MTA asincrónicas](asynchronous-mfts.md) deben devolver el **valor TRUE.**

Para obtener más información, vea [Control de cambios de flujo.](handling-stream-changes.md)

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                              |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| aplicaciones para UWP\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFT asincrónicas](asynchronous-mfts.md)
</dt> <dt>

[Transformar atributos](transform-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> </dl>

 

 




