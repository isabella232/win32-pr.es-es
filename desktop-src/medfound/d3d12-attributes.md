---
description: Atributos de Direct3D 12
title: Atributos de Direct3D 12
ms.topic: article
ms.date: 08/13/2021
ms.openlocfilehash: 646d2cea8923286714982a3e083eade65f664be7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572868"
---
# <a name="direct3d-12-attributes"></a>Atributos de Direct3D 12

Los atributos siguientes se pueden usar para configurar Direct3D 12 Media Foundation recursos.



| Atributo                                                                                                         | Descripción                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [MF_MT_D3D_RESOURCE_VERSION](mf-mt-d3d-resource-version.md) | Especifica la versión de Direct3D de los recursos almacenados en el flujo de datos asociado al tipo de medio. |
| [MF_MT_D3D12_CPU_READBACK](mf-mt-d3d12-cpu-readback.md) | Indica si se requiere acceso a la CPU para los recursos de Direct3D asociados. |
| [MF_MT_D3D12_RESOURCE_FLAG_ALLOW_CROSS_ADAPTER](mf-mt-d3d12-resource-flag-allow-cross-adapter.md) | Indica si los recursos de la secuencia se pueden usar para los datos entre adaptadores.  |
| [MF_MT_D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL](mf-mt-d3d12-resource-flag-allow-depth-stencil.md) | Indica si se puede crear la vista de galería de símbolos de profundidad para los recursos de Direct3D en la secuencia asociada al tipo de medio. |
| [MF_MT_D3D12_RESOURCE_FLAG_ALLOW_RENDER_TARGET](mf-mt-d3d12-resource-flag-allow-render-target.md) | Indica si se puede crear una vista de destino de representación para los recursos de Direct3D en la secuencia asociada al tipo de medio.  |
| [MF_MT_D3D12_RESOURCE_FLAG_ALLOW_SIMULTANEOUS_ACCESS](mf-mt-d3d12-resource-flag-allow-simultaneous-access.md) | Indica si varias colas de comandos diferentes pueden acceder simultáneamente a los recursos de Direct3D de la secuencia.  |
| [MF_MT_D3D12_RESOURCE_FLAG_ALLOW_UNORDERED_ACCESS](mf-mt-d3d12-resource-flag-allow-unordered-access.md) | Indica si se puede crear una vista de acceso desordenado para los recursos de Direct3D en la secuencia asociada al tipo de medio. |
| [MF_MT_D3D12_RESOURCE_FLAG_DENY_SHADER_RESOURCE](mf-mt-d3d12-resource-flag-deny-shader-resource.md) | Indica si no se puede crear la vista de recursos del sombreador para los recursos de Direct3D en la secuencia asociada al tipo de medio.  |
| [MF_MT_D3D12_TEXTURE_LAYOUT](mf-mt-d3d12-texture-layout.md) | Indica las opciones de diseño de textura que se usaron para crear los recursos de Direct3D asociados.  |
| [MF_SA_D3D12_CLEAR_VALUE](mf-sa-d3d12-clear-value.md) | Contiene un blob con la información que se usa para optimizar las operaciones claras para los recursos de Direct3D en la secuencia. |
| [MF_SA_D3D12_HEAP_FLAGS](mf-sa-d3d12-heap-flags.md) | Contiene un valor que especifica las opciones del montón usadas para los recursos de Direct3D en la secuencia. |
| [MF_SA_D3D12_HEAP_TYPE](mf-sa-d3d12-heap-type.md)  | Contiene un valor que especifica el tipo de montón usado para los recursos de Direct3D en la secuencia. |




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> <dt>

[Representador de vídeo mejorado](enhanced-video-renderer.md)
</dt> </dl>

 

 



