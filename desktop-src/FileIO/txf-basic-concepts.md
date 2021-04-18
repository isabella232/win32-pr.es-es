---
description: Describe la coherencia de lectura confirmada, el aislamiento de lectura confirmada y los conceptos de bloqueo transaccional en NTFS transaccional.
ms.assetid: 18579c4a-a832-4c89-8fb1-cd2542e4375e
title: Conceptos básicos de TxF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7f2f5d0885795f20a8dfb5e0963468ff04bb8e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361163"
---
# <a name="basic-txf-concepts"></a><span data-ttu-id="f0646-103">Conceptos básicos de TxF</span><span class="sxs-lookup"><span data-stu-id="f0646-103">Basic TxF Concepts</span></span>

## <a name="read-isolation"></a><span data-ttu-id="f0646-104">Aislamiento de lectura</span><span class="sxs-lookup"><span data-stu-id="f0646-104">Read Isolation</span></span>

<span data-ttu-id="f0646-105">NTFS transaccional (TxF) proporciona coherencia de lectura confirmada.</span><span class="sxs-lookup"><span data-stu-id="f0646-105">Transactional NTFS (TxF) provides read-committed consistency.</span></span>

<span data-ttu-id="f0646-106">Un [*escritor de transacciones*](glossary.md) hace referencia a un identificador de archivo de transacción abierto con cualquier permiso que no forma parte del acceso de lectura genérico, pero que forma parte del acceso de escritura genérico.</span><span class="sxs-lookup"><span data-stu-id="f0646-106">A [*transacted writer*](glossary.md) refers to a transacted file handle opened with any permission that is not part of generic read access but is part of generic write access.</span></span> <span data-ttu-id="f0646-107">Un *escritor de transacciones* ve la versión más reciente de un archivo que incluye todos los cambios realizados por la misma transacción.</span><span class="sxs-lookup"><span data-stu-id="f0646-107">A *transacted writer* views the most recent version of a file that includes all of the changes by the same transaction.</span></span> <span data-ttu-id="f0646-108">Solo puede haber un escritor de transacción por archivo.</span><span class="sxs-lookup"><span data-stu-id="f0646-108">There can be only one transacted writer per file.</span></span> <span data-ttu-id="f0646-109">Los escritores sin transacciones siempre están bloqueados por un escritor de transacciones, incluso si el archivo se abre con permisos de escritura compartida.</span><span class="sxs-lookup"><span data-stu-id="f0646-109">Non-transacted writers are always blocked by a transacted writer, even if the file is opened with shared-write permissions.</span></span>

<span data-ttu-id="f0646-110">Un [*lector de transacciones*](glossary.md) hace referencia a un identificador de archivo de transacciones abierto con cualquier permiso que forme parte del acceso de lectura genérico, pero que no forme parte del acceso de escritura genérico.</span><span class="sxs-lookup"><span data-stu-id="f0646-110">A [*transacted reader*](glossary.md) refers to a transacted file handle opened with any permission that is a part of generic read access but is not part of generic write access.</span></span> <span data-ttu-id="f0646-111">Un *lector de transacciones* ve una versión confirmada del archivo que existía en el momento en que se abrió el identificador de archivo.</span><span class="sxs-lookup"><span data-stu-id="f0646-111">A *transacted reader* views a committed version of the file that existed at the time the file handle was opened.</span></span> <span data-ttu-id="f0646-112">El lector de transacciones está aislado de los efectos de los escritores de transacciones.</span><span class="sxs-lookup"><span data-stu-id="f0646-112">The transacted reader is isolated from the effects of transacted writers.</span></span> <span data-ttu-id="f0646-113">Esto proporciona una vista coherente del archivo solo mientras dure el identificador de archivo y bloquea los escritores sin transacciones.</span><span class="sxs-lookup"><span data-stu-id="f0646-113">This provides a consistent view of the file only for the life of the file handle and blocks non-transacted writers.</span></span>

> [!Note]  
> <span data-ttu-id="f0646-114">Cuando se ha abierto un identificador para su modificación con la función [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) , todas las aperturas posteriores del archivo dentro de esa transacción, ya sean de solo lectura o no, las convierte el sistema para que sea un escritor de transacciones con el fin de aislamiento y otra semántica transaccional.</span><span class="sxs-lookup"><span data-stu-id="f0646-114">When a handle has been opened for modification with the [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) function, all subsequent opens of the file within that transaction whether read-only or not are converted by the system to be a transacted writer for the purposes of isolation and other transactional semantics.</span></span> <span data-ttu-id="f0646-115">Esto significa que, posteriormente, cuando se abre un identificador para el acceso de solo lectura, el identificador no recibe una vista del archivo antes del inicio de la transacción; recibe la vista de transacción activa del archivo.</span><span class="sxs-lookup"><span data-stu-id="f0646-115">This means that subsequently, when a handle is opened for read-only access, the handle does not receive a view of the file prior to the start of the transaction; it receives the active transaction view of the file.</span></span>

 

