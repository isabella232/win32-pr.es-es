---
title: Aprovisionamiento de datos de archivo
description: Describe cómo un proveedor suministra información de marcadores de posición y datos de archivos.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/01/2018
ms.topic: article
ms.openlocfilehash: 341a0f1c477b605b2a437edf311c380910744ac0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421085"
---
# <a name="providing-file-data"></a><span data-ttu-id="48f59-103">Aprovisionamiento de datos de archivo</span><span class="sxs-lookup"><span data-stu-id="48f59-103">Providing File Data</span></span>

<span data-ttu-id="48f59-104">Cuando un proveedor crea por primera vez una raíz de virtualización, está vacía en el sistema local.</span><span class="sxs-lookup"><span data-stu-id="48f59-104">When a provider first creates a virtualization root it is empty on the local system.</span></span> <span data-ttu-id="48f59-105">Es decir, ninguno de los elementos del almacén de datos de respaldo se ha almacenado en memoria caché en el disco.</span><span class="sxs-lookup"><span data-stu-id="48f59-105">That is, none of the items in the backing data store have yet been cached to disk.</span></span> <span data-ttu-id="48f59-106">A medida que se abren los elementos, ProjFS solicita información del proveedor para permitir la creación de marcadores de posición para esos elementos en el sistema de archivos local.</span><span class="sxs-lookup"><span data-stu-id="48f59-106">As items are opened, ProjFS requests information from the provider to allow placeholders for those items to be created in the local file system.</span></span>  <span data-ttu-id="48f59-107">A medida que se tiene acceso al contenido del elemento, ProjFS solicita el contenido del proveedor.</span><span class="sxs-lookup"><span data-stu-id="48f59-107">As item contents are accessed, ProjFS requests those contents from the provider.</span></span>  <span data-ttu-id="48f59-108">El resultado es que, desde la perspectiva del usuario, los archivos y directorios virtualizados aparecen de forma similar a los archivos y directorios normales que ya residen en el sistema de archivos local.</span><span class="sxs-lookup"><span data-stu-id="48f59-108">The result is that from the user's perspective, virtualized files and directories appear similar to normal files and directories that already reside on the local file system.</span></span>

## <a name="placeholder-creation"></a><span data-ttu-id="48f59-109">Creación de marcadores de posición</span><span class="sxs-lookup"><span data-stu-id="48f59-109">Placeholder Creation</span></span>

<span data-ttu-id="48f59-110">Cuando una aplicación intenta abrir un identificador a un archivo virtualizado, ProjFS llama a la devolución de llamada de **[PRJ_GET_PLACEHOLDER_INFO_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb)** para cada elemento de la ruta de acceso que todavía no existe en el disco.</span><span class="sxs-lookup"><span data-stu-id="48f59-110">When an application attempts to open a handle to a virtualized file, ProjFS calls the **[PRJ_GET_PLACEHOLDER_INFO_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb)** callback for each item of the path that does not yet exist on disk.</span></span>  <span data-ttu-id="48f59-111">Por ejemplo, si una aplicación intenta abrirse `C:\virtRoot\dir1\dir2\file.txt` , pero solo existe la ruta `C:\virtRoot\dir1` de acceso en el disco, el proveedor recibirá una devolución de llamada para `C:\virtRoot\dir1\dir2` y, a continuación, para `C:\virtRoot\dir1\dir2\file.txt` .</span><span class="sxs-lookup"><span data-stu-id="48f59-111">For example, if an application tries to open `C:\virtRoot\dir1\dir2\file.txt`, but only the path `C:\virtRoot\dir1` exists on disk, then the provider will receive a callback for `C:\virtRoot\dir1\dir2`, then for `C:\virtRoot\dir1\dir2\file.txt`.</span></span>

<span data-ttu-id="48f59-112">Cuando ProjFS llama a la devolución de llamada **PRJ_GET_PLACEHOLDER_INFO_CB** del proveedor, el proveedor realiza las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="48f59-112">When ProjFS calls the provider's **PRJ_GET_PLACEHOLDER_INFO_CB** callback, the provider performs the following actions:</span></span>

