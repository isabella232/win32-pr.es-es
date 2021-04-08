---
description: Especifica una ventana para que el motor multimedia aplique protecciones de administrador de protección de la información (OPM).
ms.assetid: E5271D72-FE16-4D28-9BBA-1440C7CE0921
title: MF_MEDIA_ENGINE_OPM_HWND atributo (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d60dd38f4f9eaca3e4eefbf84142c1509463f9b9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003343"
---
# <a name="mf_media_engine_opm_hwnd-attribute"></a>\_ \_ \_ \_ Atributo HWND de el motor de multimedia MF

Especifica una ventana para que el motor multimedia aplique protecciones de [Administrador de protección](output-protection-manager.md) de la información (OPM).

## <a name="data-type"></a>Tipo de datos

**HWnd** almacenado como **UINT64**

## <a name="remarks"></a>Observaciones

Este atributo se usa con el método [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) para inicializar el motor multimedia.

Para habilitar la protección de OPM para la reproducción de vídeo, la aplicación debe realizar una de las siguientes acciones:

-   Establezca el [atributo \_ \_ hWnd de \_ reproducción \_ del motor multimedia MF](mf-media-engine-playback-hwnd.md) al crear el motor multimedia.
-   Establezca el atributo del HWND del motor de multimedia de MF \_ \_ \_ \_ al crear el motor multimedia.
-   Llame a [**IMFMediaEngineProtectedContent:: SetOPMWindow**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setopmwindow) en cualquier momento después de crear el motor multimedia, pero antes de que se muestre el contenido protegido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                          |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Mfmediaengine. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos del motor multimedia](media-engine-attributes.md)
</dt> </dl>

 

 




