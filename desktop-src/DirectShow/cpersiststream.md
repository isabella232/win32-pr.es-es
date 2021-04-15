---
description: CPersistStream es la clase base para las propiedades persistentes de los filtros (es decir, las propiedades de filtro en los gráficos guardados).
ms.assetid: 8073e2be-aaf9-4b01-a7d5-bab5c1dcc19b
title: Clase CPersistStream
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream
api_type:
- COM
api_location: ''
ms.openlocfilehash: 690a0f45fab7c3612d215a859798460abc81728e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536741"
---
# <a name="cpersiststream-class"></a><span data-ttu-id="7abcf-103">Clase CPersistStream</span><span class="sxs-lookup"><span data-stu-id="7abcf-103">CPersistStream class</span></span>

![jerarquía de clases cpersiststream](images/pstrm01.png)

<span data-ttu-id="7abcf-105">`CPersistStream` es la clase base para las propiedades persistentes de los filtros (es decir, las propiedades de filtro en los gráficos guardados).</span><span class="sxs-lookup"><span data-stu-id="7abcf-105">`CPersistStream` is the base class for persistent properties of filters (that is, filter properties in saved graphs).</span></span>

<span data-ttu-id="7abcf-106">La manera más sencilla de usar `CPersistStream` es:</span><span class="sxs-lookup"><span data-stu-id="7abcf-106">The simplest way to use `CPersistStream` is to:</span></span>

1.  <span data-ttu-id="7abcf-107">Organice para que el filtro herede esta clase.</span><span class="sxs-lookup"><span data-stu-id="7abcf-107">Arrange for your filter to inherit this class.</span></span>
2.  <span data-ttu-id="7abcf-108">Implemente [**WriteToStream**](cpersiststream-writetostream.md) y [**ReadFromStream**](cpersiststream-readfromstream.md) en la clase.</span><span class="sxs-lookup"><span data-stu-id="7abcf-108">Implement [**WriteToStream**](cpersiststream-writetostream.md) and [**ReadFromStream**](cpersiststream-readfromstream.md) in your class.</span></span> <span data-ttu-id="7abcf-109">Estos invalidarán las funciones aquí, que no hacen nada pero actúan como marcadores de posición.</span><span class="sxs-lookup"><span data-stu-id="7abcf-109">These will override the functions here, which do nothing but act as placeholders.</span></span>
3.  <span data-ttu-id="7abcf-110">Cambie **NonDelegatingQueryInterface** para controlar **IPersistStream**.</span><span class="sxs-lookup"><span data-stu-id="7abcf-110">Change your **NonDelegatingQueryInterface** to handle **IPersistStream**.</span></span>
4.  <span data-ttu-id="7abcf-111">Implemente [**SizeMax**](cpersiststream-sizemax.md) para devolver un límite superior en el número de bytes de datos que se guardan.</span><span class="sxs-lookup"><span data-stu-id="7abcf-111">Implement [**SizeMax**](cpersiststream-sizemax.md) to return an upper bound on the number of bytes of data you save.</span></span>

    <span data-ttu-id="7abcf-112">Si guarda datos de™ Unicode, recuerde que WCHAR tiene 2 bytes.</span><span class="sxs-lookup"><span data-stu-id="7abcf-112">If you save Unicode™ data, remember that a WCHAR is 2 bytes.</span></span>

5.  <span data-ttu-id="7abcf-113">Cuando cambien los datos, llame a [**SetDirty**](cpersiststream-setdirty.md).</span><span class="sxs-lookup"><span data-stu-id="7abcf-113">When your data changes, call [**SetDirty**](cpersiststream-setdirty.md).</span></span>

## <a name="version-numbers"></a><span data-ttu-id="7abcf-114">Números de versión</span><span class="sxs-lookup"><span data-stu-id="7abcf-114">Version Numbers</span></span>