<span data-ttu-id="f0646-116">Un identificador de archivo sin transacciones no ve ningún cambio realizado dentro de una transacción hasta que se confirma la transacción.</span><span class="sxs-lookup"><span data-stu-id="f0646-116">A non-transacted file handle does not see any changes made within a transaction until the transaction is committed.</span></span> <span data-ttu-id="f0646-117">El identificador de archivo sin transacciones recibe una vista aislada similar a un lector de transacciones, pero a diferencia de un lector de transacciones, recibe la actualización del archivo cuando un escritor de transacciones confirma la transacción.</span><span class="sxs-lookup"><span data-stu-id="f0646-117">The non-transacted file handle receives an isolated view that is similar to a transacted reader, but unlike a transacted reader, it receives the file update when a transacted writer commits the transaction.</span></span>

## <a name="isolation-levels"></a><span data-ttu-id="f0646-118">Niveles de aislamiento</span><span class="sxs-lookup"><span data-stu-id="f0646-118">Isolation Levels</span></span>

<span data-ttu-id="f0646-119">TxF proporciona aislamiento de lectura confirmada.</span><span class="sxs-lookup"><span data-stu-id="f0646-119">TxF provides read-committed isolation.</span></span> <span data-ttu-id="f0646-120">Esto significa que las actualizaciones de archivos no se ven fuera de la transacción.</span><span class="sxs-lookup"><span data-stu-id="f0646-120">This means that file updates are not seen outside the transaction.</span></span> <span data-ttu-id="f0646-121">Además, si un archivo se abre más de una vez al leer archivos dentro de la transacción, puede ver resultados diferentes con cada apertura subsiguiente.</span><span class="sxs-lookup"><span data-stu-id="f0646-121">In addition, if a file is opened more than once while reading files within the transaction, you may see different results with each subsequent opening.</span></span> <span data-ttu-id="f0646-122">Los archivos que estaban disponibles la primera vez que tuvo acceso a ellos pueden no estar disponibles (porque se eliminaron), o viceversa.</span><span class="sxs-lookup"><span data-stu-id="f0646-122">Files that were available the first time you accessed them may not be available (because they were deleted), or vice versa.</span></span>

## <a name="transactional-locking"></a><span data-ttu-id="f0646-123">Bloqueo transaccional</span><span class="sxs-lookup"><span data-stu-id="f0646-123">Transactional Locking</span></span>

<span data-ttu-id="f0646-124">Al crear un escritor de transacciones en un archivo, se *bloquea* el archivo de una transacción.</span><span class="sxs-lookup"><span data-stu-id="f0646-124">Creating a transacted writer on a file *transactionally locks* the file.</span></span> <span data-ttu-id="f0646-125">Una vez que un archivo está bloqueado por una transacción, otras operaciones del sistema de archivos externas a la transacción de bloqueo que intentan modificar el archivo bloqueado de forma transaccional producirán un error con **\_ \_ infracción de uso compartido de errores** o **\_ \_ conflicto transaccional de errores**.</span><span class="sxs-lookup"><span data-stu-id="f0646-125">After a file is locked by a transaction, other file system operations external to the locking transaction that try to modify the transactionally locked file will fail with either **ERROR\_SHARING\_VIOLATION** or **ERROR\_TRANSACTIONAL\_CONFLICT**.</span></span>

<span data-ttu-id="f0646-126">En la tabla siguiente se resume el bloqueo transaccional.</span><span class="sxs-lookup"><span data-stu-id="f0646-126">The following table summarizes transactional locking.</span></span>



<span data-ttu-id="f0646-127">Archivo abierto actualmente por</span><span class="sxs-lookup"><span data-stu-id="f0646-127">File currently opened by</span></span>

<span data-ttu-id="f0646-128">Intento de apertura de archivo</span><span class="sxs-lookup"><span data-stu-id="f0646-128">File open attempted by</span></span>

<span data-ttu-id="f0646-129">Conseguido</span><span class="sxs-lookup"><span data-stu-id="f0646-129">Transacted</span></span>

<span data-ttu-id="f0646-130">Sin transacciones</span><span class="sxs-lookup"><span data-stu-id="f0646-130">Non-Transacted</span></span>

<span data-ttu-id="f0646-131">Lector</span><span class="sxs-lookup"><span data-stu-id="f0646-131">Reader</span></span>

<span data-ttu-id="f0646-132">Lector/escritor</span><span class="sxs-lookup"><span data-stu-id="f0646-132">Reader/Writer</span></span>

<span data-ttu-id="f0646-133">Lector</span><span class="sxs-lookup"><span data-stu-id="f0646-133">Reader</span></span>

<span data-ttu-id="f0646-134">Lector/escritor</span><span class="sxs-lookup"><span data-stu-id="f0646-134">Reader/Writer</span></span>

