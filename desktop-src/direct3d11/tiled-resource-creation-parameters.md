---
title: Parámetros de creación de recursos en mosaico
description: Existen algunas restricciones en el tipo de recursos de Direct3D que se pueden crear con la \_ marca de mosaico de varios recursos de D3D11 \_ \_ . En esta sección se proporcionan los parámetros válidos para crear recursos en mosaico.
ms.assetid: 19A0EA7F-888D-4102-A5D2-F3B54775EDE8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b912325371c59bd46a6cc4245289b2fe5d32a924
ms.sourcegitcommit: 4dcafeb002cbee4f6028b32a956ec22cb95cbc44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/13/2019
ms.locfileid: "103784865"
---
# <a name="tiled-resource-creation-parameters"></a>Parámetros de creación de recursos en mosaico

Existen algunas restricciones en el tipo de recursos de Direct3D que se pueden crear con la marca de [**\_ mosaico de \_ varios \_ recursos de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) . En esta sección se proporcionan los parámetros válidos para crear recursos en mosaico.

<dl> <dt>

<span id="Supported_Resource_Type"></span><span id="supported_resource_type"></span><span id="SUPPORTED_RESOURCE_TYPE"></span>**Tipo de recurso admitido**
</dt> <dd>

\[Matriz Texture2D \] (incluida la \[ matriz TextureCube \] , que es una variante de la \[ matriz Texture2D \] ) o el búfer.

**No compatible:** Texture1D \[ array \] o Texture3D, pero podría ser compatible con Texture3D en el futuro.

</dd> <dt>

<span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Uso de recursos admitido**
</dt> <dd>

\_Valor predeterminado de uso de D3D11 \_ .

**No compatible:** Uso de D3D11 \_ \_ dinámico, \_ almacenamiento provisional de uso de D3D11 \_ o uso de D3D11 \_ \_ inmutable.

</dd> <dt>

<span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Marcas misceláneos de recursos admitidas**
</dt> <dd>

El \_ recurso D3D11 \_ varios \_ mosaicos (por definición), \_ varios \_ TEXTURECUBE, \_ DRAWINDIRECT \_ args, el \_ búfer \_ permite \_ vistas sin procesar \_ , \_ búfer \_ estructurado, abrazadera de \_ recursos \_ o \_ genera \_ MIPS.

**No compatible:** \_ COMPARTIDO, \_ compartido \_ KEYEDMUTEX, \_ \_ compatible con GDI \_ , \_ NTHANDLE compartido \_ , \_ contenido restringido, \_ restringir \_ \_ recurso compartido, \_ restringir \_ \_ controlador de recursos compartidos \_ , \_ protegido o \_ grupo de mosaicos \_ .

</dd> <dt>

<span id="Supported_Bind_Flags"></span><span id="supported_bind_flags"></span><span id="SUPPORTED_BIND_FLAGS"></span>**Marcas de enlace admitidas**
</dt> <dd>

\_ \_ Recurso de sombreador \_ de enlace de D3D11, \_ \_ destino de representación, \_ Galería de \_ símbolos de profundidad o \_ acceso desordenado \_ .

**No compatible:** \_ \_Búfer de constantes, \_ búfer de vértices \_ \[ tenga en cuenta que el enlace de un búfer en mosaico como SRV/UAV/RTV sigue siendo correcto \] , \_ \_ búfer de índice, \_ salida de flujo \_ , \_ \_ descodificador de enlace o \_ \_ codificador de vídeo BIND \_ .

</dd> <dt>

<span id="Supported_Formats"></span><span id="supported_formats"></span><span id="SUPPORTED_FORMATS"></span>**Formatos admitidos**
</dt> <dd>

Todos los formatos que estarán disponibles para la configuración determinada, independientemente de que se coloquen en mosaico, con algunas excepciones.

</dd> <dt>

<span id="Supported_SampleDesc__Multisample_count__quality_"></span><span id="supported_sampledesc__multisample_count__quality_"></span><span id="SUPPORTED_SAMPLEDESC__MULTISAMPLE_COUNT__QUALITY_"></span>**SampleDesc compatible (recuento de muestreo Multimuestra, calidad)**
</dt> <dd>

Lo que se admitiría para la configuración determinada, independientemente de que se haya colocado en mosaico, con algunas excepciones.

</dd> <dt>

<span id="Supported_Width_Height_MipLevels_ArraySize"></span><span id="supported_width_height_miplevels_arraysize"></span><span id="SUPPORTED_WIDTH_HEIGHT_MIPLEVELS_ARRAYSIZE"></span>**Width/height/MipLevels/tamaño admitidos**
</dt> <dd>

Extensiones completas admitidas por Direct3D 11. Los recursos en mosaico no tienen la restricción del tamaño total de la memoria impuesta en los recursos no en mosaico. Los recursos en mosaico solo están restringidos por límites generales de espacio de direcciones virtuales. Para obtener información, consulte [espacio de direcciones disponible para los recursos en mosaico](address-space-available-for-tiled-resources.md).

</dd> </dl>

El contenido inicial de la memoria del grupo de mosaicos es indefinido.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear recursos en mosaico](creating-tiled-resources.md)
</dt> </dl>

 

 




