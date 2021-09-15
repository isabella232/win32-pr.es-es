---
description: Establece un objeto visual DirectComposition de Microsoft como región de reproducción del motor multimedia.
ms.assetid: C381D28E-B7A1-4A1A-9F8D-42A4ABB1C633
title: MF_MEDIA_ENGINE_PLAYBACK_VISUAL atributo (Mfmediaengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e9c7366bd0fbf4bf36523cf7a68f2d6da70bc3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474179"
---
# <a name="mf_media_engine_playback_visual-attribute"></a>Atributo \_ VISUAL DE REPRODUCCIÓN DE MF MEDIA \_ ENGINE \_ \_

Establece un objeto visual DirectComposition de Microsoft como región de reproducción del motor multimedia.

## <a name="data-type"></a>Tipo de datos

**IDCompositionVisual \* *_ almacenado como _* IUnknown\***

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Observaciones

Para obtener más información sobre DirectComposition, vea [DirectComposition](../directcomp/directcomposition-portal.md) e [**IDCompositionVisual.**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)

Este atributo se usa con el [**método IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) para inicializar el motor multimedia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                          |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Mfmediaengine.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
