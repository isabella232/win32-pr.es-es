---
title: Ciclo de vida de la instancia de virtualización
description: Información general sobre el ciclo de vida de una instancia de virtualización de ProjFS.
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/17/2018
ms.topic: article
ms.openlocfilehash: 567eff1f7b8acf330dba7c652e2e12b724072b9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533238"
---
# <a name="virtualization-instance-lifecycle"></a><span data-ttu-id="dfadb-103">Ciclo de vida de la instancia de virtualización</span><span class="sxs-lookup"><span data-stu-id="dfadb-103">Virtualization Instance Lifecycle</span></span>

<span data-ttu-id="dfadb-104">La aplicación de proveedor mantiene una o más instancias de virtualización.</span><span class="sxs-lookup"><span data-stu-id="dfadb-104">The provider application maintains one or more virtualization instances.</span></span>  <span data-ttu-id="dfadb-105">Cada instancia de virtualización pasa por cuatro fases en su ciclo de vida:</span><span class="sxs-lookup"><span data-stu-id="dfadb-105">Each virtualization instance goes through four stages in its lifecycle:</span></span>

1. <span data-ttu-id="dfadb-106">Creación</span><span class="sxs-lookup"><span data-stu-id="dfadb-106">Creation</span></span>
2. <span data-ttu-id="dfadb-107">Inicio</span><span class="sxs-lookup"><span data-stu-id="dfadb-107">Startup</span></span>
3. <span data-ttu-id="dfadb-108">Tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="dfadb-108">Runtime</span></span>
4. <span data-ttu-id="dfadb-109">Apagar</span><span class="sxs-lookup"><span data-stu-id="dfadb-109">Shutdown</span></span>

<span data-ttu-id="dfadb-110">Tenga en cuenta que después de apagar una instancia de virtualización, no es necesario que el proveedor vuelva a crearla para reutilizarla.</span><span class="sxs-lookup"><span data-stu-id="dfadb-110">Note that after shutting down a virtualization instance the provider does not need to re-create it to reuse it.</span></span>  <span data-ttu-id="dfadb-111">Simplemente puede iniciarla de nuevo.</span><span class="sxs-lookup"><span data-stu-id="dfadb-111">It can simply start it up again.</span></span>

> <span data-ttu-id="dfadb-112">**Nota**: en esta sección se muestran ejemplos de API de ProjFS.</span><span class="sxs-lookup"><span data-stu-id="dfadb-112">**Note**: This section shows examples of ProjFS APIs.</span></span>  <span data-ttu-id="dfadb-113">Cada ejemplo está pensado para ilustrar el uso básico de la API.</span><span class="sxs-lookup"><span data-stu-id="dfadb-113">Each example is meant to illustrate basic API usage.</span></span>  <span data-ttu-id="dfadb-114">Para ver la documentación de las opciones que no se usan en estos ejemplos, consulte la referencia de la [API de ProjFS](/windows/desktop/api/_projfs).</span><span class="sxs-lookup"><span data-stu-id="dfadb-114">For documentation of options unused in these examples please consult the [ProjFS API reference](/windows/desktop/api/_projfs).</span></span>

## <a name="creating-a-virtualization-root"></a><span data-ttu-id="dfadb-115">Crear una raíz de virtualización</span><span class="sxs-lookup"><span data-stu-id="dfadb-115">Creating a virtualization root</span></span>

<span data-ttu-id="dfadb-116">Para que un proveedor pueda iniciar la instancia de virtualización que va a proyectar los elementos en el sistema de archivos local, debe crear la raíz de virtualización.</span><span class="sxs-lookup"><span data-stu-id="dfadb-116">Before a provider can start up the virtualization instance that will project items into the local file system, it must create the virtualization root.</span></span>  <span data-ttu-id="dfadb-117">La raíz de virtualización es el directorio en el que el proveedor proyecta un árbol de directorios y archivos.</span><span class="sxs-lookup"><span data-stu-id="dfadb-117">The virtualization root is the directory under which the provider projects a tree of directories and files.</span></span>

<span data-ttu-id="dfadb-118">Para crear una raíz de virtualización, el proveedor debe:</span><span class="sxs-lookup"><span data-stu-id="dfadb-118">To create a virtualization root the provider must:</span></span>

1. <span data-ttu-id="dfadb-119">Cree un directorio para que sirva como raíz de virtualización.</span><span class="sxs-lookup"><span data-stu-id="dfadb-119">Create a directory to serve as the virtualization root.</span></span>

    <span data-ttu-id="dfadb-120">El proveedor crea un directorio para actuar como la raíz de virtualización mediante, por ejemplo, **[CreateDirectory](/windows/desktop/api/fileapi/nf-fileapi-createdirectoryw)**:</span><span class="sxs-lookup"><span data-stu-id="dfadb-120">The provider creates a directory to serve as the virtualization root using, for example **[CreateDirectory](/windows/desktop/api/fileapi/nf-fileapi-createdirectoryw)**:</span></span>

    ```C++
    HRESULT hr;
    const wchar_t* rootName = LR"(C:\virtRoot)";
    if (!CreateDirectoryW(rootName, nullptr))
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        wprintf(L"Failed to create virtualization root (0x%08x)\n", hr);
        return;
    }
    ```

