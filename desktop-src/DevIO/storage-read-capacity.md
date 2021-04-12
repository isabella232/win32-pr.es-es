---
description: Contiene información sobre el tamaño de un dispositivo. Esto se devuelve desde el código de control de la capacidad de lectura de almacenamiento de IOCTL \_ \_ \_ .
ms.assetid: bd18f4b7-f87e-48f6-b7c2-68990beb8d36
title: STORAGE_READ_CAPACITY estructura (Ntddstor. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_READ_CAPACITY
api_type:
- HeaderDef
api_location:
- Ntddstor.h
ms.openlocfilehash: e57a9f4420b977598e15f9aae219c060665c9d0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423259"
---
# <a name="storage_read_capacity-structure"></a><span data-ttu-id="beb4c-104">Estructura de capacidad de \_ lectura de almacenamiento \_</span><span class="sxs-lookup"><span data-stu-id="beb4c-104">STORAGE\_READ\_CAPACITY structure</span></span>

<span data-ttu-id="beb4c-105">Contiene información sobre el tamaño de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="beb4c-105">Contains information about the size of a device.</span></span> <span data-ttu-id="beb4c-106">Esto se devuelve desde el código de control de la [**capacidad de lectura de almacenamiento de ioctl \_ \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity) .</span><span class="sxs-lookup"><span data-stu-id="beb4c-106">This is returned from the [**IOCTL\_STORAGE\_READ\_CAPACITY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity) control code.</span></span>

## <a name="syntax"></a><span data-ttu-id="beb4c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="beb4c-107">Syntax</span></span>


```C++
typedef struct _STORAGE_READ_CAPACITY {
  ULONG         Version;
  ULONG         Size;
  ULONG         BlockLength;
  LARGE_INTEGER NumberOfBlocks;
  LARGE_INTEGER DiskLength;
} STORAGE_READ_CAPACITY, *PSTORAGE_READ_CAPACITY;
```



## <a name="members"></a><span data-ttu-id="beb4c-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="beb4c-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="beb4c-109">**Versión**</span><span class="sxs-lookup"><span data-stu-id="beb4c-109">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="beb4c-110">Versión de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="beb4c-110">The version of this structure.</span></span> <span data-ttu-id="beb4c-111">El autor de la llamada debe establecer este miembro en `sizeof(STORAGE_READ_CAPACITY)` .</span><span class="sxs-lookup"><span data-stu-id="beb4c-111">The caller must set this member to `sizeof(STORAGE_READ_CAPACITY)`.</span></span>

</dd> <dt>

<span data-ttu-id="beb4c-112">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="beb4c-112">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="beb4c-113">Tamaño de los datos devueltos.</span><span class="sxs-lookup"><span data-stu-id="beb4c-113">The size of the data returned.</span></span>

</dd> <dt>

<span data-ttu-id="beb4c-114">**BlockLength**</span><span class="sxs-lookup"><span data-stu-id="beb4c-114">**BlockLength**</span></span>
</dt> <dd>

<span data-ttu-id="beb4c-115">Número de bytes por bloque.</span><span class="sxs-lookup"><span data-stu-id="beb4c-115">The number of bytes per block.</span></span>

</dd> <dt>

<span data-ttu-id="beb4c-116">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="beb4c-116">**NumberOfBlocks**</span></span>
</dt> <dd>

<span data-ttu-id="beb4c-117">Número total de bloques en el disco.</span><span class="sxs-lookup"><span data-stu-id="beb4c-117">The total number of blocks on the disk.</span></span>

</dd> <dt>

<span data-ttu-id="beb4c-118">**DiskLength**</span><span class="sxs-lookup"><span data-stu-id="beb4c-118">**DiskLength**</span></span>
</dt> <dd>

<span data-ttu-id="beb4c-119">El tamaño del disco en bytes.</span><span class="sxs-lookup"><span data-stu-id="beb4c-119">The disk size in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="beb4c-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="beb4c-120">Remarks</span></span>

<span data-ttu-id="beb4c-121">El archivo de encabezado Ntddstor. h está disponible en el kit de controladores de Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="beb4c-121">The header file Ntddstor.h is available in the Windows Driver Kit (WDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="beb4c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="beb4c-122">Requirements</span></span>



| <span data-ttu-id="beb4c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="beb4c-123">Requirement</span></span> | <span data-ttu-id="beb4c-124">Value</span><span class="sxs-lookup"><span data-stu-id="beb4c-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="beb4c-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="beb4c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="beb4c-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="beb4c-126">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="beb4c-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="beb4c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="beb4c-128">Windows Server 2008, Windows Server 2003 con SP1</span><span class="sxs-lookup"><span data-stu-id="beb4c-128">Windows Server 2008, Windows Server 2003 with SP1</span></span><br/>                          |
| <span data-ttu-id="beb4c-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="beb4c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="beb4c-130"><dt>Ntddstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="beb4c-130"><dt>Ntddstor.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="beb4c-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="beb4c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beb4c-132">**\_capacidad de \_ lectura de almacenamiento de ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="beb4c-132">**IOCTL\_STORAGE\_READ\_CAPACITY**</span></span>](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity)
</dt> </dl>

 

 




