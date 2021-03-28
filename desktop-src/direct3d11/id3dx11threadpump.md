---
title: Interfaz ID3DX11ThreadPump (D3DX11core. h)
description: Un bombeo de subprocesos ejecuta las tareas de forma asincrónica.
ms.assetid: 1a99f728-149d-4800-a6e4-e3a00cf8cf4f
keywords:
- Interfaz ID3DX11ThreadPump Direct3D 11
- Interfaz ID3DX11ThreadPump Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b60cedaa4ef84cb9f3ea31cd619d7335cc09324e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149988"
---
# <a name="id3dx11threadpump-interface"></a><span data-ttu-id="25db8-105">Interfaz ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="25db8-105">ID3DX11ThreadPump interface</span></span>

> [!Note]  
> <span data-ttu-id="25db8-106">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="25db8-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="25db8-107">Un bombeo de subprocesos ejecuta las tareas de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="25db8-107">A thread pump executes tasks asynchronously.</span></span> <span data-ttu-id="25db8-108">Se crea llamando a [**D3DX11CreateThreadPump**](d3dx11createthreadpump.md).</span><span class="sxs-lookup"><span data-stu-id="25db8-108">It is created by calling [**D3DX11CreateThreadPump**](d3dx11createthreadpump.md).</span></span> <span data-ttu-id="25db8-109">Hay varias API que toman un bombeo de subprocesos opcional como parámetro, como [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) y [**D3DX11CompileFromFile**](d3dx11compilefromfile.md). Si pasa una interfaz de bombeo de subprocesos a estas API, las funciones se ejecutarán de forma asincrónica en un subproceso independiente.</span><span class="sxs-lookup"><span data-stu-id="25db8-109">There are several APIs that take an optional thread pump as a parameter, such as [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) and [**D3DX11CompileFromFile**](d3dx11compilefromfile.md); if you pass a thread pump interface into these APIs, the functions will execute asynchronously on a separate thread.</span></span> <span data-ttu-id="25db8-110">Especialmente en equipos con varios procesadores, un bombeo de subprocesos puede cargar recursos y procesar datos sin una disminución apreciable en el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="25db8-110">Particularly on multiprocessor machines, a thread pump can load resources and process data without a noticeable decrease in performance.</span></span>

## <a name="members"></a><span data-ttu-id="25db8-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="25db8-111">Members</span></span>

<span data-ttu-id="25db8-112">La interfaz **ID3DX11ThreadPump** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="25db8-112">The **ID3DX11ThreadPump** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="25db8-113">**ID3DX11ThreadPump** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="25db8-113">**ID3DX11ThreadPump** also has these types of members:</span></span>