1. <span data-ttu-id="dfadb-121">Cree un identificador de instancia de virtualización.</span><span class="sxs-lookup"><span data-stu-id="dfadb-121">Create a virtualization instance ID.</span></span>

    <span data-ttu-id="dfadb-122">Cada instancia de virtualización tiene un identificador único denominado _identificador de instancia de virtualización_.</span><span class="sxs-lookup"><span data-stu-id="dfadb-122">Every virtualization instance has a unique ID called the _virtualization instance ID_.</span></span>  <span data-ttu-id="dfadb-123">El sistema utiliza este valor para identificar a qué instancia de virtualización está asociada su contenido.</span><span class="sxs-lookup"><span data-stu-id="dfadb-123">The system uses this value to identify which virtualization instance its contents are associated to.</span></span>

    ```C++
    GUID instanceId;
    hr = CoCreateGuid(&instanceId);
    if (FAILED(hr))
    {
        wprintf(L"Failed to create instance ID (0x%08x)\n", hr);
        return;
    }
    ```

1. <span data-ttu-id="dfadb-124">Marque el nuevo directorio como la raíz de virtualización.</span><span class="sxs-lookup"><span data-stu-id="dfadb-124">Mark the new directory as the virtualization root.</span></span>

    <span data-ttu-id="dfadb-125">El proveedor llama a **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** para marcar el nuevo directorio como la raíz de virtualización y asignarlo a la instancia de virtualización.</span><span class="sxs-lookup"><span data-stu-id="dfadb-125">The provider calls **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** to mark the new directory as the virtualization root and assign it to the virtualization instance.</span></span>

    ```C++
    hr = PrjMarkDirectoryAsPlaceholder(rootName,
                                       nullptr,
                                       nullptr,
                                       &instanceId);
    if (FAILED(hr))
    {
        wprintf(L"Failed to mark virtualization root (0x%08x)\n", hr);
        return;
    }
    ```

<span data-ttu-id="dfadb-126">El proveedor solo necesita crear la raíz de virtualización una vez para cada instancia de virtualización.</span><span class="sxs-lookup"><span data-stu-id="dfadb-126">The provider only needs to create the virtualization root once for each virtualization instance.</span></span>  <span data-ttu-id="dfadb-127">Una vez creada una raíz, su instancia asociada puede iniciarse y detenerse repetidamente sin volver a crear la raíz.</span><span class="sxs-lookup"><span data-stu-id="dfadb-127">Once a root has been created, its associated instance can be repeatedly started and stopped without recreating the root.</span></span>

## <a name="starting-a-virtualization-instance"></a><span data-ttu-id="dfadb-128">Iniciar una instancia de virtualización</span><span class="sxs-lookup"><span data-stu-id="dfadb-128">Starting a virtualization instance</span></span>

<span data-ttu-id="dfadb-129">Una vez creada la raíz de virtualización, el proveedor debe iniciar la instancia de virtualización.</span><span class="sxs-lookup"><span data-stu-id="dfadb-129">Once the virtualization root has been created the provider must start the virtualization instance.</span></span>  <span data-ttu-id="dfadb-130">Esto indica a ProjFS que el proveedor está listo para recibir devoluciones de llamada y proporcionar datos.</span><span class="sxs-lookup"><span data-stu-id="dfadb-130">This signals ProjFS that the provider is ready to receive callbacks and provide data.</span></span>

<span data-ttu-id="dfadb-131">Para iniciar la instancia de virtualización, el proveedor debe:</span><span class="sxs-lookup"><span data-stu-id="dfadb-131">To start the virtualization instance the provider must:</span></span>

1. <span data-ttu-id="dfadb-132">Configure la tabla de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="dfadb-132">Set up the callback table.</span></span>

    <span data-ttu-id="dfadb-133">ProjFS se comunica con el proveedor mediante la invocación de rutinas de devolución de llamada implementadas por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="dfadb-133">ProjFS communicates with the provider by invoking callback routines implemented by the provider.</span></span>  <span data-ttu-id="dfadb-134">El proveedor rellena una [PRJ_CALLBACKS](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callbacks) struct con punteros a sus rutinas de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="dfadb-134">The provider populates a [PRJ_CALLBACKS](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callbacks) struct with pointers to its callback routines.</span></span>

    ```C++
    PRJ_CALLBACKS callbackTable;

    // Supply required callbacks.
    callbackTable.StartDirectoryEnumerationCallback = MyStartEnumCallback;
    callbackTable.EndDirectoryEnumerationCallback = MyEndEnumCallback;
    callbackTable.GetDirectoryEnumerationCallback = MyGetEnumCallback;
    callbackTable.GetPlaceholderInfoCallback = MyGetPlaceholderInfoCallback;
    callbackTable.GetFileDataCallback = MyGetFileDataCallback;

    // The rest of the callbacks are optional.
    callbackTable.QueryFileNameCallback = nullptr;
    callbackTable.NotificationCallback = nullptr;
    callbackTable.CancelCommandCallback = nullptr;
    ```

