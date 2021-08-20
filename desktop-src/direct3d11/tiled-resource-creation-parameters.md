---
title: Parámetros de creación de recursos en mosaico
description: Hay algunas restricciones en el tipo de recursos de Direct3D que puede crear con la marca MISC TILED DE RECURSOS D3D11. \_ \_ \_ En esta sección se proporcionan los parámetros válidos para crear recursos en mosaico.
ms.assetid: 19A0EA7F-888D-4102-A5D2-F3B54775EDE8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9668c21060cbb8f39884204780ce689b3e67196aef0bdcfef891836768f04af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279845"
---
# <a name="tiled-resource-creation-parameters"></a>Parámetros de creación de recursos en mosaico

Hay algunas restricciones en el tipo de recursos de Direct3D que puede crear con la marca [**\_ \_ MISC \_ TILED DE RECURSOS D3D11.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) En esta sección se proporcionan los parámetros válidos para crear recursos en mosaico.

<dl> <dt>

<span id="Supported_Resource_Type"></span><span id="supported_resource_type"></span><span id="SUPPORTED_RESOURCE_TYPE"></span>**Tipo de recurso admitido**
</dt> <dd>

Matriz Texture2D \[ \] (incluida la matriz TextureCube \[ , que es una variante de \] Texture2D \[ \] Array) o Buffer.

**NO se admite:** Texture1D \[ Array \] o Texture3D, pero Texture3D podría ser compatible en el futuro.

</dd> <dt>

<span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Uso de recursos admitido**
</dt> <dd>

VALOR PREDETERMINADO DE USO DE D3D11. \_ \_

**NO se admite:** D3D11 \_ USAGE \_ DYNAMIC, D3D11 \_ USAGE STAGING o \_ D3D11 \_ USAGE \_ IMMUTABLE.

</dd> <dt>

<span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Marcas misc de recursos admitidas**
</dt> <dd>

RECURSO D3D11 \_ \_ \_ MISC TILED (por definición), \_ MISC \_ TEXTURECUBE, \_ DRAWINDIRECT \_ ARGS, \_ BUFFER ALLOW RAW \_ \_ VIEWS, BUFFER STRUCTURED, RESOURCE CLAMP o \_ GENERATE \_ \_ \_ \_ \_ \_ MIPS.

**NO se admite:** \_ SHARED, \_ SHARED \_ KEYEDMUTEX, \_ GDI \_ COMPATIBLE, SHARED \_ \_ NTHANDLE, \_ RESTRICTED \_ CONTENT, RESTRICT SHARED \_ \_ \_ RESOURCE, RESTRICT SHARED RESOURCE \_ \_ \_ \_ DRIVER, \_ GUARDED o TILE \_ \_ POOL.

</dd> <dt>

<span id="Supported_Bind_Flags"></span><span id="supported_bind_flags"></span><span id="SUPPORTED_BIND_FLAGS"></span>**Marcas de enlace admitidas**
</dt> <dd>

D3D11 \_ BIND \_ SHADER \_ RESOURCE, RENDER \_ \_ TARGET, DEPTH \_ \_ STENCIL o \_ UNORDERED \_ ACCESS.

**NO se admite:** \_ CONSTANT BUFFER, VERTEX BUFFER tenga en cuenta que el enlace de un búfer en mosaico como \_ \_ \_ \[ SRV/UAV/RTV sigue siendo \] correcto, \_ INDEX \_ BUFFER, STREAM OUTPUT, BIND DECODER o \_ \_ BIND VIDEO \_ \_ \_ \_ \_ ENCODER.

</dd> <dt>

<span id="Supported_Formats"></span><span id="supported_formats"></span><span id="SUPPORTED_FORMATS"></span>**Formatos admitidos**
</dt> <dd>

Todos los formatos que estarían disponibles para la configuración dada independientemente de que se esté en mosaico, con algunas excepciones.

</dd> <dt>

<span id="Supported_SampleDesc__Multisample_count__quality_"></span><span id="supported_sampledesc__multisample_count__quality_"></span><span id="SUPPORTED_SAMPLEDESC__MULTISAMPLE_COUNT__QUALITY_"></span>**SampleDesc admitido (recuento de varios ejemplos, calidad)**
</dt> <dd>

Todo lo que se admite para la configuración determinada independientemente de que se esté en mosaico, con algunas excepciones.

</dd> <dt>

<span id="Supported_Width_Height_MipLevels_ArraySize"></span><span id="supported_width_height_miplevels_arraysize"></span><span id="SUPPORTED_WIDTH_HEIGHT_MIPLEVELS_ARRAYSIZE"></span>**Width/Height/MipLevels/ArraySize admitidos**
</dt> <dd>

Extensiones completa compatibles con Direct3D 11. Los recursos en mosaico no tienen la restricción del tamaño total de memoria impuesto a los recursos que no están en mosaico. Los recursos en mosaico solo están restringidos por los límites generales de espacio de direcciones virtuales. Para obtener información, consulte [Espacio de direcciones disponible para recursos en mosaico.](address-space-available-for-tiled-resources.md)

</dd> </dl>

El contenido inicial de la memoria del grupo de mosaicos no está definido.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de recursos en mosaico](creating-tiled-resources.md)
</dt> </dl>

 

 




