---
title: 'ILockBytes: implementación de memoria global'
description: La implementación de memoria global ILockBytes se implementa en un objeto de matriz de bytes subyacente de un objeto de almacenamiento de archivos compuesto COM y está diseñado para leer y escribir directamente en la memoria global.
ms.assetid: 6ab019b0-34d7-4b6e-ba77-6b6881fabd29
keywords:
- ILockBytes Strctd STG, implementaciones, memoria global
- ILockBytes Strctd STG, implementaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9d7cae82c1503fcb53d2cfd8fee39095eb60801
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356819"
---
# <a name="ilockbytes---global-memory-implementation"></a><span data-ttu-id="a9b68-105">ILockBytes: implementación de memoria global</span><span class="sxs-lookup"><span data-stu-id="a9b68-105">ILockBytes - Global Memory Implementation</span></span>

<span data-ttu-id="a9b68-106">La implementación de memoria global ILockBytes se implementa en un objeto de matriz de bytes subyacente de un objeto de almacenamiento de archivos compuesto COM y está diseñado para leer y escribir directamente en la memoria global.</span><span class="sxs-lookup"><span data-stu-id="a9b68-106">The ILockBytes global memory implementation is implemented on a byte array object underlying a COM compound file storage object, and designed to read and write directly to global memory.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="a9b68-107">Cuándo usar</span><span class="sxs-lookup"><span data-stu-id="a9b68-107">When to Use</span></span>

<span data-ttu-id="a9b68-108">Se llama a los métodos de [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) desde las implementaciones de archivos compuestos de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) y [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) en el objeto de almacenamiento de archivos compuesto creado a través de una llamada a [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile).</span><span class="sxs-lookup"><span data-stu-id="a9b68-108">Methods of [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) are called from the compound file implementations of [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) and [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) on the compound file storage object created through a call to [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile).</span></span>

## <a name="remarks"></a><span data-ttu-id="a9b68-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a9b68-109">Remarks</span></span>

<span data-ttu-id="a9b68-110">A continuación se muestran los métodos de la implementación de memoria global [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) .</span><span class="sxs-lookup"><span data-stu-id="a9b68-110">The following are the methods of the [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) Global Memory Implementation.</span></span>

<dl> <dt>

<span data-ttu-id="a9b68-111"><span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes:: readatum**</span><span class="sxs-lookup"><span data-stu-id="a9b68-111"><span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes::ReadAt**</span></span>
</dt> <dd>

<span data-ttu-id="a9b68-112">Lee un bloque de bytes de un desplazamiento especificado al principio de la matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="a9b68-112">Reads a block of bytes from a specified offset at the beginning of the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="a9b68-113"><span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes:: WriteAt**</span><span class="sxs-lookup"><span data-stu-id="a9b68-113"><span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes::WriteAt**</span></span>
</dt> <dd>

<span data-ttu-id="a9b68-114">Escribe el bloque de bytes desde un desplazamiento especificado al principio de la matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="a9b68-114">Writes the block of bytes from a specified offset at the beginning of the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="a9b68-115"><span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes:: Flush**</span><span class="sxs-lookup"><span data-stu-id="a9b68-115"><span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes::Flush**</span></span>
</dt> <dd>

<span data-ttu-id="a9b68-116">A diferencia de la implementación basada en archivo, llamar a este método en la implementación de memoria global no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="a9b68-116">Unlike file-based implementation, calling this method in global memory implementation has no effect.</span></span>

</dd> <dt>

<span data-ttu-id="a9b68-117"><span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes:: setSize**</span><span class="sxs-lookup"><span data-stu-id="a9b68-117"><span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes::SetSize**</span></span>
</dt> <dd>

<span data-ttu-id="a9b68-118">Establece el tamaño de la matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="a9b68-118">Sets the size of the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="a9b68-119"><span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes:: LockRegion**</span><span class="sxs-lookup"><span data-stu-id="a9b68-119"><span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes::LockRegion**</span></span>
</dt> <dd>

<span data-ttu-id="a9b68-120">Esta implementación no admite el bloqueo, por lo que *dwLocksType* se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="a9b68-120">This implementation does not support locking, so *dwLocksType* is set to zero.</span></span> <span data-ttu-id="a9b68-121">El autor de la llamada debe asegurarse de que los accesos son válidos y mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="a9b68-121">The caller must ensure accesses are valid and mutually exclusive.</span></span>

</dd> <dt>

<span data-ttu-id="a9b68-122"><span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes:: UnlockRegion**</span><span class="sxs-lookup"><span data-stu-id="a9b68-122"><span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes::UnlockRegion**</span></span>
</dt> <dd>

<span data-ttu-id="a9b68-123">Esta implementación no admite el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="a9b68-123">This implementation does not support locking.</span></span>

</dd> <dt>

<span data-ttu-id="a9b68-124"><span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes:: Stat**</span><span class="sxs-lookup"><span data-stu-id="a9b68-124"><span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes::Stat**</span></span>
</dt> <dd>

<span data-ttu-id="a9b68-125">La implementación [**IStorage:: Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) proporcionada por com llama al método [**ILockBytes:: Stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) para recuperar datos sobre el objeto de matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="a9b68-125">The COM-provided [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) implementation calls the [**ILockBytes::Stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) method to retrieve data about the byte array object.</span></span> <span data-ttu-id="a9b68-126">Si no hay un nombre razonable para la matriz de bytes, el método **ILockBytes:: Stat** proporcionado por com devuelve **null** en el miembro **pwcsName** de la estructura [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) .</span><span class="sxs-lookup"><span data-stu-id="a9b68-126">If there is no reasonable name for the byte array, the COM-provided **ILockBytes::Stat** method returns **NULL** in the **pwcsName** member of the [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) structure.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="a9b68-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a9b68-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9b68-128">**ILockBytes**</span><span class="sxs-lookup"><span data-stu-id="a9b68-128">**ILockBytes**</span></span>](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[<span data-ttu-id="a9b68-129">**IStorage**</span><span class="sxs-lookup"><span data-stu-id="a9b68-129">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[<span data-ttu-id="a9b68-130">**IStream**</span><span class="sxs-lookup"><span data-stu-id="a9b68-130">**IStream**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> </dl>

 

 