-   [<span data-ttu-id="25db8-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="25db8-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="25db8-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="25db8-115">Methods</span></span>

<span data-ttu-id="25db8-116">La interfaz **ID3DX11ThreadPump** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="25db8-116">The **ID3DX11ThreadPump** interface has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="25db8-117">Método</span><span class="sxs-lookup"><span data-stu-id="25db8-117">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="25db8-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="25db8-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="25db8-119"><a href="id3dx11threadpump-addworkitem.md"><strong>AddWorkItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="25db8-119"><a href="id3dx11threadpump-addworkitem.md"><strong>AddWorkItem</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="25db8-120">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="25db8-120">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="25db8-121">Agrega un elemento de trabajo al bombeo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="25db8-121">Adds a work item to the thread pump.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="25db8-122"><a href="id3dx11threadpump-getqueuestatus.md"><strong>GetQueueStatus</strong></a></span><span class="sxs-lookup"><span data-stu-id="25db8-122"><a href="id3dx11threadpump-getqueuestatus.md"><strong>GetQueueStatus</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="25db8-123">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="25db8-123">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="25db8-124">Obtiene el número de elementos de cada una de las tres colas dentro del bombeo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="25db8-124">Gets the number of items in each of the three queues inside the thread pump.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="25db8-125"><a href="id3dx11threadpump-getworkitemcount.md"><strong>GetWorkItemCount</strong></a></span><span class="sxs-lookup"><span data-stu-id="25db8-125"><a href="id3dx11threadpump-getworkitemcount.md"><strong>GetWorkItemCount</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="25db8-126">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="25db8-126">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="25db8-127">Obtiene el número de elementos de trabajo en el bombeo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="25db8-127">Gets the number of work items in the thread pump.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="25db8-128"><a href="id3dx11threadpump-processdeviceworkitems.md"><strong>ProcessDeviceWorkItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="25db8-128"><a href="id3dx11threadpump-processdeviceworkitems.md"><strong>ProcessDeviceWorkItems</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="25db8-129">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="25db8-129">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="25db8-130">Establece los elementos de trabajo en el dispositivo una vez que han finalizado la carga y el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="25db8-130">Sets work items to the device after they have finished loading and processing.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="25db8-131"><a href="id3dx11threadpump-purgeallitems.md"><strong>PurgeAllItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="25db8-131"><a href="id3dx11threadpump-purgeallitems.md"><strong>PurgeAllItems</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="25db8-132">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="25db8-132">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="25db8-133">Borra todos los elementos de trabajo del bombeo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="25db8-133">Clears all work items from the thread pump.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="25db8-134"><a href="id3dx11threadpump-waitforallitems.md"><strong>WaitForAllItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="25db8-134"><a href="id3dx11threadpump-waitforallitems.md"><strong>WaitForAllItems</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="25db8-135">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="25db8-135">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="25db8-136">Espera a que finalicen todos los elementos de trabajo en el bombeo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="25db8-136">Waits for all work items in the thread pump to finish.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="25db8-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="25db8-137">Remarks</span></span>

### <a name="using-a-thread-pump"></a><span data-ttu-id="25db8-138">Usar un bombeo de subprocesos</span><span class="sxs-lookup"><span data-stu-id="25db8-138">Using a Thread Pump</span></span>

<span data-ttu-id="25db8-139">El bombeo de subprocesos carga y procesa los datos mediante el siguiente proceso de tres pasos:</span><span class="sxs-lookup"><span data-stu-id="25db8-139">The thread pump loads and processes data using the following three-step process:</span></span>

1.  <span data-ttu-id="25db8-140">Cargar y descomprimir los datos con un [**cargador de datos**](id3dx11dataloader.md).</span><span class="sxs-lookup"><span data-stu-id="25db8-140">Load and decompress the data with a [**Data Loader**](id3dx11dataloader.md).</span></span> <span data-ttu-id="25db8-141">El objeto del cargador de datos tiene tres métodos a los que el bombeo de subprocesos llamará internamente a medida que se cargan y descomprimen los datos: [**ID3DX11DataLoader:: Load**](id3dx11dataloader-load.md), [**ID3DX11DataLoader::D ecompress**](id3dx11dataloader-decompress.md)y [**ID3DX11DataLoader::D estroy**](id3dx11dataloader-destroy.md).</span><span class="sxs-lookup"><span data-stu-id="25db8-141">The data loader object has three methods that the thread pump will call internally as it is loading and decompressing the data: [**ID3DX11DataLoader::Load**](id3dx11dataloader-load.md), [**ID3DX11DataLoader::Decompress**](id3dx11dataloader-decompress.md), and [**ID3DX11DataLoader::Destroy**](id3dx11dataloader-destroy.md).</span></span> <span data-ttu-id="25db8-142">La funcionalidad específica de estas tres API varía en función del tipo de datos que se cargan y descomprimen.</span><span class="sxs-lookup"><span data-stu-id="25db8-142">The specific functionality of these three APIs differs depending on the type of data being loaded and decompressed.</span></span> <span data-ttu-id="25db8-143">También se puede heredar la interfaz del cargador de datos y se pueden cambiar sus API si se está cargando un archivo de datos definido en un formato personalizado propio.</span><span class="sxs-lookup"><span data-stu-id="25db8-143">The data loader interface can also be inherited and its APIs can be changed if one is loading a data file defined in one's own custom format.</span></span>
2.  <span data-ttu-id="25db8-144">Procese los datos con un [**procesador de datos**](id3dx11dataprocessor.md).</span><span class="sxs-lookup"><span data-stu-id="25db8-144">Process the data with a [**Data Processor**](id3dx11dataprocessor.md).</span></span> <span data-ttu-id="25db8-145">El objeto de procesador de datos tiene tres métodos a los que el bombeo de subprocesos llamará internamente a medida que procesa los datos: [**ID3DX11DataProcessor::P rador**](id3dx11dataprocessor-process.md), [**ID3DX11DataProcessor:: CreateDeviceObject**](id3dx11dataprocessor-createdeviceobject.md)y [**ID3DX11DataProcessor::D estroy**](id3dx11dataprocessor-destroy.md).</span><span class="sxs-lookup"><span data-stu-id="25db8-145">The data processor object has three methods that the thread pump will call internally as it is processing the data: [**ID3DX11DataProcessor::Process**](id3dx11dataprocessor-process.md), [**ID3DX11DataProcessor::CreateDeviceObject**](id3dx11dataprocessor-createdeviceobject.md), and [**ID3DX11DataProcessor::Destroy**](id3dx11dataprocessor-destroy.md).</span></span> <span data-ttu-id="25db8-146">La forma en que se procesan los datos será diferente en función del tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="25db8-146">The way it processes the data will be different depending on the type of data.</span></span> <span data-ttu-id="25db8-147">Por ejemplo, si los datos son una textura almacenada como JPEG, [**ID3DX11DataProcessor::P rador**](id3dx11dataprocessor-process.md) realizará la descompresión JPEG para obtener los bits de imagen sin formato de la imagen.</span><span class="sxs-lookup"><span data-stu-id="25db8-147">For example, if the data is a texture stored as a JPEG, then [**ID3DX11DataProcessor::Process**](id3dx11dataprocessor-process.md) will do JPEG decompression to get the image's raw image bits.</span></span> <span data-ttu-id="25db8-148">Si los datos son un sombreador, [**ID3DX11DataProcessor::P rador**](id3dx11dataprocessor-process.md) compilará el HLSL en código de bytes.</span><span class="sxs-lookup"><span data-stu-id="25db8-148">If the data is a shader, then [**ID3DX11DataProcessor::Process**](id3dx11dataprocessor-process.md) will compile the HLSL into bytecode.</span></span> <span data-ttu-id="25db8-149">Una vez procesados los datos, se creará un objeto de dispositivo para esos datos (con [**ID3DX11DataProcessor:: CreateDeviceObject**](id3dx11dataprocessor-createdeviceobject.md)) y el objeto se agregará a una cola de objetos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="25db8-149">After the data has been processed a device object will be created for that data (with [**ID3DX11DataProcessor::CreateDeviceObject**](id3dx11dataprocessor-createdeviceobject.md)) and the object will be added to a queue of device objects.</span></span> <span data-ttu-id="25db8-150">También se puede heredar la interfaz del procesador de datos y se pueden cambiar sus API si se está procesando un archivo de datos definido en un formato personalizado propio.</span><span class="sxs-lookup"><span data-stu-id="25db8-150">The data processor interface can also be inherited and its APIs can be changed if one is processing a data file defined in one's own custom format.</span></span>
3.  <span data-ttu-id="25db8-151">Enlazar el objeto de dispositivo al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="25db8-151">Bind the device object to the device.</span></span> <span data-ttu-id="25db8-152">Esto se hace cuando una aplicación de una de las llamadas a [**ID3DX11ThreadPump::P rocessdeviceworkitems**](id3dx11threadpump-processdeviceworkitems.md), que enlazará un número especificado de objetos en la cola de objetos de dispositivo al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="25db8-152">This is done when one's application calls [**ID3DX11ThreadPump::ProcessDeviceWorkItems**](id3dx11threadpump-processdeviceworkitems.md), which will bind a specified number of objects in the queue of device objects to the device.</span></span>

<span data-ttu-id="25db8-153">El bombeo de subprocesos se puede utilizar para cargar datos de una de las dos maneras siguientes: llamando a una API que toma un bombeo de subprocesos como parámetro, como [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) y [**D3DX11CompileFromFile**](d3dx11compilefromfile.md), o llamando a [**ID3DX11ThreadPump:: AddWorkItem**](id3dx11threadpump-addworkitem.md).</span><span class="sxs-lookup"><span data-stu-id="25db8-153">The thread pump can be used to load data in one of two ways: by calling an API that takes a thread pump as a parameter, such as [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) and [**D3DX11CompileFromFile**](d3dx11compilefromfile.md), or by calling [**ID3DX11ThreadPump::AddWorkItem**](id3dx11threadpump-addworkitem.md).</span></span> <span data-ttu-id="25db8-154">En el caso de las API que toman un bombeo de subprocesos, el cargador de datos y el procesador de datos se crean internamente.</span><span class="sxs-lookup"><span data-stu-id="25db8-154">In the case of the APIs that take a thread pump, the data loader and data processor are created internally.</span></span> <span data-ttu-id="25db8-155">En el caso de AddWorkItem, el cargador de datos y el procesador de datos se deben crear de antemano y, a continuación, pasarse a AddWorkItem.</span><span class="sxs-lookup"><span data-stu-id="25db8-155">In the case of AddWorkItem, the data loader and data processor must be created beforehand and are then passed into AddWorkItem.</span></span> <span data-ttu-id="25db8-156">D3DX11 proporciona un conjunto de API para crear cargadores de datos y procesadores de datos que tienen funcionalidad para cargar y procesar formatos de datos comunes.</span><span class="sxs-lookup"><span data-stu-id="25db8-156">D3DX11 provides a set of APIs for creating data loaders and data processors that have functionality for loading and processing common data formats.</span></span> <span data-ttu-id="25db8-157">En el caso de los formatos de datos personalizados, las interfaces del cargador de datos y del procesador de datos deben heredarse y sus métodos deben redefinirse.</span><span class="sxs-lookup"><span data-stu-id="25db8-157">For custom data formats, the data loader and data processor interfaces must be inherited and their methods must be redefined.</span></span>

<span data-ttu-id="25db8-158">El objeto de bombeo de subprocesos ocupa una cantidad considerable de recursos, por lo que generalmente solo se debe crear uno por aplicación.</span><span class="sxs-lookup"><span data-stu-id="25db8-158">The thread pump object takes up a substantial amount of resources, so generally only one should be created per application.</span></span>

## <a name="requirements"></a><span data-ttu-id="25db8-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25db8-159">Requirements</span></span>



| <span data-ttu-id="25db8-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="25db8-160">Requirement</span></span> | <span data-ttu-id="25db8-161">Value</span><span class="sxs-lookup"><span data-stu-id="25db8-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25db8-162">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25db8-162">Minimum supported client</span></span><br/> | <span data-ttu-id="25db8-163">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="25db8-163">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="25db8-164">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25db8-164">Minimum supported server</span></span><br/> | <span data-ttu-id="25db8-165">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="25db8-165">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="25db8-166">Encabezado</span><span class="sxs-lookup"><span data-stu-id="25db8-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="25db8-167"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="25db8-167"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="25db8-168">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="25db8-168">Library</span></span><br/>                  | <dl> <span data-ttu-id="25db8-169"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="25db8-169"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="25db8-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="25db8-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25db8-171">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="25db8-171">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

