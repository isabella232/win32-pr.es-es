---
description: Contiene un puntero a la interfaz IMFMediaEngineExtension.
ms.assetid: D2F3F41D-086A-4DEB-99D0-07574BC8F0D7
title: MF_MEDIA_ENGINE_EXTENSION atributo (Mfmediaengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4496b40e9b69091b588ad38ad47d943dce5e1966
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360704"
---
# <a name="mf_media_engine_extension-attribute"></a>Atributo MF \_ MEDIA \_ ENGINE \_ EXTENSION

Contiene un puntero a la [**interfaz IMFMediaEngineExtension.**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension)

## <a name="data-type"></a>Tipo de datos

**IMFMediaEngineExtension \* *_ almacenado como _* IUnknown\***

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Para establecer este atributo, llame [**a IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Observaciones

Este atributo se usa con el [**método IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) para inicializar el motor multimedia.

Este atributo es opcional. Úselo para proporcionar un objeto que implemente la [**interfaz IMFMediaEngineExtension.**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) Esta interfaz permite a la aplicación cargar recursos multimedia personalizados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                          |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Mfmediaengine.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