1. <span data-ttu-id="dfadb-135">Inicie la instancia de.</span><span class="sxs-lookup"><span data-stu-id="dfadb-135">Start the instance.</span></span>

    <span data-ttu-id="dfadb-136">El proveedor llama a **[PrjStartVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing)** para iniciar la instancia de virtualización.</span><span class="sxs-lookup"><span data-stu-id="dfadb-136">The provider calls **[PrjStartVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing)** to start the virtualization instance.</span></span>

    ```C++
    PRJ_NAMESPACE_VIRTUALIZATION_CONTEXT instanceHandle;
    hr = PrjStartVirtualizing(rootName,
                              &callbackTable,
                              nullptr,
                              nullptr,
                              &instanceHandle);
    if (FAILED(hr))
    {
        wprintf(L"Failed to start the virtualization instance (0x%08x)\n", hr);
        return;
    }
    ```
    <span data-ttu-id="dfadb-137">El parámetro _instanceHandle_ de **PrjStartVirtualizing** devuelve un identificador a la instancia de virtualización.</span><span class="sxs-lookup"><span data-stu-id="dfadb-137">**PrjStartVirtualizing**'s _instanceHandle_ parameter returns a handle to the virtualization instance.</span></span>  <span data-ttu-id="dfadb-138">El proveedor usa este controlador al llamar a otras API de ProjFS.</span><span class="sxs-lookup"><span data-stu-id="dfadb-138">The provider uses this handle when calling other ProjFS APIs.</span></span>

## <a name="virtualization-instance-runtime"></a><span data-ttu-id="dfadb-139">Tiempo de ejecución de instancia de virtualización</span><span class="sxs-lookup"><span data-stu-id="dfadb-139">Virtualization instance runtime</span></span>

<span data-ttu-id="dfadb-140">Una vez que se devuelve la llamada a **PrjStartVirtualizing** , ProjFS invocará las rutinas de devolución de llamada del proveedor en respuesta a las operaciones del sistema de archivos en la instancia de virtualización.</span><span class="sxs-lookup"><span data-stu-id="dfadb-140">Once the call to **PrjStartVirtualizing** returns, ProjFS will invoke the provider's callback routines in response to file system operations in the virtualization instance.</span></span>  <span data-ttu-id="dfadb-141">Para obtener información sobre cómo el proveedor puede controlar varias operaciones del sistema de archivos, consulte las secciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="dfadb-141">For information on how the provider can handle various file system operations, refer to the following sections:</span></span>

* [<span data-ttu-id="dfadb-142">Enumeración de archivos y directorios</span><span class="sxs-lookup"><span data-stu-id="dfadb-142">Enumerating Files and Directories</span></span>](enumerating-files-and-directories.md)
* [<span data-ttu-id="dfadb-143">Aprovisionamiento de datos de archivo</span><span class="sxs-lookup"><span data-stu-id="dfadb-143">Providing File Data</span></span>](providing-file-data.md)
* [<span data-ttu-id="dfadb-144">Notificaciones de operación del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="dfadb-144">File System Operation Notifications</span></span>](file-system-operation-notifications.md)
* [<span data-ttu-id="dfadb-145">Control de cambios de vista</span><span class="sxs-lookup"><span data-stu-id="dfadb-145">Handling View Changes</span></span>](handling-view-changes.md)

## <a name="shutting-down-a-virtualization-instance"></a><span data-ttu-id="dfadb-146">Cerrar una instancia de virtualización</span><span class="sxs-lookup"><span data-stu-id="dfadb-146">Shutting down a virtualization instance</span></span>

<span data-ttu-id="dfadb-147">Para indicar a ProjFS que el proveedor desea dejar de recibir devoluciones de llamada y proporcionar datos, el proveedor debe detener la instancia de virtualización.</span><span class="sxs-lookup"><span data-stu-id="dfadb-147">To signal ProjFS that the provider wants to stop receiving callbacks and providing data, the provider must stop the virtualization instance.</span></span>  <span data-ttu-id="dfadb-148">Para ello, el proveedor llama a **[PrjStopVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing)**, pasándole el identificador a la instancia de virtualización que recibió de la llamada a **PrjStartVirtualizing**.</span><span class="sxs-lookup"><span data-stu-id="dfadb-148">To do this the provider calls **[PrjStopVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing)**, passing it the handle to the virtualization instance that it received from the call to **PrjStartVirtualizing**.</span></span>

```C++
PrjStopVirtualizing(instanceHandle);
```

<span data-ttu-id="dfadb-149">Tenga en cuenta que hasta que se devuelve esta llamada, ProjFS puede continuar invocando las rutinas de devolución de llamada del proveedor.</span><span class="sxs-lookup"><span data-stu-id="dfadb-149">Note that until this call returns, ProjFS may continue to invoke the provider's callback routines.</span></span>