---
description: Contiene el valor de mérito de un códec de hardware.
ms.assetid: 1df40a42-4c02-473f-a87f-2ae2d42e4f4e
title: MFT_CODEC_MERIT_Attribute atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74745244824bc766d0f7c1e691cb5f176d1da6a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659834"
---
# <a name="mft_codec_merit_attribute-attribute"></a>\_Atributo de \_ mérito del códec de MFT \_

Contiene el valor de mérito de un códec de hardware.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

Este atributo se establece en el objeto de activación de una transformación de Media Foundation (MFT) que representa un códec de hardware. El valor del atributo es el valor de mérito del códec.

Este atributo controla el orden en el que la función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) enumera los códecs, si se establece la marca SORTANDFILTER de la **\_ \_ marca \_ de enumeración MFT** . MFTs con un valor de mérito aparecen en la lista más arriba que en otras MFTs.

Este atributo no contiene un valor de confianza. Para comprobar el valor de mérito real del códec, llame a la función [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) .

Si el valor del \_ atributo mérito del códec MFT \_ \_ no coincide con el valor de mérito recuperado [**por MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit), se produce un error en el método [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) y se devuelve el mérito de un **\_ \_ \_ códec \_ no válido**.

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

[Atributos de transformación](transform-attributes.md)
</dt> </dl>

 

 