1. <span data-ttu-id="48f59-113">El proveedor determina si el nombre solicitado existe en su memoria auxiliar.</span><span class="sxs-lookup"><span data-stu-id="48f59-113">The provider determines whether the requested name exists in its backing store.</span></span>  <span data-ttu-id="48f59-114">El proveedor debe usar **[PrjFileNameCompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** como rutina de comparación al buscar en su memoria auxiliar para determinar si el nombre solicitado existe en la memoria auxiliar.</span><span class="sxs-lookup"><span data-stu-id="48f59-114">The provider should use **[PrjFileNameCompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** as the comparison routine when searching its backing store to determine whether the requested name exists in the backing store.</span></span>  <span data-ttu-id="48f59-115">Si no es así, el proveedor devuelve HRESULT_FROM_WIN32 (ERROR_FILE_NOT_FOUND) de la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="48f59-115">If it does not, the provider returns HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND) from the callback.</span></span>

1. <span data-ttu-id="48f59-116">Si el nombre solicitado existe en la memoria auxiliar, el proveedor rellena una estructura de [PRJ_PLACEHOLDER_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_info) con los metadatos del sistema de archivos del elemento y llama a **[PrjWritePlaceholderInfo](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** para enviar los datos a ProjFS.</span><span class="sxs-lookup"><span data-stu-id="48f59-116">If the requested name does exist in the backing store, the provider populates a [PRJ_PLACEHOLDER_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_info) structure with the item's file system metadata and calls **[PrjWritePlaceholderInfo](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** to send the data to ProjFS.</span></span>  <span data-ttu-id="48f59-117">ProjFS usará esa información para crear un marcador de posición en el sistema de archivos local para el elemento.</span><span class="sxs-lookup"><span data-stu-id="48f59-117">ProjFS will use that information to create a placeholder in the local file system for the item.</span></span>

    > <span data-ttu-id="48f59-118">ProjFS utilizará cualquier FILE_ATTRIBUTE marcas que los conjuntos de proveedores en el miembro **FileBasicInfo. FileAttributes** de PRJ_PLACEHOLDER_INFO excepto FILE_ATTRIBUTE_DIRECTORY; establecerá el valor correcto para FILE_ATTRIBUTE_DIRECTORY en el miembro **FileBasicInfo. FileAttributes** según el valor proporcionado del miembro **FileBasicInfo. IsDirectory** .</span><span class="sxs-lookup"><span data-stu-id="48f59-118">ProjFS will use whatever FILE_ATTRIBUTE flags the provider sets in the **FileBasicInfo.FileAttributes** member of PRJ_PLACEHOLDER_INFO except for FILE_ATTRIBUTE_DIRECTORY; it will set the correct value for FILE_ATTRIBUTE_DIRECTORY in the **FileBasicInfo.FileAttributes** member according to the supplied value of the **FileBasicInfo.IsDirectory** member.</span></span>

    > <span data-ttu-id="48f59-119">Si la memoria auxiliar admite vínculos simbólicos, el proveedor debe usar **[PrjWritePlaceholderInfo2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo2)** para enviar los datos de marcador de posición a ProjFS.</span><span class="sxs-lookup"><span data-stu-id="48f59-119">If the backing store supports symbolic links, the provider must use **[PrjWritePlaceholderInfo2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo2)** to send the placeholder data to ProjFS.</span></span>  <span data-ttu-id="48f59-120">**PrjWritePlaceholderInfo2** admite una entrada de búfer adicional que permite al proveedor especificar que el marcador de posición es un vínculo simbólico y cuál es su destino.</span><span class="sxs-lookup"><span data-stu-id="48f59-120">**PrjWritePlaceholderInfo2** supports an extra buffer input that allows the provider to specify that the placeholder is a symbolic link and what its target is.</span></span>  <span data-ttu-id="48f59-121">De lo contrario, se comporta como se ha descrito anteriormente para **PrjWritePlaceholderInfo**.</span><span class="sxs-lookup"><span data-stu-id="48f59-121">It otherwise behaves as described above for **PrjWritePlaceholderInfo**.</span></span>  <span data-ttu-id="48f59-122">En el ejemplo siguiente se muestra cómo usar **PrjWritePlaceholderInfo2** para proporcionar compatibilidad con vínculos simbólicos.</span><span class="sxs-lookup"><span data-stu-id="48f59-122">The following sample illustrates how to use **PrjWritePlaceholderInfo2** to provide support for symbolic links.</span></span>
    >
    > <span data-ttu-id="48f59-123">Tenga en cuenta que **PrjWritePlaceholderInfo2** se admite a partir de la versión 2004 de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="48f59-123">Note that **PrjWritePlaceholderInfo2** is supported as of Windows 10, version 2004.</span></span>  <span data-ttu-id="48f59-124">Un proveedor debe sondear la existencia de **PrjWritePlaceholderInfo2**, por ejemplo, mediante **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.</span><span class="sxs-lookup"><span data-stu-id="48f59-124">A provider should probe for the existence of **PrjWritePlaceholderInfo2**, for instance by using **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.</span></span>

```C++
HRESULT
MyGetPlaceholderInfoCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData
    )
{
    // MyGetItemInfo is a routine the provider might implement to get
    // information from its backing store for a given file path.  The first
    // parameter is an _In_ parameter that supplies the name to look for.
    // If the item exists the routine provides the file information in the
    // remaining parameters, all of which are annotated _Out_:
    // * 2nd parameter: the name as it appears in the backing store
    // * 3rd-9th parameters: basic file info
    // * 10th parameter: if the item is a symbolic link, a pointer to a 
    //   NULL-terminated string identifying the link's target
    //
    // Note that the routine returns the name that is in the backing
    // store.  This is because the input file path may not be in the same
    // case as what is in the backing store.  The provider should create
    // the placeholder with the name it has in the backing store.
    //
    // Note also that this example does not provide anything beyond basic
    // file information and a possible symbolic link target.
    HRESULT hr;
    WCHAR* backingStoreName = NULL;
    WCHAR* symlinkTarget = NULL;
    PRJ_PLACEHOLDER_INFO placeholderInfo = {};
    hr = MyGetItemInfo(callbackData->FilePathName,
                       &backingStoreName,
                       &placeholderInfo.FileBasicInfo.IsDirectory,
                       &placeholderInfo.FileBasicInfo.FileSize,
                       &placeholderInfo.FileBasicInfo.CreationTime,
                       &placeholderInfo.FileBasicInfo.LastAccessTime,
                       &placeholderInfo.FileBasicInfo.LastWriteTime,
                       &placeholderInfo.FileBasicInfo.ChangeTime,
                       &placeholderInfo.FileBasicInfo.FileAttributes,
                       &symlinkTarget);

    if (FAILED(hr))
    {
        // If callbackData->FilePathName doesn't exist in our backing store then
        // MyGetItemInfo should HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND).
        // If this is some other error, e.g. E_OUTOFMEMORY because MyGetItemInfo
        // couldn't allocate space for backingStoreName, we return that.
        return hr;
    }

    // If the file path is for a symbolic link, pass that in with the placeholder info.
    if (symlinkTarget != NULL)
    {
        PRJ_EXTENDED_INFO extraInfo = {};

        extraInfo.InfoType = PRJ_EXT_INFO_SYMLINK;
        extraInfo.Symlink.TargetName = symlinkTarget;

        // If this returns an error we'll want to return that error from the callback.
        hr = PrjWritePlaceholderInfo2(callbackData->NamespaceVirtualizationContext,
                                      backingStoreName,
                                      &placeholderInfo,
                                      sizeof(placeholderInfo),
                                      &extraInfo);
    }
    else
    {
        // If this returns an error we'll want to return that error from the callback.
        hr = PrjWritePlaceholderInfo(callbackData->NamespaceVirtualizationContext,
                                     backingStoreName,
                                     &placeholderInfo,
                                     sizeof(placeholderInfo));
    }

    free(backingStoreName);

    if (symlinkTarget != NULL)
    {
        free(symlinkTarget);
    }

    return hr;
}
```

## <a name="providing-file-contents"></a><span data-ttu-id="48f59-125">Proporcionar contenido de archivo</span><span class="sxs-lookup"><span data-stu-id="48f59-125">Providing File Contents</span></span>

<span data-ttu-id="48f59-126">Cuando ProjFS necesita asegurarse de que un archivo virtualizado contiene datos, como cuando una aplicación intenta leer el archivo, ProjFS llama a la **[PRJ_GET_FILE_DATA_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** devolución de llamada para ese elemento para solicitar que el proveedor proporcione el contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="48f59-126">When ProjFS needs to ensure that a virtualized file contains data, such as when an application attempts to read from the file, ProjFS calls the **[PRJ_GET_FILE_DATA_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** callback for that item to request that the provider supply the file's contents.</span></span>  <span data-ttu-id="48f59-127">El proveedor recupera los datos del archivo desde su memoria auxiliar y usa **[PrjWriteFileData](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwritefiledata)** para enviar los datos al sistema de archivos local.</span><span class="sxs-lookup"><span data-stu-id="48f59-127">The provider retrieves the file's data from its backing store and uses **[PrjWriteFileData](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwritefiledata)** to send the data to the local file system.</span></span>

> <span data-ttu-id="48f59-128">Cuando ProjFS llama a esta devolución de llamada, el miembro **rutaaccesoarchivo** del parámetro _callbackData_ proporciona el nombre que tenía el archivo cuando se creó el marcador de posición.</span><span class="sxs-lookup"><span data-stu-id="48f59-128">When ProjFS calls this callback, the **FilePathName** member of the _callbackData_ parameter supplies the name the file had when its placeholder was created.</span></span>  <span data-ttu-id="48f59-129">Es decir, si se ha cambiado el nombre del archivo desde que se creó el marcador de posición, la devolución de llamada proporciona el nombre original (antes de cambiar el nombre), no el nombre actual (posterior al cambio de nombre).</span><span class="sxs-lookup"><span data-stu-id="48f59-129">That is, if the file has been renamed since its placeholder was created, the callback supplies the original (pre-rename) name, not the current (post-rename) name.</span></span>  <span data-ttu-id="48f59-130">Si es necesario, el proveedor puede usar el miembro **versionInfo** del parámetro _callbackData_ para determinar qué datos del archivo se solicitan.</span><span class="sxs-lookup"><span data-stu-id="48f59-130">If necessary, the provider can use the **VersionInfo** member of the _callbackData_ parameter to determine which file's data is being requested.</span></span>
>
> <span data-ttu-id="48f59-131">Para obtener más información sobre cómo se puede usar el miembro **versionInfo** de PRJ_CALLBACK_DATA, consulte la documentación de [PRJ_PLACEHOLDER_VERSION_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info) y el tema control de cambios en la [vista](handling-view-changes.md) .</span><span class="sxs-lookup"><span data-stu-id="48f59-131">For more information on how the **VersionInfo** member of PRJ_CALLBACK_DATA may be used, see the documentation for [PRJ_PLACEHOLDER_VERSION_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info) and the [Handling View Changes](handling-view-changes.md) topic.</span></span>

<span data-ttu-id="48f59-132">El proveedor puede dividir el intervalo de datos solicitado en la devolución de llamada de **PRJ_GET_FILE_DATA_CB** en varias llamadas a **PrjWriteFileData**, cada una de las cuales proporciona una parte del intervalo solicitado.</span><span class="sxs-lookup"><span data-stu-id="48f59-132">The provider is allowed to split the range of data requested in the **PRJ_GET_FILE_DATA_CB** callback into multiple calls to **PrjWriteFileData**, each supplying a portion of the requested range.</span></span>  <span data-ttu-id="48f59-133">Sin embargo, el proveedor debe proporcionar todo el intervalo solicitado antes de completar la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="48f59-133">However, the provider must supply the entire requested range before completing the callback.</span></span>  <span data-ttu-id="48f59-134">Por ejemplo, si la devolución de llamada solicita 10 MB de datos de _byteoffset (_ 0 para _longitud_ 10.485.760, el proveedor puede elegir proporcionar los datos en 10 llamadas a **PrjWriteFileData**, cada uno de los cuales envía 1 MB.</span><span class="sxs-lookup"><span data-stu-id="48f59-134">For example, if the callback requests 10 MB of data from _byteOffset_ 0 for _length_ 10,485,760, the provider may choose to supply the data in 10 calls to **PrjWriteFileData**, each sending 1 MB.</span></span>

<span data-ttu-id="48f59-135">El proveedor también puede proporcionar más del intervalo solicitado, hasta la longitud del archivo.</span><span class="sxs-lookup"><span data-stu-id="48f59-135">The provider is also free to supply more than the requested range, up to the length of the file.</span></span>  <span data-ttu-id="48f59-136">El intervalo que el proveedor suministra debe cubrir el intervalo solicitado.</span><span class="sxs-lookup"><span data-stu-id="48f59-136">The range the provider supplies must cover the requested range.</span></span>  <span data-ttu-id="48f59-137">Por ejemplo, si la devolución de llamada solicita 1 MB de datos de _byteoffset (_ 4096 para la _longitud_ 1.052.672 y el archivo tiene un tamaño total de 10 MB, el proveedor podría elegir devolver 2 MB de datos a partir del desplazamiento 0.</span><span class="sxs-lookup"><span data-stu-id="48f59-137">For example, if the callback requests 1 MB of data from _byteOffset_ 4096 for _length_ 1,052,672, and the file has a total size of 10 MB, the provider could choose to return 2 MB of data starting at offset 0.</span></span>

### <a name="buffer-alignment-considerations"></a><span data-ttu-id="48f59-138">Consideraciones sobre la alineación del búfer</span><span class="sxs-lookup"><span data-stu-id="48f59-138">Buffer Alignment Considerations</span></span>

<span data-ttu-id="48f59-139">ProjFS usa el [FILE_OBJECT](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_file_object) del autor de la llamada que requiere que los datos escriban los datos en el sistema de archivos local.</span><span class="sxs-lookup"><span data-stu-id="48f59-139">ProjFS uses the [FILE_OBJECT](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_file_object) from the caller who requires the data to write the data to the local file system.</span></span>  <span data-ttu-id="48f59-140">Sin embargo, ProjFS no puede controlar si el FILE_OBJECT se abrió para e/s en búfer o no almacenado en búfer.</span><span class="sxs-lookup"><span data-stu-id="48f59-140">However ProjFS cannot control whether that FILE_OBJECT was opened for buffered or unbuffered I/O.</span></span>  <span data-ttu-id="48f59-141">Si se abrió el FILE_OBJECT para la e/s no almacenada en búfer, las operaciones de lectura y escritura en el archivo deben cumplir ciertos requisitos de alineación.</span><span class="sxs-lookup"><span data-stu-id="48f59-141">If the FILE_OBJECT was opened for unbuffered I/O, reads and writes to the file must adhere to certain alignment requirements.</span></span>  <span data-ttu-id="48f59-142">El proveedor puede cumplir esos requisitos de alineación haciendo dos cosas:</span><span class="sxs-lookup"><span data-stu-id="48f59-142">The provider can meet those alignment requirements by doing two things:</span></span>

1. <span data-ttu-id="48f59-143">Use **[PrjAllocateAlignedBuffer](/windows/win32/api/projectedfslib/nf-projectedfslib-prjallocatealignedbuffer)** para asignar el búfer que se va a pasar en el parámetro de _búfer_ de **PrjWriteFileData**.</span><span class="sxs-lookup"><span data-stu-id="48f59-143">Use **[PrjAllocateAlignedBuffer](/windows/win32/api/projectedfslib/nf-projectedfslib-prjallocatealignedbuffer)** to allocate the buffer to pass in **PrjWriteFileData**'s _buffer_ parameter.</span></span>
1. <span data-ttu-id="48f59-144">Asegúrese de que los parámetros de _longitud_ y _byteoffset (_ de **PrjWriteFileData** son múltiplos enteros del requisito de alineación del dispositivo de almacenamiento (tenga en cuenta que el parámetro de _longitud_ no tiene que cumplir este requisito si la   +  _longitud_ de byteoffset (es igual al final del archivo).</span><span class="sxs-lookup"><span data-stu-id="48f59-144">Ensure that the _byteOffset_ and _length_ parameters of **PrjWriteFileData** are integer multiples of the storage device's alignment requirement (note that the _length_ parameter does not have to meet this requirement if _byteOffset_ + _length_ is equal to the end of the file).</span></span>  <span data-ttu-id="48f59-145">El proveedor puede usar **[PrjGetVirtualizationInstanceInfo](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetvirtualizationinstanceinfo)** para recuperar el requisito de alineación del dispositivo de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="48f59-145">The provider can use **[PrjGetVirtualizationInstanceInfo](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetvirtualizationinstanceinfo)** to retrieve the storage device's alignment requirement.</span></span>

<span data-ttu-id="48f59-146">ProjFS deja hasta el proveedor para calcular la alineación adecuada.</span><span class="sxs-lookup"><span data-stu-id="48f59-146">ProjFS leaves it up to the provider to calculate proper alignment.</span></span>  <span data-ttu-id="48f59-147">Esto se debe a que al procesar una devolución de llamada de **PRJ_GET_FILE_DATA_CB** el proveedor puede optar por devolver los datos solicitados en varias llamadas a **PrjWriteFileData** , cada una de las cuales devuelve parte del total de datos solicitados, antes de completar la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="48f59-147">This is because when processing a **PRJ_GET_FILE_DATA_CB** callback the provider may opt to return the requested data across multiple **PrjWriteFileData** calls, each returning part of the total requested data, before completing the callback.</span></span>

> <span data-ttu-id="48f59-148">Si el proveedor va a utilizar una única llamada a **PrjWriteFileData** para escribir todo el archivo, es decir, de _byteoffset (_ = 0 a _length_ = size = size (tamaño del archivo) o para devolver el intervalo exacto solicitado en la devolución de llamada **PRJ_GET_FILE_DATA_CB** , el proveedor no tiene que realizar ningún cálculo de alineación.</span><span class="sxs-lookup"><span data-stu-id="48f59-148">If the provider is going to use a single call to **PrjWriteFileData** to either write the entire file, i.e. from _byteOffset_ = 0 to _length_ = size of the file, or to return the exact range requested in the **PRJ_GET_FILE_DATA_CB** callback, the provider does not have to do any alignment calculations.</span></span>  <span data-ttu-id="48f59-149">Sin embargo, debe seguir usando **PrjAllocateAlignedBuffer** para asegurarse de que el _búfer_ cumple los requisitos de alineación del dispositivo de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="48f59-149">However, it must still use **PrjAllocateAlignedBuffer** to ensure that _buffer_ meets the storage device’s alignment requirements.</span></span>

<span data-ttu-id="48f59-150">Vea el tema [almacenamiento en búfer de archivos](/windows/desktop/FileIO/file-buffering) para obtener más información sobre operaciones de e/s almacenadas en búfer y sin almacenamiento en búfer.</span><span class="sxs-lookup"><span data-stu-id="48f59-150">See the topic [File Buffering](/windows/desktop/FileIO/file-buffering) for more information on buffered vs. unbuffered I/O.</span></span>

```C++
//  BlockAlignTruncate(): Aligns P on the previous V boundary (V must be != 0).
#define BlockAlignTruncate(P,V) ((P) & (0-((UINT64)(V))))

// This sample illustrates both returning the entire requested range in a
// single call to PrjWriteFileData(), and splitting it up into smaller 
// units.  Note that the provider must return all the requested data before
// completing the PRJ_GET_FILE_DATA_CB callback with S_OK.
HRESULT
MyGetFileDataCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData,
    _In_ UINT64 byteOffset,
    _In_ UINT32 length
    )
{
    HRESULT hr;

    // For the purposes of this sample our provider has a 1 MB limit to how
    // much data it can return at once (perhaps its backing store imposes such
    // a limit).
    UINT64 writeStartOffset;
    UINT32 writeLength;
    if (length <= 1024*1024)
    {
        // The range requested in the callback is less than 1MB, so we can return
        // the data in a single call, without doing any alignment calculations.
        writeStartOffset = byteOffset;
        writeLength = length;
    }
    else
    {
        // The range requested is more than 1MB.  Retrieve the device alignment
        // and calculate a transfer size that conforms to the device alignment and
        // is <= 1MB.
        PRJ_VIRTUALIZATION_INSTANCE_INFO instanceInfo;
        UINT32 infoSize = sizeof(instanceInfo);
        hr = PrjGetVirtualizationInstanceInfo(callbackData->NamespaceVirtualizationContext,
                                              &infoSize,
                                              &instanceInfo);

        if (FAILED(hr))
        {
            return hr;
        }

        // The first transfer will start at the beginning of the requested range,
        // which is guaranteed to have the correct alignment.
        writeStartOffset = byteOffset;

        // Ensure our transfer size is aligned to the device alignment, and is
        // no larger than 1 MB (note this assumes the device alignment is less
        // than 1 MB).
        UINT64 writeEndOffset = BlockAlignTruncate(writeStartOffset + 1024*1024,
                                                   instanceInfo->WriteAlignment);
        assert(writeEndOffset > 0);
        assert(writeEndOffset > writeStartOffset);

        writeLength = writeEndOffset - writeStartOffset;
    }

    // Allocate a buffer that adheres to the needed memory alignment.
    void* writeBuffer = NULL;
    writeBuffer = PrjAllocateAlignedBuffer(callbackData->NamespaceVirtualizationContext,
                                           writeLength);

    if (writeBuffer == NULL)
    {
        return E_OUTOFMEMORY;
    }

    do
    {
        // MyGetFileDataFromStore is a routine the provider might implement to copy
        // data for the specified file from the provider's backing store to a
        // buffer.  The routine finds the file located at callbackData->FilePathName
        // and copies writeLength bytes of its data, starting at writeStartOffset,
        // to the buffer pointed to by writeBuffer.
        hr = MyGetFileDataFromStore(callbackData->FilePathName,
                                    writeStartOffset,
                                    writeLength,
                                    writeBuffer);

        if (FAILED(hr))
        {
            PrjFreeAlignedBuffer(writeBuffer);
            return hr;
        }

        // Write the data to the file in the local file system.
        hr = PrjWriteFileData(callbackData->NamespaceVirtualizationContext,
                              callbackData->DataStreamId,
                              writeBuffer,
                              writeStartOffset,
                              writeLength);

        if (FAILED(hr))
        {
            PrjFreeAlignedBuffer(writeBuffer);
            return hr;
        }

        // The length parameter to the callback is guaranteed to be either
        // correctly aligned or to result in a write to the end of the file.
        length -= writeLength;
        if (length < writeLength)
        {
            writeLength = length;
        }
    }
    while (writeLength > 0);

    PrjFreeAlignedBuffer(writeBuffer);
    return hr;
}
```