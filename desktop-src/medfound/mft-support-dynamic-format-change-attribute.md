---
description: Especifica si una transformación de Media Foundation (MFT) admite cambios de formato dinámico.
ms.assetid: 64d32c78-8bee-4d3c-a770-5a097cb71b13
title: MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8224e9b7f0f05f430afac464e61900c7ce879fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706125"
---
# <a name="mft_support_dynamic_format_change-attribute"></a>El \_ \_ atributo de \_ cambio de formato dinámico \_ de MFT es compatible

Especifica si una transformación de Media Foundation (MFT) admite cambios de formato dinámico.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Trata como un valor booleano.

## <a name="remarks"></a>Observaciones

Este atributo puede tener los valores siguientes.



| Value     | Descripción                                                            |
|-----------|------------------------------------------------------------------------|
| **TRUE**  | El cliente puede cambiar el formato de entrada durante el streaming.               |
| **FALSE** | La MFT se debe purgar antes de que el cliente pueda cambiar el formato de entrada. |



 

Para obtener este atributo, primero llame a [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para obtener el almacén de atributos global para MFT. Después, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) para obtener el valor del atributo.

Si se produce un error en [**GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) o el atributo no está presente, el valor predeterminado es **false**.

Los [MFTs asincrónicos](asynchronous-mfts.md) deben devolver el valor **true**.

Para obtener más información, consulte [control de los cambios de flujo](handling-stream-changes.md).

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]<br/>                              |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFTs asincrónico](asynchronous-mfts.md)
</dt> <dt>

[Atributos de transformación](transform-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> </dl>

 

 




