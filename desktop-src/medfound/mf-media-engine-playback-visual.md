---
description: Establece un visual DirectComposition de Microsoft como la región de reproducción del motor multimedia.
ms.assetid: C381D28E-B7A1-4A1A-9F8D-42A4ABB1C633
title: MF_MEDIA_ENGINE_PLAYBACK_VISUAL atributo (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e9c7366bd0fbf4bf36523cf7a68f2d6da70bc3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105649323"
---
# <a name="mf_media_engine_playback_visual-attribute"></a>\_ \_ \_ Atributo visual de reproducción del motor multimedia MF \_

Establece un visual DirectComposition de Microsoft como la región de reproducción del motor multimedia.

## <a name="data-type"></a>Tipo de datos

**IDCompositionVisual \* *_ se almacena como _* IUnknown\***

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Para establecer este atributo, llame a [**IMFAttributes:: setunknown (**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Observaciones

Para obtener más información sobre DirectComposition, vea [DirectComposition](../directcomp/directcomposition-portal.md) y [**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual).

Este atributo se usa con el método [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) para inicializar el motor multimedia.

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

 

 
