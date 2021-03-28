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
# <a name="tiled-resource-creation-parameters"></a><span data-ttu-id="07a68-104">Parámetros de creación de recursos en mosaico</span><span class="sxs-lookup"><span data-stu-id="07a68-104">Tiled resource creation parameters</span></span>

<span data-ttu-id="07a68-105">Existen algunas restricciones en el tipo de recursos de Direct3D que se pueden crear con la marca de [**\_ mosaico de \_ varios \_ recursos de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) .</span><span class="sxs-lookup"><span data-stu-id="07a68-105">There are some constraints on the type of Direct3D resources that you can create with the [**D3D11\_RESOURCE\_MISC\_TILED**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) flag.</span></span> <span data-ttu-id="07a68-106">En esta sección se proporcionan los parámetros válidos para crear recursos en mosaico.</span><span class="sxs-lookup"><span data-stu-id="07a68-106">This section provides the valid parameters for creating tiled resources.</span></span>

<dl> <dt>

<span data-ttu-id="07a68-107"><span id="Supported_Resource_Type"></span><span id="supported_resource_type"></span><span id="SUPPORTED_RESOURCE_TYPE"></span>**Tipo de recurso admitido**</span><span class="sxs-lookup"><span data-stu-id="07a68-107"><span id="Supported_Resource_Type"></span><span id="supported_resource_type"></span><span id="SUPPORTED_RESOURCE_TYPE"></span>**Supported Resource Type**</span></span>
</dt> <dd>

<span data-ttu-id="07a68-108">\[Matriz Texture2D \] (incluida la \[ matriz TextureCube \] , que es una variante de la \[ matriz Texture2D \] ) o el búfer.</span><span class="sxs-lookup"><span data-stu-id="07a68-108">Texture2D\[Array\] (including TextureCube\[Array\], which is a variant of Texture2D\[Array\]) or Buffer.</span></span>

<span data-ttu-id="07a68-109">**No compatible:** Texture1D \[ array \] o Texture3D, pero podría ser compatible con Texture3D en el futuro.</span><span class="sxs-lookup"><span data-stu-id="07a68-109">**NOT supported:** Texture1D\[Array\] or Texture3D, but Texture3D might be supported in the future.</span></span>

</dd> <dt>

<span data-ttu-id="07a68-110"><span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Uso de recursos admitido**</span><span class="sxs-lookup"><span data-stu-id="07a68-110"><span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Supported Resource Usage**</span></span>
</dt> <dd>

<span data-ttu-id="07a68-111">\_Valor predeterminado de uso de D3D11 \_ .</span><span class="sxs-lookup"><span data-stu-id="07a68-111">D3D11\_USAGE\_DEFAULT.</span></span>

<span data-ttu-id="07a68-112">**No compatible:** Uso de D3D11 \_ \_ dinámico, \_ almacenamiento provisional de uso de D3D11 \_ o uso de D3D11 \_ \_ inmutable.</span><span class="sxs-lookup"><span data-stu-id="07a68-112">**NOT supported:** D3D11\_USAGE\_DYNAMIC, D3D11\_USAGE\_STAGING, or D3D11\_USAGE\_IMMUTABLE.</span></span>

</dd> <dt>

<span data-ttu-id="07a68-113"><span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Marcas misceláneos de recursos admitidas**</span><span class="sxs-lookup"><span data-stu-id="07a68-113"><span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Supported Resource Misc Flags**</span></span>
</dt> <dd>

<span data-ttu-id="07a68-114">El \_ recurso D3D11 \_ varios \_ mosaicos (por definición), \_ varios \_ TEXTURECUBE, \_ DRAWINDIRECT \_ args, el \_ búfer \_ permite \_ vistas sin procesar \_ , \_ búfer \_ estructurado, abrazadera de \_ recursos \_ o \_ genera \_ MIPS.</span><span class="sxs-lookup"><span data-stu-id="07a68-114">D3D11\_RESOURCE\_MISC\_TILED (by definition), \_MISC\_TEXTURECUBE, \_DRAWINDIRECT\_ARGS, \_BUFFER\_ALLOW\_RAW\_VIEWS, \_BUFFER\_STRUCTURED, \_RESOURCE\_CLAMP, or \_GENERATE\_MIPS.</span></span>

<span data-ttu-id="07a68-115">**No compatible:** \_ COMPARTIDO, \_ compartido \_ KEYEDMUTEX, \_ \_ compatible con GDI \_ , \_ NTHANDLE compartido \_ , \_ contenido restringido, \_ restringir \_ \_ recurso compartido, \_ restringir \_ \_ controlador de recursos compartidos \_ , \_ protegido o \_ grupo de mosaicos \_ .</span><span class="sxs-lookup"><span data-stu-id="07a68-115">**NOT supported:** \_SHARED, \_SHARED\_KEYEDMUTEX, \_GDI\_COMPATIBLE, \_SHARED\_NTHANDLE, \_RESTRICTED\_CONTENT, \_RESTRICT\_SHARED\_RESOURCE, \_RESTRICT\_SHARED\_RESOURCE\_DRIVER, \_GUARDED, or \_TILE\_POOL.</span></span>

</dd> <dt>

<span data-ttu-id="07a68-116"><span id="Supported_Bind_Flags"></span><span id="supported_bind_flags"></span><span id="SUPPORTED_BIND_FLAGS"></span>**Marcas de enlace admitidas**</span><span class="sxs-lookup"><span data-stu-id="07a68-116"><span id="Supported_Bind_Flags"></span><span id="supported_bind_flags"></span><span id="SUPPORTED_BIND_FLAGS"></span>**Supported Bind Flags**</span></span>
</dt> <dd>

