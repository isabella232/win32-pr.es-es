---
description: 'Contiene la dirección URL del archivo IFO (información de DVD) especificado por el servidor HTTP en el encabezado HTTP, &\# 0034; Pragma: ifoFileURI.dlna.org&\# 0034;.'
ms.assetid: 007e0f4d-fb37-4dec-96a7-311df567eb04
title: MF_BYTESTREAM_IFO_FILE_URI atributo (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1c80e015b68272b073c442b4064c80a6787b811
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127364106"
---
# <a name="mf_bytestream_ifo_file_uri-attribute"></a>Atributo \_ DE URI DE ARCHIVO \_ IFO \_ DE \_ MF BYTESTREAM

Contiene la dirección URL del archivo IFO (información de DVD) especificado por el servidor HTTP en el encabezado HTTP, "Pragma: ifoFileURI.dlna.org".

## <a name="data-type"></a>Tipo de datos

**LPWSTR**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Para establecer este atributo, llame [**a IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="applies-to"></a>Se aplica a

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)

## <a name="remarks"></a>Observaciones

La secuencia de bytes HTTP busca la cadena "ifoFileURI.dlna.org" en el encabezado HTTP. Si se encuentra la cadena, se copia en este atributo en la secuencia de bytes.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/>                                                        |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                                           |
| Encabezado<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de flujo de bytes](byte-stream-attributes.md)
</dt> <dt>

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




