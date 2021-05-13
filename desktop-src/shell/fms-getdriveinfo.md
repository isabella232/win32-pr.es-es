---
description: Contiene información sobre la unidad seleccionada en la ventana activa del Administrador de archivos (la ventana de directorio o la ventana Resultados de la búsqueda).
title: FMS_GETDRIVEINFO estructura (Wfext.h)
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
ms.openlocfilehash: 107e12e1076a2fc928ecb9b578ab01d64898a83a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842236"
---
# <a name="fms_getdriveinfo-structure"></a><span data-ttu-id="cda1a-103">FMS \_ GETDRIVEINFO (estructura)</span><span class="sxs-lookup"><span data-stu-id="cda1a-103">FMS\_GETDRIVEINFO structure</span></span>

<span data-ttu-id="cda1a-104">Contiene información sobre la unidad seleccionada en la ventana activa del Administrador de archivos (la ventana de directorio o la ventana Resultados de la búsqueda).</span><span class="sxs-lookup"><span data-stu-id="cda1a-104">Contains information about the drive selected in the active File Manager window (the directory window or the Search Results window).</span></span>

## <a name="syntax"></a><span data-ttu-id="cda1a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cda1a-105">Syntax</span></span>


```C++
typedef struct _FMS_GETDRIVEINFO {
  DWORD dwTotalSpace;
  DWORD dwFreeSpace;
  TCHAR szPath[260];
  TCHAR szVolume[14];
  TCHAR szShare[128];
} FMS_GETDRIVEINFO;
```



## <a name="members"></a><span data-ttu-id="cda1a-106">Members</span><span class="sxs-lookup"><span data-stu-id="cda1a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="cda1a-107">**dwTotalSpace**</span><span class="sxs-lookup"><span data-stu-id="cda1a-107">**dwTotalSpace**</span></span>
</dt> <dd>

<span data-ttu-id="cda1a-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="cda1a-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="cda1a-109">Cantidad total de espacio de almacenamiento, en bytes, en el disco asociado a la unidad.</span><span class="sxs-lookup"><span data-stu-id="cda1a-109">The total amount of storage space, in bytes, on the disk associated with the drive.</span></span>

</dd> <dt>

<span data-ttu-id="cda1a-110">**dwFreeSpace**</span><span class="sxs-lookup"><span data-stu-id="cda1a-110">**dwFreeSpace**</span></span>
</dt> <dd>

<span data-ttu-id="cda1a-111">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="cda1a-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="cda1a-112">Cantidad de espacio de almacenamiento libre, en bytes, en el disco asociado a la unidad.</span><span class="sxs-lookup"><span data-stu-id="cda1a-112">The amount of free storage space, in bytes, on the disk associated with the drive.</span></span>

</dd> <dt>

<span data-ttu-id="cda1a-113">**szPath**</span><span class="sxs-lookup"><span data-stu-id="cda1a-113">**szPath**</span></span>
</dt> <dd>

<span data-ttu-id="cda1a-114">Tipo: **TCHAR \[ 260 \]**</span><span class="sxs-lookup"><span data-stu-id="cda1a-114">Type: **TCHAR\[260\]**</span></span>

</dd> <dd>

<span data-ttu-id="cda1a-115">la ruta de acceso terminada en NULL del directorio actual.</span><span class="sxs-lookup"><span data-stu-id="cda1a-115">the null-terminated path of the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="cda1a-116">**szVolume**</span><span class="sxs-lookup"><span data-stu-id="cda1a-116">**szVolume**</span></span>
</dt> <dd>

<span data-ttu-id="cda1a-117">Tipo: **TCHAR \[ 14 \]**</span><span class="sxs-lookup"><span data-stu-id="cda1a-117">Type: **TCHAR\[14\]**</span></span>

</dd> <dd>

<span data-ttu-id="cda1a-118">La etiqueta de volumen terminada en NULL del disco asociado a la unidad.</span><span class="sxs-lookup"><span data-stu-id="cda1a-118">The null-terminated volume label of the disk associated with the drive.</span></span>

</dd> <dt>

<span data-ttu-id="cda1a-119">**szShare**</span><span class="sxs-lookup"><span data-stu-id="cda1a-119">**szShare**</span></span>
</dt> <dd>

<span data-ttu-id="cda1a-120">Tipo: **TCHAR \[ 128 \]**</span><span class="sxs-lookup"><span data-stu-id="cda1a-120">Type: **TCHAR\[128\]**</span></span>

</dd> <dd>

<span data-ttu-id="cda1a-121">Nombre terminado en NULL del recurso de red (si se accede a la unidad a través de una red).</span><span class="sxs-lookup"><span data-stu-id="cda1a-121">The null-terminated name of the network resource (if the drive is being accessed through a network).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cda1a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cda1a-122">Requirements</span></span>



| <span data-ttu-id="cda1a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="cda1a-123">Requirement</span></span> | <span data-ttu-id="cda1a-124">Value</span><span class="sxs-lookup"><span data-stu-id="cda1a-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cda1a-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cda1a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cda1a-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="cda1a-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="cda1a-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cda1a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cda1a-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cda1a-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cda1a-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cda1a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="cda1a-130"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="cda1a-130"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cda1a-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="cda1a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cda1a-132">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="cda1a-132">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="cda1a-133">**FM \_ GETDRIVEINFO**</span><span class="sxs-lookup"><span data-stu-id="cda1a-133">**FM\_GETDRIVEINFO**</span></span>](fm-getdriveinfo.md)
</dt> </dl>

 

 




