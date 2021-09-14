---
description: Obtiene la dirección URL efectiva de una secuencia de bytes.
ms.assetid: 0A83CFC0-7EAA-464B-BA39-50DF220AF683
title: MF_BYTESTREAM_EFFECTIVE_URL atributo (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95e01238f04c30f72d55f940b3f3105863247ed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127364107"
---
# <a name="mf_bytestream_effective_url-attribute"></a>Atributo \_ MF BYTESTREAM \_ EFFECTIVE \_ URL

Obtiene la dirección URL efectiva de una secuencia de bytes.

## <a name="data-type"></a>Tipo de datos

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="applies-to"></a>Se aplica a

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)

## <a name="remarks"></a>Observaciones

La dirección URL efectiva puede diferir de la dirección URL original si la dirección URL original contiene información adicional, como cadenas de búsqueda o delimitadores, o si se redirija la solicitud.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                      |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Mfobjects.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de flujo de bytes](byte-stream-attributes.md)
</dt> <dt>

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