<span data-ttu-id="07a68-117">\_ \_ Recurso de sombreador \_ de enlace de D3D11, \_ \_ destino de representación, \_ Galería de \_ símbolos de profundidad o \_ acceso desordenado \_ .</span><span class="sxs-lookup"><span data-stu-id="07a68-117">D3D11\_BIND\_SHADER\_RESOURCE, \_RENDER\_TARGET, \_DEPTH\_STENCIL, or \_UNORDERED\_ACCESS.</span></span>

<span data-ttu-id="07a68-118">**No compatible:** \_ \_Búfer de constantes, \_ búfer de vértices \_ \[ tenga en cuenta que el enlace de un búfer en mosaico como SRV/UAV/RTV sigue siendo correcto \] , \_ \_ búfer de índice, \_ salida de flujo \_ , \_ \_ descodificador de enlace o \_ \_ codificador de vídeo BIND \_ .</span><span class="sxs-lookup"><span data-stu-id="07a68-118">**NOT supported:** \_CONSTANT\_BUFFER, \_VERTEX\_BUFFER \[note that binding a tiled Buffer as an SRV/UAV/RTV is still ok\], \_INDEX\_BUFFER, \_STREAM\_OUTPUT, \_BIND\_DECODER, or \_BIND\_VIDEO\_ENCODER.</span></span>

</dd> <dt>

<span data-ttu-id="07a68-119"><span id="Supported_Formats"></span><span id="supported_formats"></span><span id="SUPPORTED_FORMATS"></span>**Formatos admitidos**</span><span class="sxs-lookup"><span data-stu-id="07a68-119"><span id="Supported_Formats"></span><span id="supported_formats"></span><span id="SUPPORTED_FORMATS"></span>**Supported Formats**</span></span>
</dt> <dd>

<span data-ttu-id="07a68-120">Todos los formatos que estarán disponibles para la configuración determinada, independientemente de que se coloquen en mosaico, con algunas excepciones.</span><span class="sxs-lookup"><span data-stu-id="07a68-120">All formats that would be available for the given configuration regardless of it being tiled, with some exceptions.</span></span>

</dd> <dt>

<span data-ttu-id="07a68-121"><span id="Supported_SampleDesc__Multisample_count__quality_"></span><span id="supported_sampledesc__multisample_count__quality_"></span><span id="SUPPORTED_SAMPLEDESC__MULTISAMPLE_COUNT__QUALITY_"></span>**SampleDesc compatible (recuento de muestreo Multimuestra, calidad)**</span><span class="sxs-lookup"><span data-stu-id="07a68-121"><span id="Supported_SampleDesc__Multisample_count__quality_"></span><span id="supported_sampledesc__multisample_count__quality_"></span><span id="SUPPORTED_SAMPLEDESC__MULTISAMPLE_COUNT__QUALITY_"></span>**Supported SampleDesc (Multisample count, quality)**</span></span>
</dt> <dd>

<span data-ttu-id="07a68-122">Lo que se admitiría para la configuración determinada, independientemente de que se haya colocado en mosaico, con algunas excepciones.</span><span class="sxs-lookup"><span data-stu-id="07a68-122">Whatever would be supported for the given configuration regardless of it being tiled, with some exceptions.</span></span>

</dd> <dt>

<span data-ttu-id="07a68-123"><span id="Supported_Width_Height_MipLevels_ArraySize"></span><span id="supported_width_height_miplevels_arraysize"></span><span id="SUPPORTED_WIDTH_HEIGHT_MIPLEVELS_ARRAYSIZE"></span>**Width/height/MipLevels/tamaño admitidos**</span><span class="sxs-lookup"><span data-stu-id="07a68-123"><span id="Supported_Width_Height_MipLevels_ArraySize"></span><span id="supported_width_height_miplevels_arraysize"></span><span id="SUPPORTED_WIDTH_HEIGHT_MIPLEVELS_ARRAYSIZE"></span>**Supported Width/Height/MipLevels/ArraySize**</span></span>
</dt> <dd>

<span data-ttu-id="07a68-124">Extensiones completas admitidas por Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="07a68-124">Full extents supported by Direct3D 11.</span></span> <span data-ttu-id="07a68-125">Los recursos en mosaico no tienen la restricción del tamaño total de la memoria impuesta en los recursos no en mosaico.</span><span class="sxs-lookup"><span data-stu-id="07a68-125">Tiled resources don't have the restriction on total memory size imposed on non-tiled resources.</span></span> <span data-ttu-id="07a68-126">Los recursos en mosaico solo están restringidos por límites generales de espacio de direcciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="07a68-126">Tiled resources are only constrained by overall virtual address space limits.</span></span> <span data-ttu-id="07a68-127">Para obtener información, consulte [espacio de direcciones disponible para los recursos en mosaico](address-space-available-for-tiled-resources.md).</span><span class="sxs-lookup"><span data-stu-id="07a68-127">For info, see [Address space available for tiled resources](address-space-available-for-tiled-resources.md).</span></span>

</dd> </dl>

<span data-ttu-id="07a68-128">El contenido inicial de la memoria del grupo de mosaicos es indefinido.</span><span class="sxs-lookup"><span data-stu-id="07a68-128">The initial contents of tile pool memory are undefined.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07a68-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="07a68-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07a68-130">Crear recursos en mosaico</span><span class="sxs-lookup"><span data-stu-id="07a68-130">Creating tiled resources</span></span>](creating-tiled-resources.md)
</dt> </dl>

 

 




