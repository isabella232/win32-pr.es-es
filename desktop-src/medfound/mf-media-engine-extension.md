---
description: Contiene un puntero a la interfaz IMFMediaEngineExtension.
ms.assetid: D2F3F41D-086A-4DEB-99D0-07574BC8F0D7
title: MF_MEDIA_ENGINE_EXTENSION atributo (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4496b40e9b69091b588ad38ad47d943dce5e1966
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104424131"
---
# <a name="mf_media_engine_extension-attribute"></a>MF \_ \_ atributo de extensión de motor multimedia \_

Contiene un puntero a la interfaz [**IMFMediaEngineExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) .

## <a name="data-type"></a>Tipo de datos

**IMFMediaEngineExtension \* *_ se almacena como _* IUnknown\***

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Para establecer este atributo, llame a [**IMFAttributes:: setunknown (**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Observaciones

Este atributo se usa con el método [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) para inicializar el motor multimedia.

Este atributo es opcional. Úselo para proporcionar un objeto que implemente la interfaz [**IMFMediaEngineExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) . Esta interfaz permite a la aplicación cargar recursos multimedia personalizados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                          |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Mfmediaengine. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




