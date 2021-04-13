---
title: ILockBytes-File-Based implementación
description: Se implementa en un objeto de matriz de bytes subyacente de un objeto de almacenamiento de archivos compuesto COM y está diseñado para leer y escribir directamente en un archivo de disco.
ms.assetid: 700b6a3c-1046-4c21-8887-16f344c23510
keywords:
- ILockBytes Strctd STG, implementaciones, basado en archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93dfe09ab0157d2d24d81b7bb2798e984d3848f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418449"
---
# <a name="ilockbytes---file-based-implementation"></a><span data-ttu-id="c103b-104">ILockBytes-File-Based implementación</span><span class="sxs-lookup"><span data-stu-id="c103b-104">ILockBytes - File-Based Implementation</span></span>

<span data-ttu-id="c103b-105">Se implementa en un objeto de matriz de bytes subyacente de un objeto de almacenamiento de archivos compuesto COM y está diseñado para leer y escribir directamente en un archivo de disco.</span><span class="sxs-lookup"><span data-stu-id="c103b-105">Implemented on a byte array object underlying a COM compound file storage object, and designed to read and write directly to a disk file.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="c103b-106">Cuándo usar</span><span class="sxs-lookup"><span data-stu-id="c103b-106">When to Use</span></span>

<span data-ttu-id="c103b-107">Se llama a los métodos de [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) desde las implementaciones de archivos compuestos de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) y [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) en el objeto de almacenamiento de archivos compuesto creado a través de una llamada a [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), por lo que no es necesario llamarlos directamente.</span><span class="sxs-lookup"><span data-stu-id="c103b-107">Methods of [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) are called from the compound file implementations of [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) and [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) on the compound file storage object created through a call to [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), so you do not need to call them directly.</span></span>

## <a name="remarks"></a><span data-ttu-id="c103b-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c103b-108">Remarks</span></span>

<span data-ttu-id="c103b-109">A continuación se muestran los métodos de la implementación de File-Based [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) .</span><span class="sxs-lookup"><span data-stu-id="c103b-109">The following are the methods of the [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) File-Based Implementation.</span></span>

<dl> <dt>

<span data-ttu-id="c103b-110"><span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes:: readatum**</span><span class="sxs-lookup"><span data-stu-id="c103b-110"><span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes::ReadAt**</span></span>
</dt> <dd>

<span data-ttu-id="c103b-111">Lee un bloque de bytes de un desplazamiento especificado al principio de la matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="c103b-111">Reads a block of bytes from a specified offset at the beginning of the byte-array.</span></span>

</dd> <dt>

<span data-ttu-id="c103b-112"><span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes:: WriteAt**</span><span class="sxs-lookup"><span data-stu-id="c103b-112"><span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes::WriteAt**</span></span>
</dt> <dd>

<span data-ttu-id="c103b-113">Escribe un bloque de bytes a partir de un desplazamiento especificado al principio de la matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="c103b-113">Writes a block of bytes from a specified offset at the beginning of the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="c103b-114"><span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes:: Flush**</span><span class="sxs-lookup"><span data-stu-id="c103b-114"><span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes::Flush**</span></span>
</dt> <dd>

<span data-ttu-id="c103b-115">Garantiza que todos los búferes internos mantenidos por la implementación de [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) se escriben en el almacenamiento físico subyacente.</span><span class="sxs-lookup"><span data-stu-id="c103b-115">Ensures that any internal buffers maintained by the [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) implementation are written out to the underlying physical storage.</span></span>

</dd> <dt>

<span data-ttu-id="c103b-116"><span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes:: setSize**</span><span class="sxs-lookup"><span data-stu-id="c103b-116"><span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes::SetSize**</span></span>
</dt> <dd>

<span data-ttu-id="c103b-117">Establece el tamaño de la matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="c103b-117">Sets the size of the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="c103b-118"><span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes:: LockRegion**</span><span class="sxs-lookup"><span data-stu-id="c103b-118"><span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes::LockRegion**</span></span>
</dt> <dd>

<span data-ttu-id="c103b-119">El parámetro *dwLockTypes* se establece en Lock \_ ONLYONCE o Lock \_ Exclusive, lo que permitirá o restringirá el acceso a las regiones bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="c103b-119">The *dwLockTypes* parameter is set to LOCK\_ONLYONCE or LOCK\_EXCLUSIVE, which will allow or restrict access to locked regions.</span></span>

</dd> <dt>

<span data-ttu-id="c103b-120"><span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes:: UnlockRegion**</span><span class="sxs-lookup"><span data-stu-id="c103b-120"><span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes::UnlockRegion**</span></span>
</dt> <dd>

<span data-ttu-id="c103b-121">Este método desbloquea la región bloqueada por [**ILockBytes:: LockRegion**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-lockregion).</span><span class="sxs-lookup"><span data-stu-id="c103b-121">This method unlocks the region locked by [**ILockBytes::LockRegion**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-lockregion).</span></span>

</dd> <dt>

<span data-ttu-id="c103b-122"><span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes:: Stat**</span><span class="sxs-lookup"><span data-stu-id="c103b-122"><span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes::Stat**</span></span>
</dt> <dd>

<span data-ttu-id="c103b-123">La implementación [**IStorage:: Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) proporcionada por com llama al método [**ILockBytes:: Stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) para recuperar información sobre el objeto de matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="c103b-123">The COM-provided [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) implementation calls the [**ILockBytes::Stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) method to retrieve information about the byte array object.</span></span> <span data-ttu-id="c103b-124">Si no hay un nombre razonable para la matriz de bytes, el método **ILockBytes:: Stat** proporcionado por com devuelve **null** en el miembro **pwcsName** de la estructura [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) .</span><span class="sxs-lookup"><span data-stu-id="c103b-124">If there is no reasonable name for the byte array, the COM-provided **ILockBytes::Stat** method returns **NULL** in the **pwcsName** member of the [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) structure.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="c103b-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c103b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c103b-126">**ILockBytes**</span><span class="sxs-lookup"><span data-stu-id="c103b-126">**ILockBytes**</span></span>](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[<span data-ttu-id="c103b-127">**IStorage**</span><span class="sxs-lookup"><span data-stu-id="c103b-127">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[<span data-ttu-id="c103b-128">**IStream**</span><span class="sxs-lookup"><span data-stu-id="c103b-128">**IStream**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> </dl>

 

 




