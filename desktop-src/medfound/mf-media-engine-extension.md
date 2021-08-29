---
description: Contiene un puntero a la interfaz IMFMediaEngineExtension.
ms.assetid: D2F3F41D-086A-4DEB-99D0-07574BC8F0D7
title: MF_MEDIA_ENGINE_EXTENSION atributo (Mfmediaengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bc008abf22541c724ae788620b9ea6ee3ea69c7620123c4234139b981951a06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118060547"
---
# <a name="mf_media_engine_extension-attribute"></a>Atributo MF \_ MEDIA \_ ENGINE \_ EXTENSION

Contiene un puntero a la [**interfaz IMFMediaEngineExtension.**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension)

## <a name="data-type"></a>Tipo de datos

**IMFMediaEngineExtension \* *_ almacenado como _* IUnknown\***

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Comentarios

Este atributo se usa con el [**método IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) para inicializar el motor multimedia.

Este atributo es opcional. Úsese para proporcionar un objeto que implemente la [**interfaz IMFMediaEngineExtension.**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) Esta interfaz permite a la aplicación cargar recursos multimedia personalizados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                          |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mfmediaengine.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




