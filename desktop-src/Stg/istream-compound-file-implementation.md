---
title: Implementación de archivos compuestos de IStream
description: La interfaz IStream permite leer y escribir datos en objetos de secuencia. En un objeto de almacenamiento estructurado, los objetos Stream contienen los datos y los almacenamientos proporcionan la estructura.
ms.assetid: 52474e37-0e14-4dcc-8e04-4442cfd26eb3
keywords:
- IStream Strctd STG, implementación de archivo compuesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d15e671521f4a1e81b78579bc1225eccb48898
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "105670045"
---
# <a name="istream---compound-file-implementation"></a><span data-ttu-id="b8dab-105">Implementación de archivos compuestos de IStream</span><span class="sxs-lookup"><span data-stu-id="b8dab-105">IStream - Compound File Implementation</span></span>

<span data-ttu-id="b8dab-106">La interfaz [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) permite leer y escribir datos en objetos de secuencia.</span><span class="sxs-lookup"><span data-stu-id="b8dab-106">The [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) interface supports reading and writing data to stream objects.</span></span> <span data-ttu-id="b8dab-107">En un objeto de almacenamiento estructurado, los objetos Stream contienen los datos y los almacenamientos proporcionan la estructura.</span><span class="sxs-lookup"><span data-stu-id="b8dab-107">In a structured storage object, stream objects contain the data and storages provide the structure.</span></span> <span data-ttu-id="b8dab-108">Los datos simples se pueden escribir directamente en una secuencia, pero con más frecuencia, las secuencias son elementos anidados dentro de un objeto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="b8dab-108">Simple data can be written directly to a stream, but more frequently, streams are elements nested within a storage object.</span></span> <span data-ttu-id="b8dab-109">Son similares a los archivos estándar.</span><span class="sxs-lookup"><span data-stu-id="b8dab-109">They are similar to standard files.</span></span>

<span data-ttu-id="b8dab-110">La especificación de [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) define más funcionalidad de la que admite la implementación de com.</span><span class="sxs-lookup"><span data-stu-id="b8dab-110">The specification of [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) defines more functionality than the COM implementation supports.</span></span> <span data-ttu-id="b8dab-111">Por ejemplo, la interfaz **IStream** define las secuencias hasta 2 ⁶ ⁴ bytes de longitud que requieren un puntero de búsqueda de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="b8dab-111">For example, the **IStream** interface defines streams up to 2⁶⁴ bytes in length requiring a 64-bit seek pointer.</span></span> <span data-ttu-id="b8dab-112">Sin embargo, la implementación COM solo admite secuencias de hasta 2 ³ ² bytes de longitud (4 GB) y las operaciones de lectura y escritura siempre están limitadas a 2 ³ ² bytes a la vez.</span><span class="sxs-lookup"><span data-stu-id="b8dab-112">However, the COM implementation only supports streams up to 2³² bytes in length (4 GB) and read and write operations are always limited to 2³² bytes at a time.</span></span> <span data-ttu-id="b8dab-113">La implementación COM tampoco admite el bloqueo de la transacción o de la región.</span><span class="sxs-lookup"><span data-stu-id="b8dab-113">The COM implementation also does not support stream transactioning or region locking.</span></span>

