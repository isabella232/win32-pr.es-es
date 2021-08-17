---
description: Contiene una lista de los idiomas RFC 1766 usados en la presentación actual.
ms.assetid: 8853bd88-d51a-478c-8c78-cf69a260e295
title: MF_PD_ASF_LANGLIST_LEGACYORDER atributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32693550ecbe48d14d6e26b9c509f3b90cfd1c327fd945583f1cdff729db7bc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102935"
---
# <a name="mf_pd_asf_langlist_legacyorder-attribute"></a>Atributo \_ \_ LEGACYORDER de ASF DE MF PD \_ LANGLIST \_

Contiene una lista de los idiomas RFC 1766 usados en la presentación actual.

## <a name="data-type"></a>Tipo de datos

**Byte \[\]**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="applies-to"></a>Se aplica a

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>Comentarios

Este atributo se aplica a los descriptores de presentación generados a partir del objeto ContentInfo de [ASF](asf-contentinfo-object.md) mediante una llamada a [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor). El formato de la matriz de bytes es el siguiente:



| Campo Objeto de lista de idioma | Tipo de datos    | Size    | Descripción                            |
|----------------------------|--------------|---------|----------------------------------------|
| Recuento de registros de identificador de idioma  | **DWORD**    | 4 bytes | Número de idiomas                    |
| Registros de identificador de idioma        | **Byte**\[\] | Varía  | Matriz de cadenas de lenguaje (consulte a continuación). |



 

El primer **DWORD es** el número de idiomas, seguido de una matriz de cadenas de identificador de idioma. Cada cadena tiene el formato siguiente:



| Campo Objeto de lista de idioma | Tipo de datos     | Size    | Descripción                                                                               |
|----------------------------|---------------|---------|-------------------------------------------------------------------------------------------|
| Longitud del identificador de idioma         | **DWORD**     | 4 bytes | Longitud de la cadena en bytes, incluido el tamaño del carácter **NULL** final. |
| Id. de idioma                | **Wchar**\[\] | Varía  | Cadena terminada en NULL que contiene el nombre de idioma RFC 1766.                           |



 

Cada cadena es una etiqueta de lenguaje compatible con RFC 1766.

Use este atributo solo por compatibilidad con versiones anteriores con el orden de enumeración de la interfaz [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) en el SDK Windows Media Format. Las cadenas de idioma se almacenan en un orden diferente en el atributo [**\_ \_ ASF \_ LANGLIST de MF PD.**](mf-pd-asf-langlist-attribute.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos del descriptor de presentación](presentation-descriptor-attributes.md)
</dt> </dl>

 

 
