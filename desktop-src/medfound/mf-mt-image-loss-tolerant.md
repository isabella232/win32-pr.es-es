---
description: Especifica si una secuencia de imágenes ASF es un tipo JPEG degradado.
ms.assetid: e29d0893-8561-4a8c-99e2-168186becd82
title: MF_MT_IMAGE_LOSS_TOLERANT atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eea33f9f5f49725d164bd26ba21b9602bffef2b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908039"
---
# <a name="mf_mt_image_loss_tolerant-attribute"></a>MF \_ MT \_ Image \_ loss \_ tolerante (atributo)

Especifica si una secuencia de imágenes ASF es un tipo JPEG degradado.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Observaciones

Este atributo se aplica al tipo de medio para flujos de imagen en ASF. Si el valor es **true**, la secuencia es un tipo de imagen JPEG degradado. De lo contrario, el flujo es un tipo de imagen JFIF. Para obtener más información sobre estos tipos de secuencias, vea la especificación ASF.

Además del \_ atributo MF MT \_ Image \_ loss \_ tolerante, el tipo de medio para un flujo de imagen ASF contiene los siguientes atributos:



| Atributo                                                 | Descripción                                |
|-----------------------------------------------------------|--------------------------------------------|
| [**\_ \_ tipo principal MF \_ MT**](mf-mt-major-type-attribute.md) | Contiene el valor **MFMediaType \_ imagen**. |
| [**\_tamaño de \_ marco MF MT \_**](mf-mt-frame-size-attribute.md) | Proporciona el tamaño de la imagen en píxeles.            |



 

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]<br/>                     |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> </dl>

 

 




