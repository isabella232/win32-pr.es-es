---
description: Contiene una lista de los lenguajes RFC 1766 usados en la presentación actual.
ms.assetid: 8853bd88-d51a-478c-8c78-cf69a260e295
title: MF_PD_ASF_LANGLIST_LEGACYORDER atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f24abc714a7605800faa8ad66f8c0b888fba6f79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687969"
---
# <a name="mf_pd_asf_langlist_legacyorder-attribute"></a>MF \_ PD \_ ASF \_ LANGLIST \_ LEGACYORDER atributo

Contiene una lista de los lenguajes RFC 1766 usados en la presentación actual.

## <a name="data-type"></a>Tipo de datos

**BYTES \[\]**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Para establecer este atributo, llame a [**IMFAttributes:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="applies-to"></a>Se aplica a

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>Observaciones

Este atributo se aplica a los descriptores de presentación que se generaron a partir del [objeto ContentInfo ASF](asf-contentinfo-object.md) mediante una llamada a [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor). El formato de la matriz de bytes es el siguiente:



| Campo de objeto de lista de idiomas | Tipo de datos    | Tamaño    | Descripción                            |
|----------------------------|--------------|---------|----------------------------------------|
| Recuento de registros de ID. de idioma  | **DWORD**    | 4 bytes | Número de idiomas                    |
| Registros de ID. de idioma        | **BYTES**\[\] | Varía  | Matriz de cadenas de lenguaje (vea más abajo). |



 

El primer **valor DWORD** es el número de idiomas seguido de una matriz de cadenas de identificador de idioma. Cada cadena tiene el formato siguiente:



| Campo de objeto de lista de idiomas | Tipo de datos     | Tamaño    | Descripción                                                                               |
|----------------------------|---------------|---------|-------------------------------------------------------------------------------------------|
| Longitud del identificador de idioma         | **DWORD**     | 4 bytes | Longitud de la cadena en bytes, incluido el tamaño del carácter **nulo** final. |
| Id. de idioma                | **WCHAR**\[\] | Varía  | Una cadena terminada en null que contiene el nombre del idioma RFC 1766.                           |



 

Cada cadena es una etiqueta de lenguaje compatible con RFC 1766.

Utilice este atributo solo para la compatibilidad con versiones anteriores con el orden de enumeración de la interfaz [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) en el SDK de Windows Media Format. Las cadenas de idioma se almacenan en un orden diferente en el atributo [**MF \_ PD \_ ASF \_ LANGLIST**](mf-pd-asf-langlist-attribute.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de descriptor de presentación](presentation-descriptor-attributes.md)
</dt> </dl>

 

 
