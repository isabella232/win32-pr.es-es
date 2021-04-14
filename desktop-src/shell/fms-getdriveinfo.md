---
description: Contiene información acerca de la unidad seleccionada en la ventana del administrador de archivos activo (la ventana Directorio o la ventana Resultados de la búsqueda).
title: FMS_GETDRIVEINFO estructura (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_GETDRIVEINFO
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 14f8a90b-d0ed-4818-a719-8fc4ea617bef
ms.openlocfilehash: b19b54d89f74fa122effa5853beb2961e0ddf1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985510"
---
# <a name="fms_getdriveinfo-structure"></a><span data-ttu-id="39ce3-103">Estructura de FMS \_ GETDRIVEINFO</span><span class="sxs-lookup"><span data-stu-id="39ce3-103">FMS\_GETDRIVEINFO structure</span></span>

<span data-ttu-id="39ce3-104">Contiene información acerca de la unidad seleccionada en la ventana del administrador de archivos activo (la ventana Directorio o la ventana Resultados de la búsqueda).</span><span class="sxs-lookup"><span data-stu-id="39ce3-104">Contains information about the drive selected in the active File Manager window (the directory window or the Search Results window).</span></span>

## <a name="syntax"></a><span data-ttu-id="39ce3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="39ce3-105">Syntax</span></span>


```C++
typedef struct _FMS_GETDRIVEINFO {
  DWORD dwTotalSpace;
  DWORD dwFreeSpace;
  TCHAR szPath[260];
  TCHAR szVolume[14];
  TCHAR szShare[128];
} FMS_GETDRIVEINFO;
```



## <a name="members"></a><span data-ttu-id="39ce3-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="39ce3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="39ce3-107">**dwTotalSpace**</span><span class="sxs-lookup"><span data-stu-id="39ce3-107">**dwTotalSpace**</span></span>
</dt> <dd>

<span data-ttu-id="39ce3-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="39ce3-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="39ce3-109">La cantidad total de espacio de almacenamiento, en bytes, del disco asociado a la unidad.</span><span class="sxs-lookup"><span data-stu-id="39ce3-109">The total amount of storage space, in bytes, on the disk associated with the drive.</span></span>

</dd> <dt>

<span data-ttu-id="39ce3-110">**dwFreeSpace**</span><span class="sxs-lookup"><span data-stu-id="39ce3-110">**dwFreeSpace**</span></span>
</dt> <dd>

<span data-ttu-id="39ce3-111">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="39ce3-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="39ce3-112">Cantidad de espacio de almacenamiento libre, en bytes, en el disco asociado a la unidad.</span><span class="sxs-lookup"><span data-stu-id="39ce3-112">The amount of free storage space, in bytes, on the disk associated with the drive.</span></span>

</dd> <dt>

<span data-ttu-id="39ce3-113">**szPath**</span><span class="sxs-lookup"><span data-stu-id="39ce3-113">**szPath**</span></span>
</dt> <dd>

<span data-ttu-id="39ce3-114">Tipo: **TCHAR \[ 260 \]**</span><span class="sxs-lookup"><span data-stu-id="39ce3-114">Type: **TCHAR\[260\]**</span></span>

</dd> <dd>

<span data-ttu-id="39ce3-115">la ruta de acceso terminada en NULL del directorio actual.</span><span class="sxs-lookup"><span data-stu-id="39ce3-115">the null-terminated path of the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="39ce3-116">**szVolume**</span><span class="sxs-lookup"><span data-stu-id="39ce3-116">**szVolume**</span></span>
</dt> <dd>

<span data-ttu-id="39ce3-117">Tipo: **TCHAR \[ 14 \]**</span><span class="sxs-lookup"><span data-stu-id="39ce3-117">Type: **TCHAR\[14\]**</span></span>

</dd> <dd>

<span data-ttu-id="39ce3-118">Etiqueta de volumen terminada en NULL del disco asociado a la unidad.</span><span class="sxs-lookup"><span data-stu-id="39ce3-118">The null-terminated volume label of the disk associated with the drive.</span></span>

</dd> <dt>

<span data-ttu-id="39ce3-119">**szShare**</span><span class="sxs-lookup"><span data-stu-id="39ce3-119">**szShare**</span></span>
</dt> <dd>

<span data-ttu-id="39ce3-120">Tipo: **TCHAR \[ 128 \]**</span><span class="sxs-lookup"><span data-stu-id="39ce3-120">Type: **TCHAR\[128\]**</span></span>

</dd> <dd>

<span data-ttu-id="39ce3-121">Nombre terminado en NULL del recurso de red (si se tiene acceso a la unidad a través de una red).</span><span class="sxs-lookup"><span data-stu-id="39ce3-121">The null-terminated name of the network resource (if the drive is being accessed through a network).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="39ce3-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39ce3-122">Requirements</span></span>



| <span data-ttu-id="39ce3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="39ce3-123">Requirement</span></span> | <span data-ttu-id="39ce3-124">Value</span><span class="sxs-lookup"><span data-stu-id="39ce3-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="39ce3-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39ce3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="39ce3-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="39ce3-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="39ce3-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39ce3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="39ce3-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="39ce3-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="39ce3-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39ce3-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="39ce3-130"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="39ce3-130"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39ce3-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="39ce3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39ce3-132">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="39ce3-132">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="39ce3-133">**\_GETDRIVEINFO FM**</span><span class="sxs-lookup"><span data-stu-id="39ce3-133">**FM\_GETDRIVEINFO**</span></span>](fm-getdriveinfo.md)
</dt> </dl>

 

 




