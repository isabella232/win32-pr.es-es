---
title: Constantes STGM (ObjBase. h)
description: Marcas que indican las condiciones para crear y eliminar los modos de acceso y objeto del objeto.
ms.assetid: 15a35da9-332a-46e1-9190-500c95e26f59
topic_type:
- apiref
api_name:
- STGM_READ
- STGM_WRITE
- STGM_READWRITE
- STGM_SHARE_DENY_NONE
- STGM_SHARE_DENY_READ
- STGM_SHARE_DENY_WRITE
- STGM_SHARE_EXCLUSIVE
- STGM_PRIORITY
- STGM_CREATE
- STGM_CONVERT
- STGM_FAILIFTHERE
- STGM_DIRECT
- STGM_TRANSACTED
- STGM_NOSCRATCH
- STGM_NOSNAPSHOT
- STGM_SIMPLE
- STGM_DIRECT_SWMR
- STGM_DELETEONRELEASE
api_location:
- ObjBase.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd283c2dfeddc48b6bd12f8317ec352cb62e4973
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489371"
---
# <a name="stgm-constants"></a><span data-ttu-id="b6143-103">Constantes de STGM</span><span class="sxs-lookup"><span data-stu-id="b6143-103">STGM Constants</span></span>

<span data-ttu-id="b6143-104">Las constantes STGM son marcas que indican las condiciones para crear y eliminar los modos de acceso y objeto del objeto.</span><span class="sxs-lookup"><span data-stu-id="b6143-104">The STGM constants are flags that indicate conditions for creating and deleting the object and access modes for the object.</span></span> <span data-ttu-id="b6143-105">Las constantes STGM se incluyen en las interfaces [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)y [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) y en las funciones [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex), [**StgCreateDocfileOnILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes), [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)y [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) .</span><span class="sxs-lookup"><span data-stu-id="b6143-105">The STGM constants are included in the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), and [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interfaces and in the [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex), [**StgCreateDocfileOnILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes), [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage), and [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) functions.</span></span>

<span data-ttu-id="b6143-106">Estos elementos se combinan a menudo con un operador **or**.</span><span class="sxs-lookup"><span data-stu-id="b6143-106">These elements are often combined using an **OR** operator.</span></span> <span data-ttu-id="b6143-107">Se interpretan en grupos, tal y como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="b6143-107">They are interpreted in groups as listed in the following table.</span></span> <span data-ttu-id="b6143-108">No es válido usar más de un elemento de un solo grupo.</span><span class="sxs-lookup"><span data-stu-id="b6143-108">It is not valid to use more than one element from a single group.</span></span>

<span data-ttu-id="b6143-109">Use una marca del grupo de creación al crear un objeto, como con [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) o [**IStorage:: CreateStream (**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span><span class="sxs-lookup"><span data-stu-id="b6143-109">Use a flag from the creation group when creating an object, such as with [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) or [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span></span>

<span data-ttu-id="b6143-110">Para obtener más información sobre la transacción, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="b6143-110">For more information about transactioning, see the Remarks section.</span></span>



| <span data-ttu-id="b6143-111">Grupo</span><span class="sxs-lookup"><span data-stu-id="b6143-111">Group</span></span>                      | <span data-ttu-id="b6143-112">Marca</span><span class="sxs-lookup"><span data-stu-id="b6143-112">Flag</span></span>                         | <span data-ttu-id="b6143-113">Value</span><span class="sxs-lookup"><span data-stu-id="b6143-113">Value</span></span>       |
|----------------------------|------------------------------|-------------|
| <span data-ttu-id="b6143-114">Access</span><span class="sxs-lookup"><span data-stu-id="b6143-114">Access</span></span>                     | <span data-ttu-id="b6143-115">**STGM \_ lectura**</span><span class="sxs-lookup"><span data-stu-id="b6143-115">**STGM\_READ**</span></span>               | <span data-ttu-id="b6143-116">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="b6143-116">0x00000000L</span></span> |
|                            | <span data-ttu-id="b6143-117">**escritura de STGM \_**</span><span class="sxs-lookup"><span data-stu-id="b6143-117">**STGM\_WRITE**</span></span>              | <span data-ttu-id="b6143-118">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="b6143-118">0x00000001L</span></span> |
|                            | <span data-ttu-id="b6143-119">**STGM \_ ReadWrite**</span><span class="sxs-lookup"><span data-stu-id="b6143-119">**STGM\_READWRITE**</span></span>          | <span data-ttu-id="b6143-120">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="b6143-120">0x00000002L</span></span> |
| <span data-ttu-id="b6143-121">Uso compartido</span><span class="sxs-lookup"><span data-stu-id="b6143-121">Sharing</span></span>                    | <span data-ttu-id="b6143-122">**STGM \_ recurso compartido \_ denegar \_ ninguno**</span><span class="sxs-lookup"><span data-stu-id="b6143-122">**STGM\_SHARE\_DENY\_NONE**</span></span>  | <span data-ttu-id="b6143-123">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="b6143-123">0x00000040L</span></span> |
|                            | <span data-ttu-id="b6143-124">**STGM \_ recurso compartido de \_ lectura denegado \_**</span><span class="sxs-lookup"><span data-stu-id="b6143-124">**STGM\_SHARE\_DENY\_READ**</span></span>  | <span data-ttu-id="b6143-125">0x00000030L</span><span class="sxs-lookup"><span data-stu-id="b6143-125">0x00000030L</span></span> |
|                            | <span data-ttu-id="b6143-126">**STGM \_ recurso compartido \_ denegar \_ escritura**</span><span class="sxs-lookup"><span data-stu-id="b6143-126">**STGM\_SHARE\_DENY\_WRITE**</span></span> | <span data-ttu-id="b6143-127">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="b6143-127">0x00000020L</span></span> |
|                            | <span data-ttu-id="b6143-128">**STGM \_ recurso compartido \_ exclusivo**</span><span class="sxs-lookup"><span data-stu-id="b6143-128">**STGM\_SHARE\_EXCLUSIVE**</span></span>   | <span data-ttu-id="b6143-129">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="b6143-129">0x00000010L</span></span> |
|                            | <span data-ttu-id="b6143-130">**prioridad de STGM \_**</span><span class="sxs-lookup"><span data-stu-id="b6143-130">**STGM\_PRIORITY**</span></span>           | <span data-ttu-id="b6143-131">0x00040000L</span><span class="sxs-lookup"><span data-stu-id="b6143-131">0x00040000L</span></span> |
| <span data-ttu-id="b6143-132">Creación</span><span class="sxs-lookup"><span data-stu-id="b6143-132">Creation</span></span>                   | <span data-ttu-id="b6143-133">**\_crear STGM**</span><span class="sxs-lookup"><span data-stu-id="b6143-133">**STGM\_CREATE**</span></span>             | <span data-ttu-id="b6143-134">0x00001000L</span><span class="sxs-lookup"><span data-stu-id="b6143-134">0x00001000L</span></span> |
|                            | <span data-ttu-id="b6143-135">**STGM \_ convertir**</span><span class="sxs-lookup"><span data-stu-id="b6143-135">**STGM\_CONVERT**</span></span>            | <span data-ttu-id="b6143-136">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="b6143-136">0x00020000L</span></span> |
|                            | <span data-ttu-id="b6143-137">**STGM \_ FAILIFTHERE**</span><span class="sxs-lookup"><span data-stu-id="b6143-137">**STGM\_FAILIFTHERE**</span></span>        | <span data-ttu-id="b6143-138">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="b6143-138">0x00000000L</span></span> |
| <span data-ttu-id="b6143-139">Transaccional</span><span class="sxs-lookup"><span data-stu-id="b6143-139">Transactioning</span></span>             | <span data-ttu-id="b6143-140">**STGM \_ directo**</span><span class="sxs-lookup"><span data-stu-id="b6143-140">**STGM\_DIRECT**</span></span>             | <span data-ttu-id="b6143-141">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="b6143-141">0x00000000L</span></span> |
|                            | <span data-ttu-id="b6143-142">**STGM \_ transacción**</span><span class="sxs-lookup"><span data-stu-id="b6143-142">**STGM\_TRANSACTED**</span></span>         | <span data-ttu-id="b6143-143">0x00010000L</span><span class="sxs-lookup"><span data-stu-id="b6143-143">0x00010000L</span></span> |
| <span data-ttu-id="b6143-144">Rendimiento de la transacción</span><span class="sxs-lookup"><span data-stu-id="b6143-144">Transactioning Performance</span></span> | <span data-ttu-id="b6143-145">**STGM \_ NOscratch**</span><span class="sxs-lookup"><span data-stu-id="b6143-145">**STGM\_NOSCRATCH**</span></span>          | <span data-ttu-id="b6143-146">0x00100000L</span><span class="sxs-lookup"><span data-stu-id="b6143-146">0x00100000L</span></span> |
|                            | <span data-ttu-id="b6143-147">**STGM \_ NOsnapshot**</span><span class="sxs-lookup"><span data-stu-id="b6143-147">**STGM\_NOSNAPSHOT**</span></span>         | <span data-ttu-id="b6143-148">0x00200000L</span><span class="sxs-lookup"><span data-stu-id="b6143-148">0x00200000L</span></span> |
| <span data-ttu-id="b6143-149">Direct SWMR y simple</span><span class="sxs-lookup"><span data-stu-id="b6143-149">Direct SWMR and Simple</span></span>     | <span data-ttu-id="b6143-150">**STGM \_ simple**</span><span class="sxs-lookup"><span data-stu-id="b6143-150">**STGM\_SIMPLE**</span></span>             | <span data-ttu-id="b6143-151">0x08000000L</span><span class="sxs-lookup"><span data-stu-id="b6143-151">0x08000000L</span></span> |
|                            | <span data-ttu-id="b6143-152">**STGM \_ Direct \_ SWMR**</span><span class="sxs-lookup"><span data-stu-id="b6143-152">**STGM\_DIRECT\_SWMR**</span></span>       | <span data-ttu-id="b6143-153">0x00400000L</span><span class="sxs-lookup"><span data-stu-id="b6143-153">0x00400000L</span></span> |
| <span data-ttu-id="b6143-154">Eliminar en la versión</span><span class="sxs-lookup"><span data-stu-id="b6143-154">Delete On Release</span></span>          | <span data-ttu-id="b6143-155">**STGM \_ DELETEONRELEASE**</span><span class="sxs-lookup"><span data-stu-id="b6143-155">**STGM\_DELETEONRELEASE**</span></span>    | <span data-ttu-id="b6143-156">0x04000000L</span><span class="sxs-lookup"><span data-stu-id="b6143-156">0x04000000L</span></span> |



 

<dl> <dt>

<span data-ttu-id="b6143-157"><span id="STGM_READ"></span><span id="stgm_read"></span>**STGM \_ lectura**</span><span class="sxs-lookup"><span data-stu-id="b6143-157"><span id="STGM_READ"></span><span id="stgm_read"></span>**STGM\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6143-158">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="b6143-158">0x00000000L</span></span>
</dt> <dt>



<span data-ttu-id="b6143-159">Indica que el objeto es de solo lectura, lo que significa que no se pueden realizar modificaciones.</span><span class="sxs-lookup"><span data-stu-id="b6143-159">Indicates that the object is read-only, meaning that modifications cannot be made.</span></span> <span data-ttu-id="b6143-160">Por ejemplo, si se abre un objeto de flujo con **STGM \_ Read**, se puede llamar al método [**ISequentialStream:: Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) , pero es posible que el método [**ISequentialStream:: Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) no lo sea.</span><span class="sxs-lookup"><span data-stu-id="b6143-160">For example, if a stream object is opened with **STGM\_READ**, the [**ISequentialStream::Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) method may be called, but the [**ISequentialStream::Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) method may not.</span></span> <span data-ttu-id="b6143-161">Del mismo modo, si se abre un objeto de almacenamiento con **STGM \_ Read**, se puede llamar a los métodos [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) y [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) , pero los métodos [**IStorage:: CreateStream (**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) y [**IStorage:: CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) no pueden.</span><span class="sxs-lookup"><span data-stu-id="b6143-161">Similarly, if a storage object opened with **STGM\_READ**, the [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) and [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) methods may be called, but the [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) and [**IStorage::CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) methods may not.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6143-162"><span id="STGM_WRITE"></span><span id="stgm_write"></span>**escritura de STGM \_**</span><span class="sxs-lookup"><span data-stu-id="b6143-162"><span id="STGM_WRITE"></span><span id="stgm_write"></span>**STGM\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6143-163">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="b6143-163">0x00000001L</span></span>
</dt> <dt>



<span data-ttu-id="b6143-164">Permite guardar los cambios realizados en el objeto, pero no permite el acceso a sus datos.</span><span class="sxs-lookup"><span data-stu-id="b6143-164">Enables you to save changes to the object, but does not permit access to its data.</span></span> <span data-ttu-id="b6143-165">Las implementaciones proporcionadas de las interfaces [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) y [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) no admiten este modo de solo escritura.</span><span class="sxs-lookup"><span data-stu-id="b6143-165">The provided implementations of the [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) and [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interfaces do not support this write-only mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6143-166"><span id="STGM_READWRITE"></span><span id="stgm_readwrite"></span>**STGM \_ ReadWrite**</span><span class="sxs-lookup"><span data-stu-id="b6143-166"><span id="STGM_READWRITE"></span><span id="stgm_readwrite"></span>**STGM\_READWRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6143-167">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="b6143-167">0x00000002L</span></span>
</dt> <dt>



<span data-ttu-id="b6143-168">Habilita el acceso y la modificación de los datos de objeto.</span><span class="sxs-lookup"><span data-stu-id="b6143-168">Enables access and modification of object data.</span></span> <span data-ttu-id="b6143-169">Por ejemplo, si se crea o se abre un objeto de flujo en este modo, es posible llamar a las dos [**IStream:: Read**](/windows/desktop/api/Objidl/nn-objidl-istream) y **IStream:: Write**.</span><span class="sxs-lookup"><span data-stu-id="b6143-169">For example, if a stream object is created or opened in this mode, it is possible to call both [**IStream::Read**](/windows/desktop/api/Objidl/nn-objidl-istream) and **IStream::Write**.</span></span> <span data-ttu-id="b6143-170">Tenga en cuenta que esta constante no es un simple binario **u** operación de los elementos **STGM \_ Write** y **STGM \_ Read** .</span><span class="sxs-lookup"><span data-stu-id="b6143-170">Be aware that this constant is not a simple binary **OR** operation of the **STGM\_WRITE** and **STGM\_READ** elements.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6143-171"><span id="STGM_SHARE_DENY_NONE"></span><span id="stgm_share_deny_none"></span>**STGM \_ recurso compartido \_ denegar \_ ninguno**</span><span class="sxs-lookup"><span data-stu-id="b6143-171"><span id="STGM_SHARE_DENY_NONE"></span><span id="stgm_share_deny_none"></span>**STGM\_SHARE\_DENY\_NONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6143-172">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="b6143-172">0x00000040L</span></span>
</dt> <dt>



<span data-ttu-id="b6143-173">Especifica que no se deniega el acceso de lectura o escritura a las aperturas posteriores del objeto.</span><span class="sxs-lookup"><span data-stu-id="b6143-173">Specifies that subsequent openings of the object are not denied read or write access.</span></span> <span data-ttu-id="b6143-174">Si no se especifica ninguna marca del grupo de uso compartido, se presupone esta marca.</span><span class="sxs-lookup"><span data-stu-id="b6143-174">If no flag from the sharing group is specified, this flag is assumed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6143-175"><span id="STGM_SHARE_DENY_READ"></span><span id="stgm_share_deny_read"></span>**STGM \_ recurso compartido de \_ lectura denegado \_**</span><span class="sxs-lookup"><span data-stu-id="b6143-175"><span id="STGM_SHARE_DENY_READ"></span><span id="stgm_share_deny_read"></span>**STGM\_SHARE\_DENY\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6143-176">0x00000030L</span><span class="sxs-lookup"><span data-stu-id="b6143-176">0x00000030L</span></span>
</dt> <dt>



<span data-ttu-id="b6143-177">Evita que otros usuarios abran posteriormente el objeto en el modo de **\_ lectura STGM** .</span><span class="sxs-lookup"><span data-stu-id="b6143-177">Prevents others from subsequently opening the object in **STGM\_READ** mode.</span></span> <span data-ttu-id="b6143-178">Normalmente se usa en un objeto de almacenamiento raíz.</span><span class="sxs-lookup"><span data-stu-id="b6143-178">It is typically used on a root storage object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6143-179"><span id="STGM_SHARE_DENY_WRITE"></span><span id="stgm_share_deny_write"></span>**STGM \_ recurso compartido \_ denegar \_ escritura**</span><span class="sxs-lookup"><span data-stu-id="b6143-179"><span id="STGM_SHARE_DENY_WRITE"></span><span id="stgm_share_deny_write"></span>**STGM\_SHARE\_DENY\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6143-180">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="b6143-180">0x00000020L</span></span>
</dt> <dt>



<span data-ttu-id="b6143-181">Evita que otros usuarios abran posteriormente el objeto para el acceso de **STGM \_ Write** o **STGM \_ ReadWrite** .</span><span class="sxs-lookup"><span data-stu-id="b6143-181">Prevents others from subsequently opening the object for **STGM\_WRITE** or **STGM\_READWRITE** access.</span></span> <span data-ttu-id="b6143-182">En el modo de transacción, el uso compartido de **STGM \_ share \_ denegar \_ escritura** o el **\_ recurso compartido de STGM \_ exclusivo** puede mejorar significativamente el rendimiento porque no requieren instantáneas.</span><span class="sxs-lookup"><span data-stu-id="b6143-182">In transacted mode, sharing of **STGM\_SHARE\_DENY\_WRITE** or **STGM\_SHARE\_EXCLUSIVE** can significantly improve performance because they do not require snapshots.</span></span> <span data-ttu-id="b6143-183">Para obtener más información sobre la transacción, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="b6143-183">For more information about transactioning, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6143-184"><span id="STGM_SHARE_EXCLUSIVE"></span><span id="stgm_share_exclusive"></span>**STGM \_ recurso compartido \_ exclusivo**</span><span class="sxs-lookup"><span data-stu-id="b6143-184"><span id="STGM_SHARE_EXCLUSIVE"></span><span id="stgm_share_exclusive"></span>**STGM\_SHARE\_EXCLUSIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6143-185">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="b6143-185">0x00000010L</span></span>
</dt> <dt>



<span data-ttu-id="b6143-186">Evita que otros usuarios abran posteriormente el objeto en cualquier modo.</span><span class="sxs-lookup"><span data-stu-id="b6143-186">Prevents others from subsequently opening the object in any mode.</span></span> <span data-ttu-id="b6143-187">Tenga en cuenta que este valor no es **una operación OR** bit a bit simple de los valores de lectura de los recursos compartidos **STGM \_ \_ \_ Read** y **STGM \_ share \_ Deny \_** .</span><span class="sxs-lookup"><span data-stu-id="b6143-187">Be aware that this value is not a simple bitwise **OR** operation of the **STGM\_SHARE\_DENY\_READ** and **STGM\_SHARE\_DENY\_WRITE** values.</span></span> <span data-ttu-id="b6143-188">En el modo de transacción, el uso compartido de **STGM \_ share \_ denegar \_ escritura** o el **\_ recurso compartido de STGM \_ exclusivo** puede mejorar significativamente el rendimiento porque no requieren instantáneas.</span><span class="sxs-lookup"><span data-stu-id="b6143-188">In transacted mode, sharing of **STGM\_SHARE\_DENY\_WRITE** or **STGM\_SHARE\_EXCLUSIVE** can significantly improve performance because they do not require snapshots.</span></span> <span data-ttu-id="b6143-189">Para obtener más información sobre la transacción, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="b6143-189">For more information about transactioning, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6143-190"><span id="STGM_PRIORITY"></span><span id="stgm_priority"></span>**prioridad de STGM \_**</span><span class="sxs-lookup"><span data-stu-id="b6143-190"><span id="STGM_PRIORITY"></span><span id="stgm_priority"></span>**STGM\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6143-191">0x00040000L</span><span class="sxs-lookup"><span data-stu-id="b6143-191">0x00040000L</span></span>
</dt> <dt>



<span data-ttu-id="b6143-192">Abre el objeto de almacenamiento con acceso exclusivo a la versión confirmada más recientemente.</span><span class="sxs-lookup"><span data-stu-id="b6143-192">Opens the storage object with exclusive access to the most recently committed version.</span></span> <span data-ttu-id="b6143-193">Por lo tanto, otros usuarios no pueden confirmar los cambios en el objeto mientras está abierto en modo de prioridad.</span><span class="sxs-lookup"><span data-stu-id="b6143-193">Thus, other users cannot commit changes to the object while you have it open in priority mode.</span></span> <span data-ttu-id="b6143-194">Obtiene ventajas de rendimiento para las operaciones de copia, pero impide que otros confirmen los cambios.</span><span class="sxs-lookup"><span data-stu-id="b6143-194">You gain performance benefits for copy operations, but you prevent others from committing changes.</span></span> <span data-ttu-id="b6143-195">Limite el tiempo que los objetos están abiertos en modo de prioridad.</span><span class="sxs-lookup"><span data-stu-id="b6143-195">Limit the time that objects are open in priority mode.</span></span> <span data-ttu-id="b6143-196">Debe especificar **STGM \_ Direct** y **STGM \_ Read** con el modo Priority y no puede especificar **STGM \_ DELETEONRELEASE**.</span><span class="sxs-lookup"><span data-stu-id="b6143-196">You must specify **STGM\_DIRECT** and **STGM\_READ** with priority mode, and you cannot specify **STGM\_DELETEONRELEASE**.</span></span> <span data-ttu-id="b6143-197">**STGM \_ DELETEONRELEASE** solo es válido cuando se crea un objeto raíz, como con [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex).</span><span class="sxs-lookup"><span data-stu-id="b6143-197">**STGM\_DELETEONRELEASE** is only valid when creating a root object, such as with [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex).</span></span> <span data-ttu-id="b6143-198">No es válido cuando se abre un objeto raíz existente, como con [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex).</span><span class="sxs-lookup"><span data-stu-id="b6143-198">It is not valid when opening an existing root object, such as with [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex).</span></span> <span data-ttu-id="b6143-199">Tampoco es válido al crear o abrir un subelemento, como con [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage).</span><span class="sxs-lookup"><span data-stu-id="b6143-199">It is also not valid when creating or opening a subelement, such as with [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6143-200"><span id="STGM_CREATE"></span><span id="stgm_create"></span>**\_crear STGM**</span><span class="sxs-lookup"><span data-stu-id="b6143-200"><span id="STGM_CREATE"></span><span id="stgm_create"></span>**STGM\_CREATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6143-201">0x00001000L</span><span class="sxs-lookup"><span data-stu-id="b6143-201">0x00001000L</span></span>
</dt> <dt>



<span data-ttu-id="b6143-202">Indica que se debe quitar un objeto o secuencia de almacenamiento existente antes de que el nuevo objeto lo reemplace.</span><span class="sxs-lookup"><span data-stu-id="b6143-202">Indicates that an existing storage object or stream should be removed before the new object replaces it.</span></span> <span data-ttu-id="b6143-203">Cuando se especifica este marcador, se crea un nuevo objeto solo si el objeto existente se ha quitado correctamente.</span><span class="sxs-lookup"><span data-stu-id="b6143-203">A new object is created when this flag is specified only if the existing object has been successfully removed.</span></span>

<span data-ttu-id="b6143-204">Esta marca se usa al intentar crear:</span><span class="sxs-lookup"><span data-stu-id="b6143-204">This flag is used when attempting to create:</span></span>

-   <span data-ttu-id="b6143-205">Un objeto de almacenamiento en un disco, pero existe un archivo con ese nombre.</span><span class="sxs-lookup"><span data-stu-id="b6143-205">A storage object on a disk, but a file of that name exists.</span></span>
-   <span data-ttu-id="b6143-206">Un objeto dentro de un objeto de almacenamiento, pero existe un objeto con el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="b6143-206">An object inside a storage object, but an object with the specified name exists.</span></span>
-   <span data-ttu-id="b6143-207">Objeto de matriz de bytes, pero existe uno con el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="b6143-207">A byte array object, but one with the specified name exists.</span></span>

<span data-ttu-id="b6143-208">Esta marca no se puede usar con operaciones de apertura, como [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) o [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream).</span><span class="sxs-lookup"><span data-stu-id="b6143-208">This flag cannot be used with open operations, such as [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) or [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6143-209"><span id="STGM_CONVERT"></span><span id="stgm_convert"></span>**STGM \_ convertir**</span><span class="sxs-lookup"><span data-stu-id="b6143-209"><span id="STGM_CONVERT"></span><span id="stgm_convert"></span>**STGM\_CONVERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6143-210">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="b6143-210">0x00020000L</span></span>
</dt> <dt>



<span data-ttu-id="b6143-211">Crea el nuevo objeto conservando los datos existentes en una secuencia denominada "contents".</span><span class="sxs-lookup"><span data-stu-id="b6143-211">Creates the new object while preserving existing data in a stream named "Contents".</span></span> <span data-ttu-id="b6143-212">En el caso de un objeto de almacenamiento o una matriz de bytes, se da formato a los datos antiguos en una secuencia, independientemente de si el archivo o la matriz de bytes existentes contiene actualmente un objeto de almacenamiento en capas.</span><span class="sxs-lookup"><span data-stu-id="b6143-212">In the case of a storage object or a byte array, the old data is formatted into a stream regardless of whether the existing file or byte array currently contains a layered storage object.</span></span> <span data-ttu-id="b6143-213">Esta marca solo se puede usar al crear un objeto de almacenamiento raíz.</span><span class="sxs-lookup"><span data-stu-id="b6143-213">This flag can only be used when creating a root storage object.</span></span> <span data-ttu-id="b6143-214">No se puede usar dentro de un objeto de almacenamiento. por ejemplo, en [**IStorage:: CreateStream (**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span><span class="sxs-lookup"><span data-stu-id="b6143-214">It cannot be used within a storage object; for example, in [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span></span> <span data-ttu-id="b6143-215">Tampoco es válido usar esta marca y la marca **STGM \_ DELETEONRELEASE** simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="b6143-215">It is also not valid to use this flag and the **STGM\_DELETEONRELEASE** flag simultaneously.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6143-216"><span id="STGM_FAILIFTHERE"></span><span id="stgm_failifthere"></span>**STGM \_ FAILIFTHERE**</span><span class="sxs-lookup"><span data-stu-id="b6143-216"><span id="STGM_FAILIFTHERE"></span><span id="stgm_failifthere"></span>**STGM\_FAILIFTHERE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6143-217">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="b6143-217">0x00000000L</span></span>
</dt> <dt>



<span data-ttu-id="b6143-218">Hace que se produzca un error en la operación de creación si existe un objeto con el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="b6143-218">Causes the create operation to fail if an existing object with the specified name exists.</span></span> <span data-ttu-id="b6143-219">En este caso, se devuelve **STG \_ E \_ FILEALREADYEXISTS** .</span><span class="sxs-lookup"><span data-stu-id="b6143-219">In this case, **STG\_E\_FILEALREADYEXISTS** is returned.</span></span> <span data-ttu-id="b6143-220">Este es el modo de creación predeterminado; es decir, si no se especifica ninguna otra marca Create, se implica **STGM \_ FAILIFTHERE** .</span><span class="sxs-lookup"><span data-stu-id="b6143-220">This is the default creation mode; that is, if no other create flag is specified, **STGM\_FAILIFTHERE** is implied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6143-221"><span id="STGM_DIRECT"></span><span id="stgm_direct"></span>**STGM \_ directo**</span><span class="sxs-lookup"><span data-stu-id="b6143-221"><span id="STGM_DIRECT"></span><span id="stgm_direct"></span>**STGM\_DIRECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6143-222">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="b6143-222">0x00000000L</span></span>
</dt> <dt>



<span data-ttu-id="b6143-223">Indica que, en modo directo, cada cambio en un elemento de almacenamiento o de secuencia se escribe a medida que se produce.</span><span class="sxs-lookup"><span data-stu-id="b6143-223">Indicates that, in direct mode, each change to a storage or stream element is written as it occurs.</span></span> <span data-ttu-id="b6143-224">Este es el valor predeterminado si no se especifica **STGM \_ Direct** ni **STGM \_ transaccionad** .</span><span class="sxs-lookup"><span data-stu-id="b6143-224">This is the default if neither **STGM\_DIRECT** nor **STGM\_TRANSACTED** is specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6143-225"><span id="STGM_TRANSACTED"></span><span id="stgm_transacted"></span>**STGM \_ transacción**</span><span class="sxs-lookup"><span data-stu-id="b6143-225"><span id="STGM_TRANSACTED"></span><span id="stgm_transacted"></span>**STGM\_TRANSACTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6143-226">0x00010000L</span><span class="sxs-lookup"><span data-stu-id="b6143-226">0x00010000L</span></span>
</dt> <dt>



<span data-ttu-id="b6143-227">Indica que, en el modo de transacción, los cambios se almacenan en búfer y se escriben solo si se llama a una operación de confirmación explícita.</span><span class="sxs-lookup"><span data-stu-id="b6143-227">Indicates that, in transacted mode, changes are buffered and written only if an explicit commit operation is called.</span></span> <span data-ttu-id="b6143-228">Para omitir los cambios, llame al método [**Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert) en la interfaz [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)o [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) .</span><span class="sxs-lookup"><span data-stu-id="b6143-228">To ignore the changes, call the [**Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert) method in the [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), or [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interface.</span></span> <span data-ttu-id="b6143-229">La implementación de archivo compuesto COM de **IStorage** no admite secuencias de transacción, lo que significa que las secuencias solo se pueden abrir en modo directo, y no se pueden revertir los cambios en ellas, pero se admiten los almacenamientos de transacciones.</span><span class="sxs-lookup"><span data-stu-id="b6143-229">The COM compound file implementation of **IStorage** does not support transacted streams, which means that streams can be opened only in direct mode, and you cannot revert changes to them, however transacted storages are supported.</span></span> <span data-ttu-id="b6143-230">Las implementaciones de archivos compuestos, independientes y del sistema de archivos NTFS de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) de forma similar no admiten conjuntos de propiedades con transacciones simples, ya que estos conjuntos de propiedades se almacenan en secuencias.</span><span class="sxs-lookup"><span data-stu-id="b6143-230">The compound file, stand-alone, and NTFS file system implementations of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) similarly do not support transacted, simple property sets because these property sets are stored in streams.</span></span> <span data-ttu-id="b6143-231">Sin embargo, se admite la transacción de conjuntos de propiedades no simples, que se pueden crear especificando la marca **PROPSETFLAG \_ nonsimple** en el parámetro *grfFlags* de [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create).</span><span class="sxs-lookup"><span data-stu-id="b6143-231">However, transactioning of nonsimple property sets, which can be created by specifying the **PROPSETFLAG\_NONSIMPLE** flag in the *grfFlags* parameter of [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create), are supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6143-232"><span id="STGM_NOSCRATCH"></span><span id="stgm_noscratch"></span>**STGM \_ NOscratch**</span><span class="sxs-lookup"><span data-stu-id="b6143-232"><span id="STGM_NOSCRATCH"></span><span id="stgm_noscratch"></span>**STGM\_NOSCRATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6143-233">0x00100000L</span><span class="sxs-lookup"><span data-stu-id="b6143-233">0x00100000L</span></span>
</dt> <dt>



<span data-ttu-id="b6143-234">Indica que, en el modo de transacción, normalmente se utiliza un archivo temporal temporal para guardar las modificaciones hasta que se llama al método **commit** .</span><span class="sxs-lookup"><span data-stu-id="b6143-234">Indicates that, in transacted mode, a temporary scratch file is usually used to save modifications until the **Commit** method is called.</span></span> <span data-ttu-id="b6143-235">La especificación de **STGM \_ noscratch** permite que la parte no utilizada del archivo original se use como espacio de trabajo en lugar de crear un nuevo archivo para ese propósito.</span><span class="sxs-lookup"><span data-stu-id="b6143-235">Specifying **STGM\_NOSCRATCH** permits the unused portion of the original file to be used as work space instead of creating a new file for that purpose.</span></span> <span data-ttu-id="b6143-236">Esto no afecta a los datos del archivo original y, en algunos casos, puede mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="b6143-236">This does not affect the data in the original file, and in certain cases can result in improved performance.</span></span> <span data-ttu-id="b6143-237">No es válido especificar esta marca sin especificar también **STGM \_ transacción**, y esta marca solo se puede usar en una raíz abierta.</span><span class="sxs-lookup"><span data-stu-id="b6143-237">It is not valid to specify this flag without also specifying **STGM\_TRANSACTED**, and this flag may only be used in a root open.</span></span> <span data-ttu-id="b6143-238">Para obtener más información sobre el modo noscratch, consulte la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="b6143-238">For more information about NoScratch mode, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6143-239"><span id="STGM_NOSNAPSHOT"></span><span id="stgm_nosnapshot"></span>**STGM \_ NOsnapshot**</span><span class="sxs-lookup"><span data-stu-id="b6143-239"><span id="STGM_NOSNAPSHOT"></span><span id="stgm_nosnapshot"></span>**STGM\_NOSNAPSHOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6143-240">0x00200000L</span><span class="sxs-lookup"><span data-stu-id="b6143-240">0x00200000L</span></span>
</dt> <dt>



<span data-ttu-id="b6143-241">Esta marca se usa al abrir un objeto de almacenamiento con **STGM \_ transaccionad** y sin **STGM \_ share \_** or **STGM \_ share \_ Deny \_ Write**.</span><span class="sxs-lookup"><span data-stu-id="b6143-241">This flag is used when opening a storage object with **STGM\_TRANSACTED** and without **STGM\_SHARE\_EXCLUSIVE** or **STGM\_SHARE\_DENY\_WRITE**.</span></span> <span data-ttu-id="b6143-242">En este caso, la especificación de **STGM \_ nosnapshot** evita que la implementación proporcionada por el sistema cree una copia de instantánea del archivo.</span><span class="sxs-lookup"><span data-stu-id="b6143-242">In this case, specifying **STGM\_NOSNAPSHOT** prevents the system-provided implementation from creating a snapshot copy of the file.</span></span> <span data-ttu-id="b6143-243">En su lugar, los cambios realizados en el archivo se escriben al final del archivo.</span><span class="sxs-lookup"><span data-stu-id="b6143-243">Instead, changes to the file are written to the end of the file.</span></span> <span data-ttu-id="b6143-244">No se recupera el espacio no utilizado a menos que se realice la consolidación durante la confirmación, y solo hay un escritor actual en el archivo.</span><span class="sxs-lookup"><span data-stu-id="b6143-244">Unused space is not reclaimed unless consolidation is performed during the commit, and there is only one current writer on the file.</span></span> <span data-ttu-id="b6143-245">Cuando el archivo se abre en modo sin instantánea, no se puede realizar otra operación de apertura sin especificar **STGM \_ nosnapshot**.</span><span class="sxs-lookup"><span data-stu-id="b6143-245">When the file is opened in no snapshot mode, another open operation cannot be performed without specifying **STGM\_NOSNAPSHOT**.</span></span> <span data-ttu-id="b6143-246">Esta marca solo se puede usar en una operación de apertura raíz.</span><span class="sxs-lookup"><span data-stu-id="b6143-246">This flag may only be used in a root open operation.</span></span> <span data-ttu-id="b6143-247">Para obtener más información sobre el modo nosnapshot, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="b6143-247">For more information about NoSnapshot mode, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6143-248"><span id="STGM_SIMPLE"></span><span id="stgm_simple"></span>**STGM \_ simple**</span><span class="sxs-lookup"><span data-stu-id="b6143-248"><span id="STGM_SIMPLE"></span><span id="stgm_simple"></span>**STGM\_SIMPLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6143-249">0x08000000L</span><span class="sxs-lookup"><span data-stu-id="b6143-249">0x08000000L</span></span>
</dt> <dt>



<span data-ttu-id="b6143-250">Proporciona una implementación más rápida de un archivo compuesto en un caso limitado, pero que se usa con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="b6143-250">Provides a faster implementation of a compound file in a limited, but frequently used, case.</span></span> <span data-ttu-id="b6143-251">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="b6143-251">For more information, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6143-252"><span id="STGM_DIRECT_SWMR"></span><span id="stgm_direct_swmr"></span>**STGM \_ Direct \_ SWMR**</span><span class="sxs-lookup"><span data-stu-id="b6143-252"><span id="STGM_DIRECT_SWMR"></span><span id="stgm_direct_swmr"></span>**STGM\_DIRECT\_SWMR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6143-253">0x00400000L</span><span class="sxs-lookup"><span data-stu-id="b6143-253">0x00400000L</span></span>
</dt> <dt>



<span data-ttu-id="b6143-254">Admite el modo directo para las operaciones de archivo de un solo escritor.</span><span class="sxs-lookup"><span data-stu-id="b6143-254">Supports direct mode for single-writer, multireader file operations.</span></span> <span data-ttu-id="b6143-255">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="b6143-255">For more information, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6143-256"><span id="STGM_DELETEONRELEASE"></span><span id="stgm_deleteonrelease"></span>**STGM \_ DELETEONRELEASE**</span><span class="sxs-lookup"><span data-stu-id="b6143-256"><span id="STGM_DELETEONRELEASE"></span><span id="stgm_deleteonrelease"></span>**STGM\_DELETEONRELEASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6143-257">0x04000000L</span><span class="sxs-lookup"><span data-stu-id="b6143-257">0x04000000L</span></span>
</dt> <dt>



<span data-ttu-id="b6143-258">Indica que el archivo subyacente se va a destruir automáticamente cuando se libere el objeto de almacenamiento raíz.</span><span class="sxs-lookup"><span data-stu-id="b6143-258">Indicates that the underlying file is to be automatically destroyed when the root storage object is released.</span></span> <span data-ttu-id="b6143-259">Esta característica es muy útil para crear archivos temporales.</span><span class="sxs-lookup"><span data-stu-id="b6143-259">This feature is most useful for creating temporary files.</span></span> <span data-ttu-id="b6143-260">Esta marca solo se puede usar al crear un objeto raíz, como con [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex).</span><span class="sxs-lookup"><span data-stu-id="b6143-260">This flag can only be used when creating a root object, such as with [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex).</span></span> <span data-ttu-id="b6143-261">No es válido al abrir un objeto raíz, como con [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex), o al crear o abrir un subelemento, como con [**IStorage:: CreateStream (**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span><span class="sxs-lookup"><span data-stu-id="b6143-261">It is not valid when opening a root object, such as with [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex), or when creating or opening a subelement, such as with [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span></span> <span data-ttu-id="b6143-262">Tampoco es válido usar esta marca y la marca de conversión STGM \_ simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="b6143-262">It is also not valid to use this flag and the STGM\_CONVERT flag simultaneously.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b6143-263">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b6143-263">Remarks</span></span>

<span data-ttu-id="b6143-264">Puede combinar estas marcas, pero solo puede elegir una marca de cada grupo de marcas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="b6143-264">You can combine these flags, but you can only choose one flag from each group of related flags.</span></span> <span data-ttu-id="b6143-265">Normalmente se debe especificar una marca de cada uno de los grupos de acceso y uso compartido para todas las funciones y métodos que usan estas constantes.</span><span class="sxs-lookup"><span data-stu-id="b6143-265">Typically one flag from each of the access and sharing groups must be specified for all functions and methods which use these constants.</span></span> <span data-ttu-id="b6143-266">Las marcas de otros grupos son opcionales.</span><span class="sxs-lookup"><span data-stu-id="b6143-266">Flags from other groups are optional.</span></span>

### <a name="transacted-mode"></a><span data-ttu-id="b6143-267">Modo de transacción</span><span class="sxs-lookup"><span data-stu-id="b6143-267">Transacted Mode</span></span>

<span data-ttu-id="b6143-268">Cuando se especifica la marca **STGM \_ Direct**, solo se puede especificar una de las siguientes combinaciones de marcas de los grupos de acceso y uso compartido.</span><span class="sxs-lookup"><span data-stu-id="b6143-268">When the **STGM\_DIRECT** flag is specified, only one of the following combination of flags may be specified from the access and sharing groups.</span></span>

``` syntax
    STGM_READ      | STGM_SHARE_DENY_WRITE
```

``` syntax
    STGM_READWRITE | STGM_SHARE_EXCLUSIVE
```

``` syntax
    STGM_READ      | STGM_PRIORITY
```

<span data-ttu-id="b6143-269">Tenga en cuenta que el modo directo está implicado por la ausencia de **STGM \_ transacción**.</span><span class="sxs-lookup"><span data-stu-id="b6143-269">Be aware that direct mode is implied by the absence of **STGM\_TRANSACTED**.</span></span> <span data-ttu-id="b6143-270">Es decir, si no se especifica **STGM \_ Direct** ni **STGM \_ transaccionad** , se supone **STGM \_ Direct** .</span><span class="sxs-lookup"><span data-stu-id="b6143-270">That is, if neither **STGM\_DIRECT** nor **STGM\_TRANSACTED** is specified, **STGM\_DIRECT** is assumed.</span></span>

<span data-ttu-id="b6143-271">Cuando se especifica la marca de **\_ transacción STGM** , los objetos se crean o se abren en modo de transacción.</span><span class="sxs-lookup"><span data-stu-id="b6143-271">When the **STGM\_TRANSACTED** flag is specified, objects are created or opened in transacted mode.</span></span> <span data-ttu-id="b6143-272">En este modo, los cambios realizados en un objeto no se conservan hasta que se confirman.</span><span class="sxs-lookup"><span data-stu-id="b6143-272">In this mode, changes to an object do not persist until they are committed.</span></span> <span data-ttu-id="b6143-273">Por ejemplo, los cambios en un objeto de almacenamiento con transacciones no se conservan hasta que se llama al método [**IStorage:: commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) .</span><span class="sxs-lookup"><span data-stu-id="b6143-273">For example, changes to a transacted storage object are not persisted until the [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) method is called.</span></span> <span data-ttu-id="b6143-274">Los cambios en este tipo de objeto de almacenamiento se perderán si se libera el objeto de almacenamiento (versión final) antes de que se llame al método **commit** , o bien, si se llama al método [**IStorage:: Revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert) .</span><span class="sxs-lookup"><span data-stu-id="b6143-274">Changes to such a storage object will be lost if the storage object is released (final release) before the **Commit** method is called, or if the [**IStorage::Revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert) method is called.</span></span>

<span data-ttu-id="b6143-275">Cuando se crea o se abre un objeto en modo de transacción, la implementación debe conservar los datos originales y las actualizaciones de estos datos, de modo que las actualizaciones se puedan revertir si es necesario.</span><span class="sxs-lookup"><span data-stu-id="b6143-275">When an object is created or opened in transacted mode, the implementation must keep both the original data and updates to this data, so that updates can be reverted if necessary.</span></span> <span data-ttu-id="b6143-276">Normalmente, esto se realiza mediante la escritura de cambios en un área de borrador hasta que se confirman, o bien mediante la creación de una copia, denominada instantánea, de los datos confirmados más recientemente.</span><span class="sxs-lookup"><span data-stu-id="b6143-276">This is typically performed by writing changes to a scratch area until they are committed, or by creating a copy, called a snapshot, of the most recently committed data.</span></span>

<span data-ttu-id="b6143-277">Cuando se abre un objeto de almacenamiento raíz en modo de transacción, la ubicación y el comportamiento de los datos Scratch y las copias de instantáneas se pueden controlar para optimizar el rendimiento con las marcas **\_ noscratch** y **STGM \_ nosnapshot** de STGM.</span><span class="sxs-lookup"><span data-stu-id="b6143-277">When a root storage object is opened in transacted mode, the location and behavior of the scratch data and the snapshot copies can be controlled to optimize performance with the **STGM\_NOSCRATCH** and **STGM\_NOSNAPSHOT** flags.</span></span> <span data-ttu-id="b6143-278">(Un objeto de almacenamiento raíz se obtiene de, por ejemplo, la función [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) ; un objeto de almacenamiento obtenido del método [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) es un objeto de subalmacenamiento). Normalmente, los datos y las instantáneas temporales se almacenan en archivos temporales, independientes del almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="b6143-278">(A root storage object is obtained from, for example, the [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) function; a storage object obtained from the [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) method is a substorage object.) Typically, the scratch data and snapshots are stored in temporary files, separate from the storage.</span></span>

<span data-ttu-id="b6143-279">El efecto de estas marcas depende del número de lectores o escritores que tengan acceso al almacenamiento raíz.</span><span class="sxs-lookup"><span data-stu-id="b6143-279">The effect of these flags depends on the number of readers and/or writers accessing the root storage.</span></span>

<span data-ttu-id="b6143-280">En el caso de "un solo escritor", se abre un objeto de almacenamiento en modo de transacción para el acceso de escritura y no puede haber ningún otro acceso al archivo.</span><span class="sxs-lookup"><span data-stu-id="b6143-280">In the "single-writer" case, a transacted mode storage object is opened for write access and there can be no other access to the file.</span></span> <span data-ttu-id="b6143-281">Es decir, el archivo se abre con **STGM \_ transaccionad**, Access of **STGM \_ Write** o **STGM \_ ReadWrite** y el uso compartido de **STGM \_ share \_ Exclusive**.</span><span class="sxs-lookup"><span data-stu-id="b6143-281">That is, the file is opened with **STGM\_TRANSACTED**, access of **STGM\_WRITE** or **STGM\_READWRITE**, and sharing of **STGM\_SHARE\_EXCLUSIVE**.</span></span> <span data-ttu-id="b6143-282">En este caso, los cambios en el objeto de almacenamiento se escriben en el área de borrado.</span><span class="sxs-lookup"><span data-stu-id="b6143-282">In this case, changes to the storage object are written to the scratch area.</span></span> <span data-ttu-id="b6143-283">Cuando estos cambios se confirman, se copian en el almacenamiento original.</span><span class="sxs-lookup"><span data-stu-id="b6143-283">When those changes are committed, they are copied to the original storage.</span></span> <span data-ttu-id="b6143-284">Por lo tanto, si no se realiza ningún cambio realmente en el objeto de almacenamiento, no habrá ninguna transferencia de datos innecesaria.</span><span class="sxs-lookup"><span data-stu-id="b6143-284">Therefore, if no changes are actually made to the storage object, there will be no unnecessary data transfer.</span></span>

<span data-ttu-id="b6143-285">En el caso de "varios escritores", se abre un objeto de almacenamiento con transacciones para el acceso de escritura, pero se comparte en tal asway como para permitir otros escritores.</span><span class="sxs-lookup"><span data-stu-id="b6143-285">In the "multiple-writer" case, a transacted storage object is opened for write access, but is shared in such asway as to allow other writers.</span></span> <span data-ttu-id="b6143-286">Es decir, el objeto de almacenamiento se abre **con \_ STGM transaccionad**, Access of **STGM \_ Write** o **STGM \_ ReadWrite** y el uso compartido de **STGM \_ share \_ Deny \_ Read**.</span><span class="sxs-lookup"><span data-stu-id="b6143-286">That is, the storage object is opened with **STGM\_TRANSACTED**, access of **STGM\_WRITE** or **STGM\_READWRITE**, and sharing of **STGM\_SHARE\_DENY\_READ**.</span></span> <span data-ttu-id="b6143-287">Si en su lugar se especifica el uso compartido del **\_ recurso compartido STGM \_ denegar \_ ninguno** , el caso sería "varios escritores, varios lectores".</span><span class="sxs-lookup"><span data-stu-id="b6143-287">If sharing of **STGM\_SHARE\_DENY\_NONE** is specified instead, then the case is "multiple-writer, multiple-reader".</span></span> <span data-ttu-id="b6143-288">En estos casos, se realizará una instantánea de los datos originales durante la operación de apertura.</span><span class="sxs-lookup"><span data-stu-id="b6143-288">In these cases, a snapshot of the original data will be made during the open operation.</span></span> <span data-ttu-id="b6143-289">Por lo tanto, incluso si no se realiza ningún cambio en el almacenamiento y/o no se abre realmente por otro escritor simultáneamente, la transferencia de datos sigue siendo necesaria durante la apertura.</span><span class="sxs-lookup"><span data-stu-id="b6143-289">Therefore, even if no changes are actually made to the storage and/or it is not actually opened by another writer simultaneously, data transfer is still necessary during the open.</span></span> <span data-ttu-id="b6143-290">Como resultado, se puede obtener el mejor rendimiento en tiempo de ejecución abriendo el objeto de almacenamiento en los modos **STGM \_ share \_ Deny \_ Write** o **STGM \_ share \_** .</span><span class="sxs-lookup"><span data-stu-id="b6143-290">As a result the best open-time performance can be obtained by opening the storage object in **STGM\_SHARE\_DENY\_WRITE** or **STGM\_SHARE\_EXCLUSIVE** modes.</span></span> <span data-ttu-id="b6143-291">Para obtener más información sobre cómo se confirman los cambios cuando hay varios escritores, vea [**IStorage:: commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit).</span><span class="sxs-lookup"><span data-stu-id="b6143-291">For more information about how changes are committed when there are multiple writers, see [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit).</span></span>

<span data-ttu-id="b6143-292">En el caso de "un solo escritor, varios lectores", se abre un objeto de almacenamiento con transacciones para el acceso de escritura, pero se comparte con los lectores.</span><span class="sxs-lookup"><span data-stu-id="b6143-292">In the "single-writer, multiple-reader" case, a transacted storage object is opened for write access, but is shared with readers.</span></span> <span data-ttu-id="b6143-293">Es decir, el escritor abre el objeto de almacenamiento con **STGM \_ transaccionad**, el acceso **de STGM \_ ReadWrite** o **STGM \_ Write** y el uso compartido de **STGM \_ share \_ Deny \_ Write**.</span><span class="sxs-lookup"><span data-stu-id="b6143-293">That is, the storage object is opened by the writer with **STGM\_TRANSACTED**, access of **STGM\_READWRITE** or **STGM\_WRITE**, and sharing of **STGM\_SHARE\_DENY\_WRITE**.</span></span> <span data-ttu-id="b6143-294">Los lectores abren el almacenamiento con **\_ transacciones de STGM**, el acceso de **STGM \_ Read** y el uso compartido **del \_ recurso compartido STGM no \_ deniega \_ ninguno**.</span><span class="sxs-lookup"><span data-stu-id="b6143-294">The storage is opened by readers with **STGM\_TRANSACTED**, access of **STGM\_READ**, and sharing of **STGM\_SHARE\_DENY\_NONE**.</span></span> <span data-ttu-id="b6143-295">En este caso, el escritor usa el área de borrado para almacenar los cambios no confirmados.</span><span class="sxs-lookup"><span data-stu-id="b6143-295">In this case the writer uses the scratch area to store uncommitted changes.</span></span> <span data-ttu-id="b6143-296">Como en los casos anteriores, el lector incurre en una penalización de rendimiento de tiempo abierto mientras se crea una copia de instantánea de los datos.</span><span class="sxs-lookup"><span data-stu-id="b6143-296">As in the cases above, the reader incurs an open-time performance penalty while a snapshot copy of the data is created.</span></span>

<span data-ttu-id="b6143-297">Normalmente, el área de borrado es un archivo temporal, independiente de los datos originales.</span><span class="sxs-lookup"><span data-stu-id="b6143-297">Typically, the scratch area is a temporary file, separate from the original data.</span></span> <span data-ttu-id="b6143-298">Cuando los cambios se confirman en el archivo original, los datos se deben transferir desde el archivo temporal.</span><span class="sxs-lookup"><span data-stu-id="b6143-298">When changes are committed to the original file, the data must be transferred from the temporary file.</span></span> <span data-ttu-id="b6143-299">Para evitar esta transferencia de datos, se puede especificar la marca **STGM \_ noscratch**.</span><span class="sxs-lookup"><span data-stu-id="b6143-299">To avoid this data transfer, the **STGM\_NOSCRATCH** flag may be specified.</span></span> <span data-ttu-id="b6143-300">Cuando se especifica esta marca, se usan partes del archivo de objeto de almacenamiento para el área de borrado, en lugar de un archivo temporal independiente.</span><span class="sxs-lookup"><span data-stu-id="b6143-300">When this flag is specified, portions of the storage object file are used for the scratch area, rather than a separate temporary file.</span></span> <span data-ttu-id="b6143-301">Como resultado, la confirmación de los cambios puede realizarse rápidamente, ya que se requiere poca transferencia de datos.</span><span class="sxs-lookup"><span data-stu-id="b6143-301">As a result, committing changes can be performed quickly, because little data transfer is required.</span></span> <span data-ttu-id="b6143-302">El inconveniente es que el archivo de almacenamiento puede ser mayor de lo que, en caso contrario, debe aumentarse para que sea lo suficientemente grande como para los datos originales y el área de borrado.</span><span class="sxs-lookup"><span data-stu-id="b6143-302">The disadvantage is that the storage file can become larger than it would otherwise be, because it must be grown to be large enough for both the original data and the scratch area.</span></span> <span data-ttu-id="b6143-303">Para consolidar los datos y quitar este área innecesaria, vuelva a abrir el almacenamiento raíz en modo de transacción, pero sin establecer la marca **STGM \_ noscratch** .</span><span class="sxs-lookup"><span data-stu-id="b6143-303">To consolidate the data and remove this unnecessary area, reopen the root storage in transacted mode, but without setting the **STGM\_NOSCRATCH** flag.</span></span> <span data-ttu-id="b6143-304">A continuación, llame a [**IStorage:: commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) con el marcador de **STGC \_ ConsoliDate** establecido.</span><span class="sxs-lookup"><span data-stu-id="b6143-304">Then, call [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) with the **STGC\_CONSOLIDATE** flag set.</span></span>

<span data-ttu-id="b6143-305">El área de instantáneas, como el área de borrador, también es, normalmente, un archivo temporal, y esto también puede verse afectado por una marca STGM.</span><span class="sxs-lookup"><span data-stu-id="b6143-305">The snapshot area, like the scratch area, is also, typically, a temporary file, and this too can be affected with a STGM flag.</span></span> <span data-ttu-id="b6143-306">Al especificar la marca **STGM \_ nosnapshot** , no se crea un archivo de instantánea temporal independiente.</span><span class="sxs-lookup"><span data-stu-id="b6143-306">By specifying the **STGM\_NOSNAPSHOT** flag, a separate temporary snapshot file is not created.</span></span> <span data-ttu-id="b6143-307">En su lugar, los datos originales nunca se modifican, incluso si hay uno o más escritores por objeto.</span><span class="sxs-lookup"><span data-stu-id="b6143-307">Instead, the original data is never modified, even if there are one or more writers per object.</span></span> <span data-ttu-id="b6143-308">Cuando se confirman los cambios, se agregan al archivo, pero los datos originales permanecen intactos.</span><span class="sxs-lookup"><span data-stu-id="b6143-308">When changes are committed, they are added to the file, but the original data remains intact.</span></span> <span data-ttu-id="b6143-309">Este modo aumenta la eficacia, ya que reduce el tiempo de ejecución eliminando el requisito de crear una instantánea durante la operación de apertura.</span><span class="sxs-lookup"><span data-stu-id="b6143-309">This mode increases efficiency because it reduces run time by eliminating the requirement of creating a snapshot during the open operation.</span></span> <span data-ttu-id="b6143-310">Sin embargo, el uso de este modo puede dar lugar a un archivo de almacenamiento muy grande, ya que los datos del archivo no se pueden sobrescribir nunca.</span><span class="sxs-lookup"><span data-stu-id="b6143-310">However, using this mode may result in a very large storage file because data in the file can never be overwritten.</span></span> <span data-ttu-id="b6143-311">No es límite para el tamaño de los archivos abiertos en el modo nosnapshot.</span><span class="sxs-lookup"><span data-stu-id="b6143-311">This is no limit to the size of files opened in NoSnapshot mode.</span></span>

### <a name="direct-single-writer-multiple-reader-mode"></a><span data-ttu-id="b6143-312">Un solo escritor directo, modo de Multiple-Reader</span><span class="sxs-lookup"><span data-stu-id="b6143-312">Direct Single-Writer, Multiple-Reader Mode</span></span>

<span data-ttu-id="b6143-313">Tal como se describe, es posible tener un solo escritor y varios lectores de un objeto de almacenamiento, si ese objeto está abierto en modo de transacción.</span><span class="sxs-lookup"><span data-stu-id="b6143-313">As described, it is possible to have a single writer and multiple readers of a storage object, if that object is opened in transacted mode.</span></span> <span data-ttu-id="b6143-314">También es posible lograr el caso de un solo escritor y MultiRead en modo directo, especificando la marca **STGM \_ Direct \_ SWMR** .</span><span class="sxs-lookup"><span data-stu-id="b6143-314">It is also possible to achieve the single-writer, multireader case in direct mode, by specifying the **STGM\_DIRECT\_SWMR** flag.</span></span>

<span data-ttu-id="b6143-315">En el modo **STGM \_ Direct \_ SWMR** , es posible que un llamador abra un objeto para el acceso de lectura y escritura, mientras que otros llamadores tienen el archivo abierto al mismo tiempo para el acceso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b6143-315">In **STGM\_DIRECT\_SWMR** mode, it is possible for one caller to open an object for read/write access, while other callers simultaneously have the file open for read-only access.</span></span> <span data-ttu-id="b6143-316">No es válido usar esta marca en combinación con la marca de **\_ transacción STGM** .</span><span class="sxs-lookup"><span data-stu-id="b6143-316">It is not valid to use this flag in combination with the **STGM\_TRANSACTED** flag.</span></span> <span data-ttu-id="b6143-317">En este modo, el escritor abre el objeto con las marcas siguientes:</span><span class="sxs-lookup"><span data-stu-id="b6143-317">In this mode, the writer opens the object with the following flags:</span></span>

<span data-ttu-id="b6143-318">**STGM \_ Direct \_ SWMR** \| **STGM \_ ReadWrite** \| **STGM \_ recurso compartido \_ DENYWRITE**</span><span class="sxs-lookup"><span data-stu-id="b6143-318">**STGM\_DIRECT\_SWMR** \| **STGM\_READWRITE** \| **STGM\_SHARE\_DENYWRITE**</span></span>

<span data-ttu-id="b6143-319">y cada uno de los lectores abre el objeto con estas marcas:</span><span class="sxs-lookup"><span data-stu-id="b6143-319">and each of the readers opens the object with these flags:</span></span>

<span data-ttu-id="b6143-320">**STGM \_ Direct \_ SWMR** \| **STGM \_ Read** \| **STGM \_ share \_ denegar \_ ninguno**</span><span class="sxs-lookup"><span data-stu-id="b6143-320">**STGM\_DIRECT\_SWMR** \| **STGM\_READ** \| **STGM\_SHARE\_DENY\_NONE**</span></span>

<span data-ttu-id="b6143-321">En este modo, para modificar el objeto de almacenamiento, el escritor debe obtener acceso exclusivo al objeto.</span><span class="sxs-lookup"><span data-stu-id="b6143-321">In this mode, to modify the storage object, the writer must get exclusive access to the object.</span></span> <span data-ttu-id="b6143-322">Esto es posible cuando todos los lectores la han cerrado.</span><span class="sxs-lookup"><span data-stu-id="b6143-322">This is possible when all the readers have closed it.</span></span> <span data-ttu-id="b6143-323">El escritor usa la interfaz [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) para obtener este acceso exclusivo.</span><span class="sxs-lookup"><span data-stu-id="b6143-323">The writer uses the [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) interface to obtain this exclusive access.</span></span>

### <a name="simple-mode"></a><span data-ttu-id="b6143-324">Modo simple</span><span class="sxs-lookup"><span data-stu-id="b6143-324">Simple Mode</span></span>

<span data-ttu-id="b6143-325">El modo simple (**STGM \_ simple**) es útil para las aplicaciones que realizan operaciones de guardado completas.</span><span class="sxs-lookup"><span data-stu-id="b6143-325">Simple mode (**STGM\_SIMPLE**) is useful for applications that perform complete save operations.</span></span> <span data-ttu-id="b6143-326">Es eficaz, pero tiene las siguientes restricciones:</span><span class="sxs-lookup"><span data-stu-id="b6143-326">It is efficient, but has the following constraints:</span></span>

-   <span data-ttu-id="b6143-327">No existe compatibilidad para los subalmacenamientos.</span><span class="sxs-lookup"><span data-stu-id="b6143-327">No support exists for substorages.</span></span>
-   <span data-ttu-id="b6143-328">No se pueden calcular las referencias del objeto de almacenamiento y de los objetos de secuencia obtenidos de él.</span><span class="sxs-lookup"><span data-stu-id="b6143-328">The storage object, and stream objects obtained from it, cannot be marshaled.</span></span>
-   <span data-ttu-id="b6143-329">Cada flujo tiene un tamaño mínimo.</span><span class="sxs-lookup"><span data-stu-id="b6143-329">Each stream has a minimum size.</span></span> <span data-ttu-id="b6143-330">Si se escriben menos bytes como mínimo en una secuencia cuando se libera la secuencia, la secuencia se extiende al tamaño mínimo.</span><span class="sxs-lookup"><span data-stu-id="b6143-330">If fewer than the minimum bytes are written into a stream when the stream is released, the stream is extended to the minimum size.</span></span> <span data-ttu-id="b6143-331">Por ejemplo, el tamaño mínimo de una implementación de [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) determinada es de 4 KB.</span><span class="sxs-lookup"><span data-stu-id="b6143-331">For example, the minimum size for a particular [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) implementation is 4 KB.</span></span> <span data-ttu-id="b6143-332">Se crea un flujo y se escribe 1 KB en él.</span><span class="sxs-lookup"><span data-stu-id="b6143-332">A stream is created and 1 KB is written to it.</span></span> <span data-ttu-id="b6143-333">En el lanzamiento final de esa **IStream**, el tamaño de la secuencia se extenderá automáticamente a 4 KB.</span><span class="sxs-lookup"><span data-stu-id="b6143-333">At the final release of that **IStream**, the stream size will be automatically extended to 4 KB.</span></span> <span data-ttu-id="b6143-334">Posteriormente, al abrir la secuencia y llamar al método [**IStream:: Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) , se mostrará un tamaño de 4 KB.</span><span class="sxs-lookup"><span data-stu-id="b6143-334">Subsequently, opening the stream and calling the [**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) method will show a size of 4 KB.</span></span>
-   <span data-ttu-id="b6143-335">No todos los métodos de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) o [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) serán compatibles con la implementación de.</span><span class="sxs-lookup"><span data-stu-id="b6143-335">Not all methods of [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) or [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) will be supported by the implementation.</span></span> <span data-ttu-id="b6143-336">Para obtener más información, vea [implementación de archivos compuestos de IStorage](istorage-compound-file-implementation.md)e [implementación de archivos compuestos de IStream](istream-compound-file-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="b6143-336">For more information, see [IStorage - Compound File Implementation](istorage-compound-file-implementation.md), and [IStream - Compound File Implementation](istream-compound-file-implementation.md).</span></span>

<span data-ttu-id="b6143-337">El [cálculo de referencias](/windows/desktop/Midl/marshaling-ole-data-types) es el proceso de empaquetar, desempaquetar y enviar parámetros de método de interfaz a través de los límites de subprocesos o procesos dentro de una llamada a procedimiento remoto (RPC).</span><span class="sxs-lookup"><span data-stu-id="b6143-337">[Marshaling](/windows/desktop/Midl/marshaling-ole-data-types) is the process of packaging, unpackaging, and sending interface method parameters across thread or process boundaries within a Remote Procedure Call (RPC).</span></span> <span data-ttu-id="b6143-338">Para obtener más información, vea Serialización de [detalles](../com/marshaling-details.md) y [serialización](../com/interface-marshaling.md)de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="b6143-338">For more information, see [Marshaling Details](../com/marshaling-details.md) and [Interface Marshaling](../com/interface-marshaling.md).</span></span>

<span data-ttu-id="b6143-339">Cuando una operación de creación obtiene un objeto de almacenamiento en modo simple:</span><span class="sxs-lookup"><span data-stu-id="b6143-339">When a storage object is obtained by a Create operation in simple mode:</span></span>

-   <span data-ttu-id="b6143-340">Los elementos de secuencia se pueden crear, pero no abrir.</span><span class="sxs-lookup"><span data-stu-id="b6143-340">Stream elements can be created, but not opened.</span></span>
-   <span data-ttu-id="b6143-341">Cuando se crea un elemento de secuencia mediante una llamada a [**IStorage:: CreateStream (**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream), no es posible crear otro flujo hasta que se libere el objeto de secuencia.</span><span class="sxs-lookup"><span data-stu-id="b6143-341">When a stream element is created by calling [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream), it is not possible to create another stream until that stream object is released.</span></span>
-   <span data-ttu-id="b6143-342">Una vez que se escriben todas las secuencias, llame a [**IStorage:: commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) para vaciar los cambios.</span><span class="sxs-lookup"><span data-stu-id="b6143-342">After all streams are written, call [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) to flush the changes.</span></span>

<span data-ttu-id="b6143-343">Cuando una operación de apertura obtiene un objeto de almacenamiento en modo simple:</span><span class="sxs-lookup"><span data-stu-id="b6143-343">When a storage object is obtained by an Open operation in simple mode:</span></span>

-   <span data-ttu-id="b6143-344">Es posible abrir un solo elemento de secuencia a la vez.</span><span class="sxs-lookup"><span data-stu-id="b6143-344">It is possible to open only one stream element at a time.</span></span>
-   <span data-ttu-id="b6143-345">No es posible cambiar el tamaño de una secuencia llamando al método [**IStream:: setSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) o buscando o escribiendo más allá del final de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="b6143-345">It is not possible to change the size of a stream by calling the [**IStream::SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) method or by seeking or writing beyond the end of the stream.</span></span> <span data-ttu-id="b6143-346">Sin embargo, dado que todos los flujos tienen un tamaño mínimo, es posible usar el flujo hasta ese tamaño, aunque se hayan escrito menos datos en él.</span><span class="sxs-lookup"><span data-stu-id="b6143-346">However, because all streams are of a minimum size, it is possible to use the stream up to that size, even if less data was originally written to it.</span></span> <span data-ttu-id="b6143-347">Para determinar el tamaño de una secuencia, use el método [**IStream:: Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) .</span><span class="sxs-lookup"><span data-stu-id="b6143-347">To determine the size of a stream, use the [**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) method.</span></span>

<span data-ttu-id="b6143-348">Tenga en cuenta que, si un objeto de almacenamiento modifica un elemento de almacenamiento que no está en modo simple, no será posible, de nuevo, abrir ese elemento de almacenamiento en modo simple.</span><span class="sxs-lookup"><span data-stu-id="b6143-348">Be aware that, if a storage element is modified by a storage object that is not in simple mode, it will not be possible, again, to open that storage element in simple mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6143-349">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6143-349">Requirements</span></span>



| <span data-ttu-id="b6143-350">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6143-350">Requirement</span></span> | <span data-ttu-id="b6143-351">Value</span><span class="sxs-lookup"><span data-stu-id="b6143-351">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b6143-352">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6143-352">Minimum supported client</span></span><br/> | <span data-ttu-id="b6143-353">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b6143-353">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b6143-354">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6143-354">Minimum supported server</span></span><br/> | <span data-ttu-id="b6143-355">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b6143-355">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b6143-356">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b6143-356">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6143-357"><dt>ObjBase. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6143-357"><dt>ObjBase.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6143-358">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6143-358">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6143-359">**ISequentialStream:: Read**</span><span class="sxs-lookup"><span data-stu-id="b6143-359">**ISequentialStream::Read**</span></span>](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)
</dt> <dt>

[<span data-ttu-id="b6143-360">**IStorage**</span><span class="sxs-lookup"><span data-stu-id="b6143-360">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[<span data-ttu-id="b6143-361">**StgCreateDocfile**</span><span class="sxs-lookup"><span data-stu-id="b6143-361">**StgCreateDocfile**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[<span data-ttu-id="b6143-362">**StgCreateDocfileOnILockBytes**</span><span class="sxs-lookup"><span data-stu-id="b6143-362">**StgCreateDocfileOnILockBytes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes)
</dt> <dt>

[<span data-ttu-id="b6143-363">**StgCreateStorageEx**</span><span class="sxs-lookup"><span data-stu-id="b6143-363">**StgCreateStorageEx**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)
</dt> <dt>

[<span data-ttu-id="b6143-364">**StgOpenStorage**</span><span class="sxs-lookup"><span data-stu-id="b6143-364">**StgOpenStorage**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> <dt>

[<span data-ttu-id="b6143-365">**StgOpenStorageEx**</span><span class="sxs-lookup"><span data-stu-id="b6143-365">**StgOpenStorageEx**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)
</dt> <dt>

[<span data-ttu-id="b6143-366">**StgOpenStorageOnILockBytes**</span><span class="sxs-lookup"><span data-stu-id="b6143-366">**StgOpenStorageOnILockBytes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageonilockbytes)
</dt> </dl>

 