<span data-ttu-id="b8dab-114">Para crear una secuencia simple basada en la memoria global, obtenga un puntero [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) llamando a la función de API [**CreateStreamOnHGlobal**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal).</span><span class="sxs-lookup"><span data-stu-id="b8dab-114">To create a simple stream based on global memory, get an [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) pointer by calling the API function [**CreateStreamOnHGlobal**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal).</span></span> <span data-ttu-id="b8dab-115">Para obtener un puntero **IStream** dentro de un objeto de archivo compuesto, llame a [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) o [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage).</span><span class="sxs-lookup"><span data-stu-id="b8dab-115">To get an **IStream** pointer within a compound file object, call either [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) or [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage).</span></span> <span data-ttu-id="b8dab-116">Estas funciones recuperan un puntero [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , con el que se puede llamar a [**CreateStream (**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) o [**OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) para un puntero **IStream** .</span><span class="sxs-lookup"><span data-stu-id="b8dab-116">These functions retrieve an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) pointer, with which you can then call [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) or [**OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) for an **IStream** pointer.</span></span> <span data-ttu-id="b8dab-117">En cualquier caso, se usa el mismo código de implementación de **IStream** .</span><span class="sxs-lookup"><span data-stu-id="b8dab-117">In either case, the same **IStream** implementation code is used.</span></span>

> [!Note]  
> <span data-ttu-id="b8dab-118">La implementación de archivos compuestos de almacenamiento estructurado no se realiza correctamente en un método [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para [**ISequentialStream**](/windows/desktop/api/Objidl/nn-objidl-isequentialstream), pero incluye los métodos de [**lectura**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) y [**escritura**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) a través del puntero de interfaz [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="b8dab-118">The compound file implementation of structured storage does not succeed on a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method for [**ISequentialStream**](/windows/desktop/api/Objidl/nn-objidl-isequentialstream), but it includes the [**Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) and [**Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) methods through the [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) interface pointer.</span></span>

 

## <a name="when-to-use"></a><span data-ttu-id="b8dab-119">Cuándo usar</span><span class="sxs-lookup"><span data-stu-id="b8dab-119">When to Use</span></span>

<span data-ttu-id="b8dab-120">Llame a los métodos de [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) para leer y escribir datos en una secuencia.</span><span class="sxs-lookup"><span data-stu-id="b8dab-120">Call the methods of [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) to read and write data to a stream.</span></span>

<span data-ttu-id="b8dab-121">Dado que los objetos de secuencia se pueden serializar en otros procesos, las aplicaciones pueden compartir los datos de los objetos de almacenamiento sin tener que usar la memoria global.</span><span class="sxs-lookup"><span data-stu-id="b8dab-121">Because stream objects can be marshaled to other processes, applications can share the data in storage objects without having to use global memory.</span></span> <span data-ttu-id="b8dab-122">En la implementación de archivo compuesto COM de objetos de secuencia, las funciones personalizadas de serialización en COM crean una versión remota del objeto original en el nuevo proceso cuando los dos procesos tienen acceso de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="b8dab-122">In the COM compound file implementation of stream objects, the custom marshaling facilities in COM create a remote version of the original object in the new process when the two processes have shared-memory access.</span></span> <span data-ttu-id="b8dab-123">Por lo tanto, la versión remota no necesita comunicarse con el proceso original para llevar a cabo sus funciones.</span><span class="sxs-lookup"><span data-stu-id="b8dab-123">Thus, the remote version does not need to communicate with the original process to carry out its functions.</span></span>

<span data-ttu-id="b8dab-124">La versión remota del objeto de secuencia comparte el mismo puntero de búsqueda que la secuencia original.</span><span class="sxs-lookup"><span data-stu-id="b8dab-124">The remote version of the stream object shares the same seek pointer as the original stream.</span></span> <span data-ttu-id="b8dab-125">Si no desea compartir el puntero de búsqueda, use el método [**IStream:: Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) para proporcionar una copia del objeto de secuencia para el proceso remoto.</span><span class="sxs-lookup"><span data-stu-id="b8dab-125">If you do not want to share the seek pointer, use the [**IStream::Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) method to provide a copy of the stream object for the remote process.</span></span>

> [!Note]
> <span data-ttu-id="b8dab-126">Si se crea un objeto de secuencia que es mayor que el montón en la memoria del equipo y se utiliza un identificador **HGLOBAL** para un objeto de memoria global, el objeto de secuencia llama al método [**GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) internamente al requiere más memoria.</span><span class="sxs-lookup"><span data-stu-id="b8dab-126">If creating a stream object that is larger than the heap in your computer's memory and you are using an **HGLOBAL** handle to a global memory object, the stream object calls the [**GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) method internally whe it requires more memory.</span></span> <span data-ttu-id="b8dab-127">Dado que **GlobalRealloc** siempre copia los datos del origen en el destino, el aumento de un objeto de secuencia de 20 MB a 25 MB, por ejemplo, requiere una gran cantidad de tiempo.</span><span class="sxs-lookup"><span data-stu-id="b8dab-127">Because **GlobalRealloc** always copies data from the source to the destination, increasing a stream object from 20 MB to 25 MB, for example, requires large amounts of time.</span></span> <span data-ttu-id="b8dab-128">Esto se debe al tamaño de los incrementos copiados y se empeora si hay menos de 45 MB de memoria en el equipo debido al intercambio de disco.</span><span class="sxs-lookup"><span data-stu-id="b8dab-128">This is due to the size of the increments copied and is worsened if there is less than 45 MB of memory on the computer because of disk swapping.</span></span>
>
> <span data-ttu-id="b8dab-129">La solución preferida consiste en implementar un método [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) que use la memoria asignada por [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) en lugar de [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc).</span><span class="sxs-lookup"><span data-stu-id="b8dab-129">The preferred solution is to implement an [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) method that uses memory allocated by [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) instead of [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc).</span></span> <span data-ttu-id="b8dab-130">Esto puede reservar un gran fragmento de espacio de direcciones virtuales y, a continuación, confirmar la memoria dentro de ese espacio de direcciones según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="b8dab-130">This can reserve a large chunk of virtual address space and then commit memory within that address space as required.</span></span> <span data-ttu-id="b8dab-131">No se realiza la copia de datos y la memoria se confirma solo cuando es necesario.</span><span class="sxs-lookup"><span data-stu-id="b8dab-131">No data copying occurs and memory is committed only as it is required.</span></span>
>
> <span data-ttu-id="b8dab-132">Una alternativa a [**GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) es llamar al método [**IStream:: setSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) en el objeto de secuencia para aumentar la asignación de memoria de antemano.</span><span class="sxs-lookup"><span data-stu-id="b8dab-132">An alternative to [**GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) is to call the [**IStream::SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) method on the stream object to increase the memory allocation in advance.</span></span> <span data-ttu-id="b8dab-133">Sin embargo, esto no es tan eficaz como el uso de [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc), como se describió anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b8dab-133">This is not, however, as efficient as using [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc), as described above.</span></span>

 

## <a name="methods"></a><span data-ttu-id="b8dab-134">Métodos</span><span class="sxs-lookup"><span data-stu-id="b8dab-134">Methods</span></span>

<dl> <dt>

<span data-ttu-id="b8dab-135"><span id="ISequentialStream__Read"></span><span id="isequentialstream__read"></span><span id="ISEQUENTIALSTREAM__READ"></span>[**ISequentialStream:: Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)</span><span class="sxs-lookup"><span data-stu-id="b8dab-135"><span id="ISequentialStream__Read"></span><span id="isequentialstream__read"></span><span id="ISEQUENTIALSTREAM__READ"></span>[**ISequentialStream::Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)</span></span>
</dt> <dd>

<span data-ttu-id="b8dab-136">Lee un número especificado de bytes del objeto de flujo en la memoria, empezando en el puntero de búsqueda actual.</span><span class="sxs-lookup"><span data-stu-id="b8dab-136">Reads a specified number of bytes from the stream object into memory starting at the current seek pointer.</span></span> <span data-ttu-id="b8dab-137">Esta implementación devuelve \_ si se alcanzó el final de la secuencia durante la lectura.</span><span class="sxs-lookup"><span data-stu-id="b8dab-137">This implementation returns S\_OK if the end of the stream was reached during the read.</span></span> <span data-ttu-id="b8dab-138">(Esto es lo mismo que el comportamiento de "fin de archivo" que se encuentra en el sistema de archivos FAT de MS-DOS).</span><span class="sxs-lookup"><span data-stu-id="b8dab-138">(This is the same as the "end of file" behavior found in the MS-DOS FAT file system.)</span></span>

</dd> <dt>

<span data-ttu-id="b8dab-139"><span id="ISequentialStream__Write"></span><span id="isequentialstream__write"></span><span id="ISEQUENTIALSTREAM__WRITE"></span>[**ISequentialStream:: Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write)</span><span class="sxs-lookup"><span data-stu-id="b8dab-139"><span id="ISequentialStream__Write"></span><span id="isequentialstream__write"></span><span id="ISEQUENTIALSTREAM__WRITE"></span>[**ISequentialStream::Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write)</span></span>
</dt> <dd>

<span data-ttu-id="b8dab-140">Escribe un número especificado de bytes en el objeto de flujo, empezando en el puntero de búsqueda actual.</span><span class="sxs-lookup"><span data-stu-id="b8dab-140">Writes a specified number from bytes into the stream object starting at the current seek pointer.</span></span> <span data-ttu-id="b8dab-141">En esta implementación, los objetos de secuencia no son dispersos.</span><span class="sxs-lookup"><span data-stu-id="b8dab-141">In this implementation, stream objects are not sparse.</span></span> <span data-ttu-id="b8dab-142">Los bytes de relleno se asignan finalmente en el disco y se asignan a la secuencia.</span><span class="sxs-lookup"><span data-stu-id="b8dab-142">Any fill bytes are eventually allocated on the disk and assigned to the stream.</span></span>

</dd> <dt>

<span data-ttu-id="b8dab-143"><span id="IStream__Seek"></span><span id="istream__seek"></span><span id="ISTREAM__SEEK"></span>[**IStream:: Seek**](/windows/desktop/api/Objidl/nf-objidl-istream-seek)</span><span class="sxs-lookup"><span data-stu-id="b8dab-143"><span id="IStream__Seek"></span><span id="istream__seek"></span><span id="ISTREAM__SEEK"></span>[**IStream::Seek**](/windows/desktop/api/Objidl/nf-objidl-istream-seek)</span></span>
</dt> <dd>

<span data-ttu-id="b8dab-144">Cambia el puntero de búsqueda a una nueva ubicación respecto al principio del flujo, al final del flujo o al puntero de búsqueda actual.</span><span class="sxs-lookup"><span data-stu-id="b8dab-144">Changes the seek pointer to a new location relative to the beginning of the stream, to the end of the stream, or to the current seek pointer.</span></span>

</dd> <dt>

<span data-ttu-id="b8dab-145"><span id="IStream__SetSize"></span><span id="istream__setsize"></span><span id="ISTREAM__SETSIZE"></span>[**IStream:: setSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize)</span><span class="sxs-lookup"><span data-stu-id="b8dab-145"><span id="IStream__SetSize"></span><span id="istream__setsize"></span><span id="ISTREAM__SETSIZE"></span>[**IStream::SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize)</span></span>
</dt> <dd>

<span data-ttu-id="b8dab-146">Cambia el tamaño del objeto de secuencia.</span><span class="sxs-lookup"><span data-stu-id="b8dab-146">Changes the size of the stream object.</span></span> <span data-ttu-id="b8dab-147">En esta implementación, no hay ninguna garantía de que el espacio asignado sea contiguo.</span><span class="sxs-lookup"><span data-stu-id="b8dab-147">In this implementation, there is no guarantee that the space allocated will be contiguous.</span></span>

</dd> <dt>

<span data-ttu-id="b8dab-148"><span id="IStream__CopyTo"></span><span id="istream__copyto"></span><span id="ISTREAM__COPYTO"></span>[**IStream:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto)</span><span class="sxs-lookup"><span data-stu-id="b8dab-148"><span id="IStream__CopyTo"></span><span id="istream__copyto"></span><span id="ISTREAM__COPYTO"></span>[**IStream::CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto)</span></span>
</dt> <dd>

<span data-ttu-id="b8dab-149">Copia un número especificado de bytes del puntero de búsqueda actual del flujo en el puntero de búsqueda actual de otro flujo.</span><span class="sxs-lookup"><span data-stu-id="b8dab-149">Copies a specified number of bytes from the current seek pointer in the stream to the current seek pointer in another stream.</span></span>

</dd> <dt>

<span data-ttu-id="b8dab-150"><span id="IStream__Commit"></span><span id="istream__commit"></span><span id="ISTREAM__COMMIT"></span>[**IStream:: commit**](/windows/desktop/api/Objidl/nf-objidl-istream-commit)</span><span class="sxs-lookup"><span data-stu-id="b8dab-150"><span id="IStream__Commit"></span><span id="istream__commit"></span><span id="ISTREAM__COMMIT"></span>[**IStream::Commit**](/windows/desktop/api/Objidl/nf-objidl-istream-commit)</span></span>
</dt> <dd>

<span data-ttu-id="b8dab-151">La implementación de archivo compuesto de [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) admite la apertura de secuencias solo en modo directo, no en modo de transacción.</span><span class="sxs-lookup"><span data-stu-id="b8dab-151">The compound file implementation of [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) supports opening streams only in direct mode, not transacted mode.</span></span> <span data-ttu-id="b8dab-152">Por lo tanto, el método no tiene ningún efecto cuando se llama a otro para vaciar todos los búferes de memoria en el siguiente nivel de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="b8dab-152">Therefore, the method has no effect when called other than to flush all memory buffers to the next storage level.</span></span>

<span data-ttu-id="b8dab-153">En esta implementación, no importa si confirma los cambios en los flujos, solo necesita confirmar los cambios de los objetos de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="b8dab-153">In this implementation, it does not matter if you commit changes to streams, you need only commit changes for storage objects.</span></span>

</dd> <dt>

<span data-ttu-id="b8dab-154"><span id="IStream__Revert"></span><span id="istream__revert"></span><span id="ISTREAM__REVERT"></span>[**IStream:: revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert)</span><span class="sxs-lookup"><span data-stu-id="b8dab-154"><span id="IStream__Revert"></span><span id="istream__revert"></span><span id="ISTREAM__REVERT"></span>[**IStream::Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert)</span></span>
</dt> <dd>

<span data-ttu-id="b8dab-155">Esta implementación no admite secuencias de transacción, por lo que una llamada a este método no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="b8dab-155">This implementation does not support transacted streams, so a call to this method has no effect.</span></span>

</dd> <dt>

<span data-ttu-id="b8dab-156"><span id="IStream__LockRegion"></span><span id="istream__lockregion"></span><span id="ISTREAM__LOCKREGION"></span>[**IStream:: LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion)</span><span class="sxs-lookup"><span data-stu-id="b8dab-156"><span id="IStream__LockRegion"></span><span id="istream__lockregion"></span><span id="ISTREAM__LOCKREGION"></span>[**IStream::LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion)</span></span>
</dt> <dd>

<span data-ttu-id="b8dab-157">Esta implementación no admite el bloqueo de intervalo, por lo que una llamada a este método no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="b8dab-157">Range-locking is not supported by this implementation, so a call to this method has no effect.</span></span>

</dd> <dt>

<span data-ttu-id="b8dab-158"><span id="IStream__UnlockRegion"></span><span id="istream__unlockregion"></span><span id="ISTREAM__UNLOCKREGION"></span>[**IStream:: UnlockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-unlockregion)</span><span class="sxs-lookup"><span data-stu-id="b8dab-158"><span id="IStream__UnlockRegion"></span><span id="istream__unlockregion"></span><span id="ISTREAM__UNLOCKREGION"></span>[**IStream::UnlockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-unlockregion)</span></span>
</dt> <dd>

<span data-ttu-id="b8dab-159">Quita la restricción de acceso de un intervalo de bytes previamente restringido con [**IStream:: LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion).</span><span class="sxs-lookup"><span data-stu-id="b8dab-159">Removes the access restriction on a range of bytes previously restricted with [**IStream::LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion).</span></span>

</dd> <dt>

<span data-ttu-id="b8dab-160"><span id="IStream__Stat"></span><span id="istream__stat"></span><span id="ISTREAM__STAT"></span>[**IStream:: Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)</span><span class="sxs-lookup"><span data-stu-id="b8dab-160"><span id="IStream__Stat"></span><span id="istream__stat"></span><span id="ISTREAM__STAT"></span>[**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)</span></span>
</dt> <dd>

<span data-ttu-id="b8dab-161">Recupera la estructura [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) para esta secuencia.</span><span class="sxs-lookup"><span data-stu-id="b8dab-161">Retrieves the [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) structure for this stream</span></span>

</dd> <dt>

<span data-ttu-id="b8dab-162"><span id="IStream__Clone"></span><span id="istream__clone"></span><span id="ISTREAM__CLONE"></span>[**IStream:: Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone)</span><span class="sxs-lookup"><span data-stu-id="b8dab-162"><span id="IStream__Clone"></span><span id="istream__clone"></span><span id="ISTREAM__CLONE"></span>[**IStream::Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone)</span></span>
</dt> <dd>

<span data-ttu-id="b8dab-163">Crea un nuevo objeto de flujo con su propio puntero de búsqueda que hace referencia a los mismos bytes que el flujo original.</span><span class="sxs-lookup"><span data-stu-id="b8dab-163">Creates a new stream object with its own seek pointer that references the same bytes as the original stream.</span></span>

</dd> </dl>

<span data-ttu-id="b8dab-164">Una [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) de modo simple está sujeta a las siguientes restricciones.</span><span class="sxs-lookup"><span data-stu-id="b8dab-164">A simple-mode [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) is subject to the following constraints.</span></span>

-   <span data-ttu-id="b8dab-165">Una secuencia es un modo simple si se ha creado o abierto desde un almacenamiento de modo simple.</span><span class="sxs-lookup"><span data-stu-id="b8dab-165">A stream is simple mode if it was created or opened from a simple-mode storage.</span></span> <span data-ttu-id="b8dab-166">Un almacenamiento es un modo sencillo si se crea o se abre con la \_ marca de STGM simple establecida en el parámetro *grfMode* .</span><span class="sxs-lookup"><span data-stu-id="b8dab-166">A storage is simple mode if it is created or opened with the STGM\_SIMPLE flag set in the *grfMode* parameter.</span></span>
-   <span data-ttu-id="b8dab-167">No se admiten los métodos [**Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) y [**CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto) .</span><span class="sxs-lookup"><span data-stu-id="b8dab-167">The [**Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) and [**CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto) methods are not supported.</span></span>
-   <span data-ttu-id="b8dab-168">Se admite el método [**STAT**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) , pero \_ se debe especificar el valor Noname de STATFLAG.</span><span class="sxs-lookup"><span data-stu-id="b8dab-168">The [**Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) method is supported, but the STATFLAG\_NONAME value must be specified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8dab-169">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b8dab-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8dab-170">**IStream**</span><span class="sxs-lookup"><span data-stu-id="b8dab-170">**IStream**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> <dt>

[<span data-ttu-id="b8dab-171">**IStorage**</span><span class="sxs-lookup"><span data-stu-id="b8dab-171">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[<span data-ttu-id="b8dab-172">**CreateStreamOnHGlobal**</span><span class="sxs-lookup"><span data-stu-id="b8dab-172">**CreateStreamOnHGlobal**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal)
</dt> <dt>

[<span data-ttu-id="b8dab-173">**StgCreateDocfile**</span><span class="sxs-lookup"><span data-stu-id="b8dab-173">**StgCreateDocfile**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[<span data-ttu-id="b8dab-174">**StgOpenStorage**</span><span class="sxs-lookup"><span data-stu-id="b8dab-174">**StgOpenStorage**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> </dl>

 

 