<span data-ttu-id="7abcf-115">En algún momento puede decidir modificar o ampliar el formato de los datos.</span><span class="sxs-lookup"><span data-stu-id="7abcf-115">At some point you might decide to alter or extend the format of your data.</span></span> <span data-ttu-id="7abcf-116">A continuación, le interesará tener un número de versión en todas las secuencias guardadas antiguas para que pueda saber cuándo las Lee, si representan el formulario antiguo o nuevo.</span><span class="sxs-lookup"><span data-stu-id="7abcf-116">You will then wish you had a version number in all the old saved streams so you can tell, when you read them, whether they represent the old or new form.</span></span> <span data-ttu-id="7abcf-117">Para ayudarle, esta clase escribe y lee un número de versión.</span><span class="sxs-lookup"><span data-stu-id="7abcf-117">To assist you, this class writes and reads a version number.</span></span> <span data-ttu-id="7abcf-118">Cuando escribe, llama a [**GetSoftwareVersion**](cpersiststream-getsoftwareversion.md) para consultar la versión del software que se usa en ese momento.</span><span class="sxs-lookup"><span data-stu-id="7abcf-118">When it writes, it calls [**GetSoftwareVersion**](cpersiststream-getsoftwareversion.md) to inquire as to the version of the software being used at the moment.</span></span> <span data-ttu-id="7abcf-119">(En efecto, se trata de un número de versión del diseño de datos en el archivo). Escribe esto como la primera cosa en los datos.</span><span class="sxs-lookup"><span data-stu-id="7abcf-119">(In effect, this is a version number of the data layout in the file.) It writes this as the first thing in the data.</span></span> <span data-ttu-id="7abcf-120">Si desea cambiar la versión, implemente (invalide) **GetSoftwareVersion**.</span><span class="sxs-lookup"><span data-stu-id="7abcf-120">If you want to change the version, implement (override) **GetSoftwareVersion**.</span></span> <span data-ttu-id="7abcf-121">Lee el número de versión del archivo en **MP \_ dwFileVersion** antes de llamar a [**ReadFromStream**](cpersiststream-readfromstream.md), por lo que en **ReadFromStream** puede comprobar **MPS \_ dwFileVersion** para ver si está leyendo un archivo de versión anterior.</span><span class="sxs-lookup"><span data-stu-id="7abcf-121">It reads the version number from the file into **mPS\_dwFileVersion** before calling [**ReadFromStream**](cpersiststream-readfromstream.md), so in **ReadFromStream** you can check **mPS\_dwFileVersion** to see if you are reading an old version file.</span></span> <span data-ttu-id="7abcf-122">Normalmente, debe aceptar archivos cuya versión no sea más reciente que la versión de software que los Lee.</span><span class="sxs-lookup"><span data-stu-id="7abcf-122">Usually you should accept files whose version is no newer than the software version that is reading them.</span></span>

<span data-ttu-id="7abcf-123">**CPersistStream** implementa [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream).</span><span class="sxs-lookup"><span data-stu-id="7abcf-123">**CPersistStream** implements [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream).</span></span> <span data-ttu-id="7abcf-124">Para obtener más información sobre la implementación, vea la referencia de COM en el SDK de la plataforma de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7abcf-124">For more implementation information, see the COM Reference in the Microsoft Platform SDK.</span></span>



