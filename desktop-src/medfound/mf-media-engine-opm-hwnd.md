---
description: Especifica una ventana para que el motor de medios aplique protecciones del Administrador de protección de salida (OPM).
ms.assetid: E5271D72-FE16-4D28-9BBA-1440C7CE0921
title: MF_MEDIA_ENGINE_OPM_HWND atributo (Mfmediaengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d60dd38f4f9eaca3e4eefbf84142c1509463f9b9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474188"
---
# <a name="mf_media_engine_opm_hwnd-attribute"></a>Atributo \_ \_ \_ HWND OPM \_ de MF MEDIA ENGINE

Especifica una ventana para que el motor de medios [aplique](output-protection-manager.md) protecciones del Administrador de protección de salida (OPM).

## <a name="data-type"></a>Tipo de datos

**HWND almacenado** como **UINT64**

## <a name="remarks"></a>Observaciones

Este atributo se usa con el [**método IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) para inicializar el motor multimedia.

Para habilitar las protecciones de OPM para la reproducción de vídeo, la aplicación debe realizar una de las siguientes acciones:

-   Establezca el [atributo MF MEDIA ENGINE PLAYBACK \_ \_ \_ \_ HWND](mf-media-engine-playback-hwnd.md) al crear el motor multimedia.
-   Establezca el atributo MF \_ MEDIA \_ ENGINE \_ OPM \_ HWND al crear el motor multimedia.
-   Llame [**a IMFMediaEngineProtectedContent::SetOPMWindow**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setopmwindow) en cualquier momento después de crear el motor multimedia, pero antes de que se muestre el contenido protegido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                          |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Mfmediaengine.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos del motor multimedia](media-engine-attributes.md)
</dt> </dl>

 

 




