---
description: La siguiente definición de interfaz se proporciona como un estándar que se puede seguir al desarrollar un proveedor de servicios de tarjetas inteligentes.
ms.assetid: 68cc0bbe-ce8e-4da1-b907-596caa95a39c
title: Interfaz ISCardFileAccess
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess
api_type:
- COM
api_location: ''
ms.openlocfilehash: fcfcdc75bcf10b922a242574bfabe267c949fa52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910877"
---
# <a name="iscardfileaccess-interface"></a><span data-ttu-id="b9cc4-103">Interfaz ISCardFileAccess</span><span class="sxs-lookup"><span data-stu-id="b9cc4-103">ISCardFileAccess interface</span></span>

<span data-ttu-id="b9cc4-104">\[La interfaz **ISCardFileAccess** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="b9cc4-104">\[The **ISCardFileAccess** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b9cc4-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b9cc4-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b9cc4-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="b9cc4-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="b9cc4-107">La siguiente definición de interfaz se proporciona como un estándar que se puede seguir al desarrollar un [*proveedor de servicios*](../secgloss/c-gly.md)de [*tarjetas inteligentes*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="b9cc4-107">The following interface definition is provided as a standard that can be followed when developing a [*smart card*](../secgloss/s-gly.md) [*service provider*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="b9cc4-108">La interfaz **ISCardFileAccess** se puede usar para implementar una interfaz de alto nivel en un sistema de archivos basado en tarjeta con un sistema de archivos de tarjeta subyacente basado en la estructura definida en ISO/IEC 7816-4.</span><span class="sxs-lookup"><span data-stu-id="b9cc4-108">The **ISCardFileAccess** interface can be used to implement a high-level interface to a card-based file system with an underlying card file system based on the structure defined in ISO/IEC 7816-4.</span></span> <span data-ttu-id="b9cc4-109">Otras implementaciones son posibles, pero se espera que sea la más común.</span><span class="sxs-lookup"><span data-stu-id="b9cc4-109">Other implementations are possible, but this is expected to be the most common.</span></span>

<span data-ttu-id="b9cc4-110">La interfaz **ISCardFileAccess** se puede usar para exponer entidades del sistema de archivos de una manera muy familiar para los desarrolladores de aplicaciones en el entorno de PC.</span><span class="sxs-lookup"><span data-stu-id="b9cc4-110">The **ISCardFileAccess** interface can be used to expose file system entities in a manner very familiar to application developers in the PC environment.</span></span> <span data-ttu-id="b9cc4-111">Proporciona mecanismos para buscar archivos específicos y realizar operaciones comunes, como seleccionar, leer, escribir, crear y eliminar.</span><span class="sxs-lookup"><span data-stu-id="b9cc4-111">It provides mechanisms for locating specific files and performing common operations such as selecting, reading, writing, creating and deleting.</span></span> <span data-ttu-id="b9cc4-112">Encapsula y enmascara gran parte de los detalles de bajo nivel implicados en la realización de estas operaciones en el nivel de tarjeta.</span><span class="sxs-lookup"><span data-stu-id="b9cc4-112">It encapsulates and masks much of the low-level detail involved in performing these operations at the card level.</span></span>

<span data-ttu-id="b9cc4-113">A continuación se usa el uso típico de la interfaz **ISCardFileAccess** .</span><span class="sxs-lookup"><span data-stu-id="b9cc4-113">Following is a typical use of the **ISCardFileAccess** interface.</span></span> <span data-ttu-id="b9cc4-114">En este caso, la interfaz **ISCardFileAccess** se usa para seleccionar, abrir y escribir en un archivo.</span><span class="sxs-lookup"><span data-stu-id="b9cc4-114">In this case, the **ISCardFileAccess** interface is used to select, open, and write to a file.</span></span>

<span data-ttu-id="b9cc4-115">**Para escribir en un archivo**</span><span class="sxs-lookup"><span data-stu-id="b9cc4-115">**To write to a file**</span></span>

1.  <span data-ttu-id="b9cc4-116">Llame a [**ISCardManage:: CreateFileAccess**](iscardmanage-createfileaccess.md) para crear una interfaz **ISCardFileAccess** .</span><span class="sxs-lookup"><span data-stu-id="b9cc4-116">Call [**ISCardManage::CreateFileAccess**](iscardmanage-createfileaccess.md) to create an **ISCardFileAccess** interface.</span></span>
2.  <span data-ttu-id="b9cc4-117">Llame a [**Open**](iscardfileaccess-open.md) para seleccionar y abrir el archivo.</span><span class="sxs-lookup"><span data-stu-id="b9cc4-117">Call [**Open**](iscardfileaccess-open.md) to select and open the file.</span></span>
3.  <span data-ttu-id="b9cc4-118">Llamar a [**Write**](iscardfileaccess-write.md).</span><span class="sxs-lookup"><span data-stu-id="b9cc4-118">Call [**Write**](iscardfileaccess-write.md).</span></span>
4.  <span data-ttu-id="b9cc4-119">Llamar a [**Close**](iscardfileaccess-close.md).</span><span class="sxs-lookup"><span data-stu-id="b9cc4-119">Call [**Close**](iscardfileaccess-close.md).</span></span>
5.  <span data-ttu-id="b9cc4-120">Libere la interfaz **ISCardFileAccess** .</span><span class="sxs-lookup"><span data-stu-id="b9cc4-120">Release the **ISCardFileAccess** interface.</span></span>

## <a name="members"></a><span data-ttu-id="b9cc4-121">Miembros</span><span class="sxs-lookup"><span data-stu-id="b9cc4-121">Members</span></span>

<span data-ttu-id="b9cc4-122">La interfaz **ISCardFileAccess** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="b9cc4-122">The **ISCardFileAccess** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="b9cc4-123">**ISCardFileAccess** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b9cc4-123">**ISCardFileAccess** also has these types of members:</span></span>

-   [<span data-ttu-id="b9cc4-124">Métodos</span><span class="sxs-lookup"><span data-stu-id="b9cc4-124">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b9cc4-125">Métodos</span><span class="sxs-lookup"><span data-stu-id="b9cc4-125">Methods</span></span>

<span data-ttu-id="b9cc4-126">La interfaz **ISCardFileAccess** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="b9cc4-126">The **ISCardFileAccess** interface has these methods.</span></span>



| <span data-ttu-id="b9cc4-127">Método</span><span class="sxs-lookup"><span data-stu-id="b9cc4-127">Method</span></span>                                                              | <span data-ttu-id="b9cc4-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9cc4-128">Description</span></span>                                                                                                                                  |
|:--------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b9cc4-129">**ChangeDir**</span><span class="sxs-lookup"><span data-stu-id="b9cc4-129">**ChangeDir**</span></span>](iscardfileaccess-changedir.md)                     | <span data-ttu-id="b9cc4-130">Cambia el directorio de la tarjeta inteligente actual al nuevo directorio especificado.</span><span class="sxs-lookup"><span data-stu-id="b9cc4-130">Changes the current smart card directory to the new specified directory.</span></span><br/>                                                          |
| [<span data-ttu-id="b9cc4-131">**Cercanos**</span><span class="sxs-lookup"><span data-stu-id="b9cc4-131">**Close**</span></span>](iscardfileaccess-close.md)                             | <span data-ttu-id="b9cc4-132">Cierra el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="b9cc4-132">Closes the specified file.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="b9cc4-133">**A**</span><span class="sxs-lookup"><span data-stu-id="b9cc4-133">**Create**</span></span>](iscardfileaccess-create.md)                           | <span data-ttu-id="b9cc4-134">Crea un archivo en una ubicación determinada dentro del sistema de archivos ICC.</span><span class="sxs-lookup"><span data-stu-id="b9cc4-134">Creates a file at a given location within the ICC file system.</span></span><br/>                                                                    |
| [<span data-ttu-id="b9cc4-135">**Elimínelos**</span><span class="sxs-lookup"><span data-stu-id="b9cc4-135">**Delete**</span></span>](iscardfileaccess-delete.md)                           | <span data-ttu-id="b9cc4-136">Elimina un archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="b9cc4-136">Deletes a specified file.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="b9cc4-137">**Directorio**</span><span class="sxs-lookup"><span data-stu-id="b9cc4-137">**Directory**</span></span>](iscardfileaccess-directory.md)                     | <span data-ttu-id="b9cc4-138">Recupera una lista de archivos.</span><span class="sxs-lookup"><span data-stu-id="b9cc4-138">Retrieves a list of files.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="b9cc4-139">**GetCurrentDir**</span><span class="sxs-lookup"><span data-stu-id="b9cc4-139">**GetCurrentDir**</span></span>](iscardfileaccess-getcurrentdir.md)             | <span data-ttu-id="b9cc4-140">Devuelve una ruta de acceso absoluta al directorio seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="b9cc4-140">Returns an absolute path to the currently selected directory.</span></span><br/>                                                                     |
| [<span data-ttu-id="b9cc4-141">**GetFileCapabilities**</span><span class="sxs-lookup"><span data-stu-id="b9cc4-141">**GetFileCapabilities**</span></span>](iscardfileaccess-getfilecapabilities.md) | <span data-ttu-id="b9cc4-142">Recupera las capacidades del archivo.</span><span class="sxs-lookup"><span data-stu-id="b9cc4-142">Retrieves file capabilities.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="b9cc4-143">**GetProperties**</span><span class="sxs-lookup"><span data-stu-id="b9cc4-143">**GetProperties**</span></span>](iscardfileaccess-getproperties.md)             | <span data-ttu-id="b9cc4-144">Recupera los datos primitivos a los que se hace referencia mediante etiquetas para el objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="b9cc4-144">Retrieves the primitive data referred by tags for the specified object.</span></span><br/>                                                           |
| [<span data-ttu-id="b9cc4-145">**Invalidar**</span><span class="sxs-lookup"><span data-stu-id="b9cc4-145">**Invalidate**</span></span>](iscardfileaccess-invalidate.md)                   | <span data-ttu-id="b9cc4-146">Hace que el archivo especificado no sea válido.</span><span class="sxs-lookup"><span data-stu-id="b9cc4-146">Makes the specified file not valid.</span></span><br/>                                                                                               |
| [<span data-ttu-id="b9cc4-147">**Ábra**</span><span class="sxs-lookup"><span data-stu-id="b9cc4-147">**Open**</span></span>](iscardfileaccess-open.md)                               | <span data-ttu-id="b9cc4-148">Abre el archivo especificado para su uso posterior.</span><span class="sxs-lookup"><span data-stu-id="b9cc4-148">Opens the specified file for further use.</span></span><br/>                                                                                         |
| [<span data-ttu-id="b9cc4-149">**Lectura**</span><span class="sxs-lookup"><span data-stu-id="b9cc4-149">**Read**</span></span>](iscardfileaccess-read.md)                               | <span data-ttu-id="b9cc4-150">Lee y devuelve los datos especificados de un archivo determinado.</span><span class="sxs-lookup"><span data-stu-id="b9cc4-150">Reads and returns the specified data from a given file.</span></span><br/>                                                                           |
| [<span data-ttu-id="b9cc4-151">**Rehabilitate**</span><span class="sxs-lookup"><span data-stu-id="b9cc4-151">**Rehabilitate**</span></span>](iscardfileaccess-rehabilitate.md)               | <span data-ttu-id="b9cc4-152">Crea un archivo (EF o DF), que previamente se ha convertido en no válido mediante el comando Invalidate, al que puede tener acceso la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b9cc4-152">Makes a file (EF or DF), which has been previously made not valid by using the Invalidate command, accessible by the application.</span></span><br/> |
| [<span data-ttu-id="b9cc4-153">**Seek**</span><span class="sxs-lookup"><span data-stu-id="b9cc4-153">**Seek**</span></span>](iscardfileaccess-seek.md)                               | <span data-ttu-id="b9cc4-154">Selecciona el objeto del que se realizará el permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b9cc4-154">Selects the object from which read/write permission will be done.</span></span><br/>                                                                 |
| [<span data-ttu-id="b9cc4-155">**SetProperties**</span><span class="sxs-lookup"><span data-stu-id="b9cc4-155">**SetProperties**</span></span>](iscardfileaccess-setproperties.md)             | <span data-ttu-id="b9cc4-156">Establece los datos primitivos a los que se hace referencia mediante etiquetas para el objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="b9cc4-156">Sets the primitive data referred by tags for the specified object.</span></span><br/>                                                                |
| [<span data-ttu-id="b9cc4-157">**Escritura**</span><span class="sxs-lookup"><span data-stu-id="b9cc4-157">**Write**</span></span>](iscardfileaccess-write.md)                             | <span data-ttu-id="b9cc4-158">Escribe datos en un archivo abierto actual.</span><span class="sxs-lookup"><span data-stu-id="b9cc4-158">Writes data to a current opened file.</span></span><br/>                                                                                             |



 

## <a name="requirements"></a><span data-ttu-id="b9cc4-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9cc4-159">Requirements</span></span>



| <span data-ttu-id="b9cc4-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9cc4-160">Requirement</span></span> | <span data-ttu-id="b9cc4-161">Value</span><span class="sxs-lookup"><span data-stu-id="b9cc4-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b9cc4-162">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9cc4-162">Minimum supported client</span></span><br/> | <span data-ttu-id="b9cc4-163">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="b9cc4-163">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="b9cc4-164">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9cc4-164">Minimum supported server</span></span><br/> | <span data-ttu-id="b9cc4-165">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b9cc4-165">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b9cc4-166">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="b9cc4-166">End of client support</span></span><br/>    | <span data-ttu-id="b9cc4-167">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b9cc4-167">Windows XP</span></span><br/>                                |
| <span data-ttu-id="b9cc4-168">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="b9cc4-168">End of server support</span></span><br/>    | <span data-ttu-id="b9cc4-169">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b9cc4-169">Windows Server 2003</span></span><br/>                       |



 

 