<span data-ttu-id="f0646-135">Lector de transacciones</span><span class="sxs-lookup"><span data-stu-id="f0646-135">Transacted Reader</span></span>

<span data-ttu-id="f0646-136">Sí</span><span class="sxs-lookup"><span data-stu-id="f0646-136">Yes</span></span>

<span data-ttu-id="f0646-137">Sí</span><span class="sxs-lookup"><span data-stu-id="f0646-137">Yes</span></span>

<span data-ttu-id="f0646-138">Sí</span><span class="sxs-lookup"><span data-stu-id="f0646-138">Yes</span></span>

<span data-ttu-id="f0646-139">No2</span><span class="sxs-lookup"><span data-stu-id="f0646-139">No2</span></span>

<span data-ttu-id="f0646-140">Lector/escritor de transacción</span><span class="sxs-lookup"><span data-stu-id="f0646-140">Transacted Reader/Writer</span></span>

<span data-ttu-id="f0646-141">Sí</span><span class="sxs-lookup"><span data-stu-id="f0646-141">Yes</span></span>

<span data-ttu-id="f0646-142">No2</span><span class="sxs-lookup"><span data-stu-id="f0646-142">No2</span></span>

<span data-ttu-id="f0646-143">Sí</span><span class="sxs-lookup"><span data-stu-id="f0646-143">Yes</span></span>

<span data-ttu-id="f0646-144">No2</span><span class="sxs-lookup"><span data-stu-id="f0646-144">No2</span></span>

<span data-ttu-id="f0646-145">Lector sin transacciones</span><span class="sxs-lookup"><span data-stu-id="f0646-145">Non-Transacted Reader</span></span>

<span data-ttu-id="f0646-146">Sí</span><span class="sxs-lookup"><span data-stu-id="f0646-146">Yes</span></span>

<span data-ttu-id="f0646-147">Sí</span><span class="sxs-lookup"><span data-stu-id="f0646-147">Yes</span></span>

<span data-ttu-id="f0646-148">Sí</span><span class="sxs-lookup"><span data-stu-id="f0646-148">Yes</span></span>

<span data-ttu-id="f0646-149">Sí</span><span class="sxs-lookup"><span data-stu-id="f0646-149">Yes</span></span>

<span data-ttu-id="f0646-150">Lector/escritor sin transacciones</span><span class="sxs-lookup"><span data-stu-id="f0646-150">Non-Transacted Reader/Writer</span></span>

<span data-ttu-id="f0646-151">No1</span><span class="sxs-lookup"><span data-stu-id="f0646-151">No1</span></span>

<span data-ttu-id="f0646-152">No1</span><span class="sxs-lookup"><span data-stu-id="f0646-152">No1</span></span>

<span data-ttu-id="f0646-153">Sí</span><span class="sxs-lookup"><span data-stu-id="f0646-153">Yes</span></span>

<span data-ttu-id="f0646-154">Sí</span><span class="sxs-lookup"><span data-stu-id="f0646-154">Yes</span></span>

1. <span data-ttu-id="f0646-155">Error de **\_ \_ conflicto transaccional**</span><span class="sxs-lookup"><span data-stu-id="f0646-155">Fails with **ERROR\_TRANSACTIONAL\_CONFLICT**</span></span><br/> <span data-ttu-id="f0646-156">2. se produce un **error de \_ \_ infracción de uso compartido**</span><span class="sxs-lookup"><span data-stu-id="f0646-156">2. Fails with **ERROR\_SHARING\_VIOLATION**</span></span><br/>



 

<span data-ttu-id="f0646-157">Si abre una secuencia con nombre para una modificación que está utilizando una transacción, se requiere que el archivo completo esté bloqueado.</span><span class="sxs-lookup"><span data-stu-id="f0646-157">If you open a named stream for a modification that is using a transaction, the entire file is required to be locked.</span></span>

<span data-ttu-id="f0646-158">Además del bloqueo transaccional, se aplican las reglas típicas de uso compartido de archivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="f0646-158">In addition to transactional locking, typical NTFS file-sharing rules apply.</span></span>

<span data-ttu-id="f0646-159">En paralelo, debe tener en cuenta los dos modos de uso compartido de archivos siguientes:</span><span class="sxs-lookup"><span data-stu-id="f0646-159">You need to consider the following two file sharing modes in parallel:</span></span>

-   <span data-ttu-id="f0646-160">Modo de bloqueo transaccional.</span><span class="sxs-lookup"><span data-stu-id="f0646-160">The transactional locking mode.</span></span>
-   <span data-ttu-id="f0646-161">Modos normales de uso compartido de archivos.</span><span class="sxs-lookup"><span data-stu-id="f0646-161">Normal file-sharing modes.</span></span>

<span data-ttu-id="f0646-162">El modo que sea más restrictivo es el que se aplica.</span><span class="sxs-lookup"><span data-stu-id="f0646-162">Whichever mode is more restrictive is the one that applies.</span></span>

 

 




