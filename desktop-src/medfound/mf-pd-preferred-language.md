---
description: Contiene el idioma RFC 1766 preferido del origen multimedia.
ms.assetid: 30f99804-6aea-473b-9bbf-e8c715501391
title: MF_PD_PREFERRED_LANGUAGE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81bb121c7181724ef06b3e8fe9239342a140104a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279048"
---
# <a name="mf_pd_preferred_language-attribute"></a>MF \_ PD \_ \_ atributo de idioma preferido

Contiene el idioma RFC 1766 preferido del origen multimedia.

## <a name="data-type"></a>Tipo de datos

**WCHAR**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Para establecer este atributo, llame a [**IMFAttributes:: Settring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="applies-to"></a>Se aplica a

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>Observaciones

El \_ atributo de \_ idioma preferido MF PD \_ es opcional. Una aplicación puede establecer este atributo en un origen de medios (como un origen de red) para especificar su idioma preferido.

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]<br/>                     |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de descriptor de presentación](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