| <span data-ttu-id="7abcf-125">Miembros de datos protegidos</span><span class="sxs-lookup"><span data-stu-id="7abcf-125">Protected Data Members</span></span>                                          | <span data-ttu-id="7abcf-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="7abcf-126">Description</span></span>                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="7abcf-127">dwFileVersion de mPS \_</span><span class="sxs-lookup"><span data-stu-id="7abcf-127">mPS\_dwFileVersion</span></span>                                              | <span data-ttu-id="7abcf-128">Número de versión del archivo.</span><span class="sxs-lookup"><span data-stu-id="7abcf-128">Version number of the file.</span></span>                                                   |
| <span data-ttu-id="7abcf-129">fDirty de mPS \_</span><span class="sxs-lookup"><span data-stu-id="7abcf-129">mPS\_fDirty</span></span>                                                     | <span data-ttu-id="7abcf-130">Los datos de esta secuencia se deben guardar.</span><span class="sxs-lookup"><span data-stu-id="7abcf-130">Data for this stream must be saved.</span></span>                                           |
| <span data-ttu-id="7abcf-131">Funciones de miembro</span><span class="sxs-lookup"><span data-stu-id="7abcf-131">Member Functions</span></span>                                                | <span data-ttu-id="7abcf-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="7abcf-132">Description</span></span>                                                                   |
| [<span data-ttu-id="7abcf-133">**CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="7abcf-133">**CPersistStream**</span></span>](cpersiststream-cpersiststream.md)         | <span data-ttu-id="7abcf-134">Construye un objeto **CPersistStream** .</span><span class="sxs-lookup"><span data-stu-id="7abcf-134">Constructs a **CPersistStream** object.</span></span>                                       |
| [<span data-ttu-id="7abcf-135">**SetDirty**</span><span class="sxs-lookup"><span data-stu-id="7abcf-135">**SetDirty**</span></span>](cpersiststream-setdirty.md)                     | <span data-ttu-id="7abcf-136">Indica que el objeto se debe guardar en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="7abcf-136">Indicates that the object must be saved to the stream.</span></span>                        |
| <span data-ttu-id="7abcf-137">Funciones miembro reemplazables</span><span class="sxs-lookup"><span data-stu-id="7abcf-137">Overridable Member Functions</span></span>                                    | <span data-ttu-id="7abcf-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="7abcf-138">Description</span></span>                                                                   |
| [<span data-ttu-id="7abcf-139">**GetClassID**</span><span class="sxs-lookup"><span data-stu-id="7abcf-139">**GetClassID**</span></span>](cpersiststream-getclassid.md)                 | <span data-ttu-id="7abcf-140">Recupera el identificador de clase de esta secuencia.</span><span class="sxs-lookup"><span data-stu-id="7abcf-140">Retrieves the class identifier of this stream.</span></span>                                |
| [<span data-ttu-id="7abcf-141">**GetSoftwareVersion**</span><span class="sxs-lookup"><span data-stu-id="7abcf-141">**GetSoftwareVersion**</span></span>](cpersiststream-getsoftwareversion.md) | <span data-ttu-id="7abcf-142">Recupera el número de versión de este formato de archivo.</span><span class="sxs-lookup"><span data-stu-id="7abcf-142">Retrieves the version number for this file format.</span></span>                            |
| [<span data-ttu-id="7abcf-143">**ReadFromStream**</span><span class="sxs-lookup"><span data-stu-id="7abcf-143">**ReadFromStream**</span></span>](cpersiststream-readfromstream.md)         | <span data-ttu-id="7abcf-144">Lee los datos del filtro de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="7abcf-144">Reads the filter's data from the stream.</span></span>                                      |
| [<span data-ttu-id="7abcf-145">**SizeMax**</span><span class="sxs-lookup"><span data-stu-id="7abcf-145">**SizeMax**</span></span>](cpersiststream-sizemax.md)                       | <span data-ttu-id="7abcf-146">Recupera el número de bytes necesarios para los datos (sin incluir el número de versión).</span><span class="sxs-lookup"><span data-stu-id="7abcf-146">Retrieves the number of bytes needed for data (not including version number).</span></span> |
| [<span data-ttu-id="7abcf-147">**WriteToStream**</span><span class="sxs-lookup"><span data-stu-id="7abcf-147">**WriteToStream**</span></span>](cpersiststream-writetostream.md)           | <span data-ttu-id="7abcf-148">Escribe los datos del filtro en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="7abcf-148">Writes the filter's data to the stream.</span></span>                                       |
| <span data-ttu-id="7abcf-149">Métodos IPersistStream</span><span class="sxs-lookup"><span data-stu-id="7abcf-149">IPersistStream Methods</span></span>                                          | <span data-ttu-id="7abcf-150">Descripción</span><span class="sxs-lookup"><span data-stu-id="7abcf-150">Description</span></span>                                                                   |
| [<span data-ttu-id="7abcf-151">**GetSizeMax**</span><span class="sxs-lookup"><span data-stu-id="7abcf-151">**GetSizeMax**</span></span>](cpersiststream-getsizemax.md)                 | <span data-ttu-id="7abcf-152">Recupera el número de bytes necesarios para los datos (incluido el número de versión).</span><span class="sxs-lookup"><span data-stu-id="7abcf-152">Retrieves the number of bytes needed for data (including version number).</span></span>     |
| [<span data-ttu-id="7abcf-153">**IsDirty**</span><span class="sxs-lookup"><span data-stu-id="7abcf-153">**IsDirty**</span></span>](cpersiststream-isdirty.md)                       | <span data-ttu-id="7abcf-154">Comprueba si se debe guardar el objeto.</span><span class="sxs-lookup"><span data-stu-id="7abcf-154">Checks if the object must be saved.</span></span>                                           |
| [<span data-ttu-id="7abcf-155">**Cargar**</span><span class="sxs-lookup"><span data-stu-id="7abcf-155">**Load**</span></span>](cpersiststream-load.md)                             | <span data-ttu-id="7abcf-156">Carga los datos de la secuencia en la memoria.</span><span class="sxs-lookup"><span data-stu-id="7abcf-156">Loads the data from the stream into memory.</span></span>                                   |
| [<span data-ttu-id="7abcf-157">**Guardar**</span><span class="sxs-lookup"><span data-stu-id="7abcf-157">**Save**</span></span>](cpersiststream-save.md)                             | <span data-ttu-id="7abcf-158">Guarda los datos de la memoria en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="7abcf-158">Saves the data from memory to the stream.</span></span>                                     |



 

 

 
