---
title: Enumeración de archivos y directorios
description: Describe el modo en que un proveedor ProjFS participa en la enumeración de directorios.
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/25/2018
ms.topic: article
ms.openlocfilehash: e0712ceb927388b090a84a89f80f0e2d3a1befbb
ms.sourcegitcommit: 80d74c0bf4fc402865a1ad223480abe1ce4d1115
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2020
ms.locfileid: "103789141"
---
# <a name="enumerating-files-and-directories"></a><span data-ttu-id="888c3-103">Enumeración de archivos y directorios</span><span class="sxs-lookup"><span data-stu-id="888c3-103">Enumerating Files and Directories</span></span>

<span data-ttu-id="888c3-104">Cuando un proveedor crea por primera vez una raíz de virtualización, está vacía en el sistema local.</span><span class="sxs-lookup"><span data-stu-id="888c3-104">When a provider first creates a virtualization root it is empty on the local system.</span></span>  <span data-ttu-id="888c3-105">Es decir, ninguno de los elementos del almacén de datos de respaldo se ha almacenado en memoria caché en el disco.</span><span class="sxs-lookup"><span data-stu-id="888c3-105">That is, none of the items in the backing data store have yet been cached to disk.</span></span>  <span data-ttu-id="888c3-106">A medida que se abre cada elemento, se almacena en caché, pero hasta que se abre un elemento, éste solo existe en el almacén de datos de respaldo.</span><span class="sxs-lookup"><span data-stu-id="888c3-106">As each item is opened it is cached, but until an item is opened it only exists in the backing data store.</span></span>

<span data-ttu-id="888c3-107">Puesto que los elementos sin abrir no tienen ninguna presencia local, la enumeración de directorios normal no revelaría su existencia al usuario.</span><span class="sxs-lookup"><span data-stu-id="888c3-107">Since unopened items have no local presence, normal directory enumeration would not reveal their existence to the user.</span></span>  <span data-ttu-id="888c3-108">Por lo tanto, el proveedor debe participar en la enumeración de directorios devolviendo información a ProjFS acerca de los elementos de su almacén de datos de respaldo.</span><span class="sxs-lookup"><span data-stu-id="888c3-108">Therefore the provider must participate in directory enumeration by returning information to ProjFS about items in its backing data store.</span></span>  <span data-ttu-id="888c3-109">ProjFS combina la información del proveedor con lo que se encuentra en el sistema de archivos local para presentar al usuario una lista unificada del contenido de un directorio.</span><span class="sxs-lookup"><span data-stu-id="888c3-109">ProjFS merges the information from the provider with what is on the local file system to present to the user a unified list of the contents of a directory.</span></span>

## <a name="directory-enumeration-callbacks"></a><span data-ttu-id="888c3-110">Devoluciones de llamada de enumeración de directorio</span><span class="sxs-lookup"><span data-stu-id="888c3-110">Directory Enumeration Callbacks</span></span>

<span data-ttu-id="888c3-111">Para participar en la enumeración de directorios, el proveedor debe implementar las devoluciones de llamada **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)**, **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** y **[PRJ_END_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb)** .</span><span class="sxs-lookup"><span data-stu-id="888c3-111">To participate in directory enumeration the provider must implement the **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)**, **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)**, and **[PRJ_END_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb)** callbacks.</span></span>  <span data-ttu-id="888c3-112">Cuando se enumera un directorio en la raíz de virtualización del proveedor, ProjFS realiza las acciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="888c3-112">When a directory under the provider's virtualization root gets enumerated, ProjFS performs the following actions:</span></span>

1. <span data-ttu-id="888c3-113">ProjFS llama a la devolución de llamada del **PRJ_START_DIRECTORY_ENUMERATION_CB** del proveedor para iniciar una sesión de enumeración.</span><span class="sxs-lookup"><span data-stu-id="888c3-113">ProjFS calls the provider's **PRJ_START_DIRECTORY_ENUMERATION_CB** callback to start an enumeration session.</span></span>

    <span data-ttu-id="888c3-114">Como parte del procesamiento de esta devolución de llamada, el proveedor debe prepararse para realizar la enumeración.</span><span class="sxs-lookup"><span data-stu-id="888c3-114">As part of processing this callback the provider should prepare to perform the enumeration.</span></span>  <span data-ttu-id="888c3-115">Por ejemplo, debe asignar cualquier memoria que necesite para realizar el seguimiento del progreso de la enumeración en su almacén de datos de respaldo.</span><span class="sxs-lookup"><span data-stu-id="888c3-115">For example, it should allocate any memory it may need to track the progress of the enumeration in its backing data store.</span></span>

    <span data-ttu-id="888c3-116">ProjFS identifica el directorio que se va a enumerar en el miembro **rutaaccesoarchivo** del parámetro _callbackData_ de la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="888c3-116">ProjFS identifies the directory being enumerated in the **FilePathName** member of the callback's _callbackData_ parameter.</span></span>  <span data-ttu-id="888c3-117">Esto se especifica como una ruta de acceso relativa a la raíz de virtualización.</span><span class="sxs-lookup"><span data-stu-id="888c3-117">This is specified as a path relative to the virtualization root.</span></span>  <span data-ttu-id="888c3-118">Por ejemplo, si la raíz de virtualización se encuentra en `C:\virtRoot` y el directorio que se está enumerando es `C:\virtRoot\dir1\dir2` , el miembro **rutaaccesoarchivo** contendrá `dir1\dir2` .</span><span class="sxs-lookup"><span data-stu-id="888c3-118">For example, if the virtualization root is located at `C:\virtRoot`, and the directory being enumerated is `C:\virtRoot\dir1\dir2`, the **FilePathName** member will contain `dir1\dir2`.</span></span>  <span data-ttu-id="888c3-119">El proveedor se preparará para enumerar la ruta de acceso en su almacén de datos de respaldo.</span><span class="sxs-lookup"><span data-stu-id="888c3-119">The provider will prepare to enumerate that path in its backing data store.</span></span>  <span data-ttu-id="888c3-120">En función de las capacidades de la memoria auxiliar de un proveedor, puede que tenga sentido realizar la enumeración de la memoria auxiliar en la **PRJ_START_DIRECTORY_ENUMERATION_CB** devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="888c3-120">Depending on the capabilities of a provider's backing store it may make sense to perform the backing store enumeration in the **PRJ_START_DIRECTORY_ENUMERATION_CB** callback.</span></span>

    <span data-ttu-id="888c3-121">Dado que se pueden producir varias enumeraciones en paralelo en el mismo directorio, cada devolución de llamada de enumeración tiene un argumento _enumerationId_ para permitir al proveedor asociar las invocaciones de devolución de llamada en una sola sesión de enumeración.</span><span class="sxs-lookup"><span data-stu-id="888c3-121">Because multiple enumerations may occur in parallel in the same directory, each enumeration callback has an _enumerationId_ argument to enable the provider to associate the callback invocations into a single enumeration session.</span></span>

    <span data-ttu-id="888c3-122">Si el proveedor Devuelve S_OK de la devolución de llamada de **PRJ_START_DIRECTORY_ENUMERATION_CB** , debe mantener cualquier información de sesión de enumeración que tenga hasta que ProjFS invoque la devolución de llamada de **PRJ_END_DIRECTORY_ENUMERATION_CB** con el mismo valor para _enumerationId_.</span><span class="sxs-lookup"><span data-stu-id="888c3-122">If the provider returns S_OK from the **PRJ_START_DIRECTORY_ENUMERATION_CB** callback, it must maintain any enumeration session information it has until ProjFS invokes the **PRJ_END_DIRECTORY_ENUMERATION_CB** callback with the same value for _enumerationId_.</span></span>  <span data-ttu-id="888c3-123">Si el proveedor devuelve un error de **PRJ_START_DIRECTORY_ENUMERATION_CB**, ProjFS no invocará la devolución de llamada de **PRJ_END_DIRECTORY_ENUMERATION_CB** para ese _enumerationId_.</span><span class="sxs-lookup"><span data-stu-id="888c3-123">If the provider returns an error from **PRJ_START_DIRECTORY_ENUMERATION_CB**, ProjFS will not invoke the **PRJ_END_DIRECTORY_ENUMERATION_CB** callback for that _enumerationId_.</span></span>

1. <span data-ttu-id="888c3-124">ProjFS llama a la devolución de llamada **PRJ_GET_DIRECTORY_ENUMERATION_CB** del proveedor una o varias veces para obtener el contenido del directorio del proveedor.</span><span class="sxs-lookup"><span data-stu-id="888c3-124">ProjFS calls the provider's **PRJ_GET_DIRECTORY_ENUMERATION_CB** callback one or more times to get the directory contents from the provider.</span></span>

    <span data-ttu-id="888c3-125">En respuesta a esta devolución de llamada, el proveedor devuelve una lista ordenada de elementos de su almacén de datos de respaldo.</span><span class="sxs-lookup"><span data-stu-id="888c3-125">In response to this callback the provider returns a sorted list of items from its backing data store.</span></span>

    <span data-ttu-id="888c3-126">La devolución de llamada puede proporcionar una expresión de búsqueda en su parámetro _searchExpression_ que el proveedor usa para establecer el ámbito de los resultados de la enumeración.</span><span class="sxs-lookup"><span data-stu-id="888c3-126">The callback may provide a search expression in its _searchExpression_ parameter that the provider uses to scope the results of the enumeration.</span></span>  <span data-ttu-id="888c3-127">Si _searchExpression_ es null, el proveedor devuelve todas las entradas en el directorio que se está enumerando.</span><span class="sxs-lookup"><span data-stu-id="888c3-127">If _searchExpression_ is NULL, the provider returns all the entries in the directory being enumerated.</span></span>  <span data-ttu-id="888c3-128">Si no es NULL, el proveedor puede usar **[PrjDoesNameContainWildCards](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdoesnamecontainwildcards)** para determinar si hay caracteres comodín en la expresión.</span><span class="sxs-lookup"><span data-stu-id="888c3-128">If it is non-NULL, the provider can use **[PrjDoesNameContainWildCards](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdoesnamecontainwildcards)** to determine whether there are wildcards in the expression.</span></span>  <span data-ttu-id="888c3-129">Si hay, el proveedor usa **[PrjFileNameMatch](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamematch)** para determinar si una entrada en el directorio coincide con la expresión de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="888c3-129">If there are, the provider uses **[PrjFileNameMatch](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamematch)** to determine whether an entry in the directory matches the search expression.</span></span>

    <span data-ttu-id="888c3-130">El proveedor debe capturar el valor de _searchExpression_ en la primera invocación de esta devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="888c3-130">The provider should capture the value of _searchExpression_ on the first invocation of this callback.</span></span>  <span data-ttu-id="888c3-131">Usa el valor capturado en cualquier invocación posterior de la devolución de llamada en la misma sesión de enumeración, a menos que se establezca PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN en el campo **Flags** del parámetro _callbackData_ de la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="888c3-131">It uses the captured value on any subsequent invocation of the callback in the same enumeration session, unless PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN is set in the **Flags** field of the callback's _callbackData_ parameter.</span></span>  <span data-ttu-id="888c3-132">En ese caso, debe volver a capturar el valor de _searchExpression_.</span><span class="sxs-lookup"><span data-stu-id="888c3-132">In that case it should recapture the value of _searchExpression_.</span></span>

    <span data-ttu-id="888c3-133">Si no hay entradas coincidentes en su memoria auxiliar, el proveedor simplemente Devuelve S_OK de la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="888c3-133">If there are no matching entries in its backing store, the provider simply returns S_OK from the callback.</span></span>  <span data-ttu-id="888c3-134">De lo contrario, el proveedor da formato a cada entrada coincidente desde su memoria auxiliar en una estructura de **[PRJ_FILE_BASIC_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_file_basic_info)** y, a continuación, usa **[PrjFillDirEntryBuffer](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer)** para rellenar el búfer proporcionado por el parámetro _dirEntryBufferHandle_ de la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="888c3-134">Otherwise the provider formats each matching entry from its backing store into a **[PRJ_FILE_BASIC_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_file_basic_info)** structure, and then uses **[PrjFillDirEntryBuffer](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer)** to fill the buffer provided by the callback's _dirEntryBufferHandle_ parameter.</span></span>  <span data-ttu-id="888c3-135">El proveedor sigue agregando entradas hasta que las haya agregado todas o hasta que **PrjFillDirEntryBuffer** devuelva HRESULT_FROM_WIN32 (ERROR_INSUFFICIENT_BUFFER).</span><span class="sxs-lookup"><span data-stu-id="888c3-135">The provider keeps adding entries until it has added them all or until **PrjFillDirEntryBuffer** returns HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER).</span></span>  <span data-ttu-id="888c3-136">Después, el proveedor Devuelve S_OK de la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="888c3-136">Then the provider returns S_OK from the callback.</span></span>  <span data-ttu-id="888c3-137">Tenga en cuenta que el proveedor debe agregar las entradas al búfer _dirEntryBufferHandle_ en el criterio de ordenación correcto.</span><span class="sxs-lookup"><span data-stu-id="888c3-137">Note that the provider must add the entries to the _dirEntryBufferHandle_ buffer in the correct sort order.</span></span>  <span data-ttu-id="888c3-138">El proveedor debe usar **[PrjFileNameCompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** para determinar el criterio de ordenación correcto.</span><span class="sxs-lookup"><span data-stu-id="888c3-138">The provider should use **[PrjFileNameCompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** to determine the correct sort order.</span></span>

    > <span data-ttu-id="888c3-139">El proveedor debe proporcionar un valor para el miembro **IsDirectory** de **PRJ_FILE_BASIC_INFO**.</span><span class="sxs-lookup"><span data-stu-id="888c3-139">The provider must supply a value for the **IsDirectory** member of **PRJ_FILE_BASIC_INFO**.</span></span>  <span data-ttu-id="888c3-140">Si **IsDirectory** es false, el proveedor también debe proporcionar un valor para el miembro de **los archivos** .</span><span class="sxs-lookup"><span data-stu-id="888c3-140">If **IsDirectory** is FALSE, the provider must also supply a value for the **FileSize** member.</span></span>
    >
    > <span data-ttu-id="888c3-141">Si el proveedor no proporciona valores para los miembros **CreationTime**, **LastAccessTime**, **LastWriteTime** y **ChangeTime** , ProjFS usará la hora actual del sistema.</span><span class="sxs-lookup"><span data-stu-id="888c3-141">If the provider does not supply values for the **CreationTime**, **LastAccessTime**, **LastWriteTime**, and **ChangeTime** members, ProjFS will use the current system time.</span></span>
    >
    > <span data-ttu-id="888c3-142">ProjFS utilizará cualquier FILE_ATTRIBUTE marcas de los conjuntos de proveedores en el miembro **FileAttributes** excepto FILE_ATTRIBUTE_DIRECTORY; establecerá el valor correcto para FILE_ATTRIBUTE_DIRECTORY en el miembro **FileAttributes** según el valor proporcionado del miembro **IsDirectory** .</span><span class="sxs-lookup"><span data-stu-id="888c3-142">ProjFS will use whatever FILE_ATTRIBUTE flags the provider sets in the **FileAttributes** member except for FILE_ATTRIBUTE_DIRECTORY; it will set the correct value for FILE_ATTRIBUTE_DIRECTORY in the **FileAttributes** member according to the supplied value of the **IsDirectory** member.</span></span>

    <span data-ttu-id="888c3-143">Si **PrjFillDirEntryBuffer** devuelve HRESULT_FROM_WIN32 (ERROR_INSUFFICIENT_BUFFER) antes de que el proveedor se quede sin entradas para agregarlo, el proveedor debe realizar un seguimiento de la entrada que estaba intentando agregar cuando recibió el error.</span><span class="sxs-lookup"><span data-stu-id="888c3-143">If **PrjFillDirEntryBuffer** returns HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER) before the provider runs out of entries to add to it, the provider must keep track of the entry it was trying to add when it received the error.</span></span>  <span data-ttu-id="888c3-144">La próxima vez que ProjFS llame a la devolución de llamada **PRJ_GET_DIRECTORY_ENUMERATION_CB** para la misma sesión de enumeración, el proveedor debe reanudar la adición de entradas al búfer _dirEntryBufferHandle_ con la entrada que estaba intentando agregar.</span><span class="sxs-lookup"><span data-stu-id="888c3-144">The next time ProjFS calls the **PRJ_GET_DIRECTORY_ENUMERATION_CB** callback for the same enumeration session, the provider must resume adding entries to the _dirEntryBufferHandle_ buffer with the entry it was trying to add.</span></span>

    > <span data-ttu-id="888c3-145">Si la memoria auxiliar admite vínculos simbólicos, el proveedor debe usar **[PrjFillDirEntryBuffer2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer2)** para rellenar el búfer proporcionado por el parámetro _dirEntryBufferHandle_ de la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="888c3-145">If the backing store supports symbolic links, the provider must use **[PrjFillDirEntryBuffer2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer2)** to fill the buffer provided by the callback's _dirEntryBufferHandle_ parameter.</span></span>  <span data-ttu-id="888c3-146">**PrjFillDirEntryBuffer2** admite una entrada de búfer adicional que permite al proveedor especificar que la entrada de enumeración es un vínculo simbólico y cuál es su destino.</span><span class="sxs-lookup"><span data-stu-id="888c3-146">**PrjFillDirEntryBuffer2** supports an extra buffer input that allows the provider to specify that the enumeration entry is a symbolic link and what its target is.</span></span>  <span data-ttu-id="888c3-147">De lo contrario, se comporta como se ha descrito anteriormente para **PrjFillDirEntryBuffer**.</span><span class="sxs-lookup"><span data-stu-id="888c3-147">It otherwise behaves as described above for **PrjFillDirEntryBuffer**.</span></span>  <span data-ttu-id="888c3-148">En el ejemplo siguiente se usa **PrjFillDirEntryBuffer2** para ilustrar la compatibilidad con vínculos simbólicos.</span><span class="sxs-lookup"><span data-stu-id="888c3-148">The following sample uses **PrjFillDirEntryBuffer2** to illustrate support for symbolic links.</span></span>
    >
    > <span data-ttu-id="888c3-149">Tenga en cuenta que **PrjFillDirEntryBuffer2** se admite a partir de la versión 2004 de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="888c3-149">Note that **PrjFillDirEntryBuffer2** is supported as of Windows 10, version 2004.</span></span>  <span data-ttu-id="888c3-150">Un proveedor debe sondear la existencia de **PrjFillDirEntryBuffer2**, por ejemplo, mediante **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.</span><span class="sxs-lookup"><span data-stu-id="888c3-150">A provider should probe for the existence of **PrjFillDirEntryBuffer2**, for instance by using **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.</span></span>

    ```C++
    typedef struct MY_ENUM_ENTRY MY_ENUM_ENTRY;

    typedef struct MY_ENUM_ENTRY {
        MY_ENUM_ENTRY* Next;
        PWSTR Name;
        BOOLEAN IsDirectory;
        INT64 FileSize;
        BOOLEAN IsSymlink;
        PWSTR SymlinkTarget;
    } MY_ENUM_ENTRY;

    typedef struct MY_ENUM_SESSION {
        GUID EnumerationId;
        PWSTR SearchExpression;
        USHORT SearchExpressionMaxLen;
        BOOLEAN SearchExpressionCaptured;
        MY_ENUM_ENTRY* EnumHead;
        MY_ENUM_ENTRY* LastEnumEntry;
        BOOLEAN EnumCompleted;
    } MY_ENUM_SESSION;

    HRESULT
    MyGetEnumCallback(
        _In_ const PRJ_CALLBACK_DATA* callbackData,
        _In_ const GUID* enumerationId,
        _In_opt_z_ PCWSTR searchExpression,
        _In_ PRJ_DIR_ENTRY_BUFFER_HANDLE dirEntryBufferHandle
        )
    {
        // MyGetEnumSession is a routine the provider might implement to find
        // information about the enumeration session that it first stored
        // when processing its PRJ_START_DIRECTORY_ENUMERATION_CB callback.
        //
        // In this example the PRJ_START_DIRECTORY_ENUMERATION_CB callback has
        // already retrieved a list of the items in the backing store located at
        // callbackData->FilePathName, sorted them using PrjFileNameCompare()
        // to determine collation order, and stored the list in session->EnumHead.
        MY_ENUM_SESSION* session = NULL;
        session = MyGetEnumSession(enumerationId);

        if (session == NULL)
        {
            return HRESULT_FROM_WIN32(ERROR_INVALID_PARAMETER);
        }

        if (!session->SearchExpressionCaptured ||
            (callbackData->Flags & PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN))
        {
            if (searchExpression != NULL)
            {
                if (wcsncpy_s(session->SearchExpression,
                              session->SearchExpressionMaxLen,
                              searchExpression,
                              wcslen(searchExpression)))
                {
                    // Failed to copy the search expression; perhaps the provider
                    // could try reallocating session->SearchExpression.
                }
            }
            else
            {
                if (wcsncpy_s(session->SearchExpression,
                              session->SearchExpressionMaxLen,
                              "*",
                              1))
                {
                    // Failed to copy the search expression; perhaps the provider
                    // could try reallocating session->SearchExpression.
                }
            }
            session->SearchExpressionCaptured = TRUE;
        }

        MY_ENUM_ENTRY* enumHead = NULL;

        // We have to start the enumeration from the beginning if we aren't
        // continuing an existing session or if the caller is requesting a restart.
        if (((session->LastEnumEntry == NULL) &&
             !session->EnumCompleted) ||
            (callbackData->Flags & PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN))
        {
            // Ensure that if the caller is requesting a restart we reset our
            // bookmark of how far we got in the enumeration.
            session->LastEnumEntry = NULL;

            // In case we're restarting ensure we don't think we're done.
            session->EnumCompleted = FALSE;

            // We need to start considering items from the beginning of the list
            // retrieved from the backing store.
            enumHead = session->EnumHead;
        }
        else
        {
            // We are resuming an existing enumeration session.  Note that
            // session->LastEnumEntry may be NULL.  That is okay; it means
            // we got all the entries the last time this callback was invoked.
            // Returning S_OK without adding any new entries to the
            // dirEntryBufferHandle buffer signals ProjFS that the enumeration
            // has returned everything it can.
            enumHead = session->LastEnumEntry;
        }

        if (enumHead == NULL)
        {
            // There are no items to return.  Remember that we've returned everything
            // we can.
            session->EnumCompleted = TRUE;
        }
        else
        {
            MY_ENUM_ENTRY* thisEntry = enumHead;
            while (thisEntry != NULL)
            {
                // We'll insert the entry into the return buffer if it matches
                // the search expression captured for this enumeration session.
                if (PrjFileNameMatch(thisEntry->Name, session->SearchExpression))
                {
                    PRJ_FILE_BASIC_INFO fileBasicInfo = {};
                    fileBasicInfo.IsDirectory = thisEntry->IsDirectory;
                    fileBasicInfo.FileSize = thisEntry->FileSize;

                    // If our backing store says this is really a symbolic link,
                    // set up to tell ProjFS that it is a symlink and what its
                    // target is.
                    PRJ_EXTENDED_INFO extraInfo = {};
                    if (thisEntry->IsSymlink)
                    {
                        extraInfo.InfoType = PRJ_EXT_INFO_SYMLINK;
                        extraInfo.Symlink.TargetName = thisEntry->SymlinkTarget;
                    }

                    // Format the entry for return to ProjFS.
                    HRESULT fillResult = PrjFillDirEntryBuffer2(dirEntryBufferHandle,
                                                                thisEntry->Name,
                                                                &fileBasicInfo,
                                                                thisEntry->IsSymlink ? &extraInfo : NULL);

                    if (fillResult == HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER))
                    {
                        // We couldn't add this entry to the buffer; remember where we left
                        // off for the next time we're called for this enumeration session.
                        session->LastEnumEntry = thisEntry;
                        return S_OK;
                    }
                }

                thisEntry = thisEntry->Next;
            }

            // We reached the end of the list of entries; remember that we've returned
            // everything we can.
            session->EnumCompleted = TRUE;
        }

        return S_OK;
    }
    ```

1. <span data-ttu-id="888c3-151">ProjFS llama a la devolución de llamada del **PRJ_END_DIRECTORY_ENUMERATION_CB** del proveedor para finalizar la sesión de enumeración.</span><span class="sxs-lookup"><span data-stu-id="888c3-151">ProjFS calls the provider's **PRJ_END_DIRECTORY_ENUMERATION_CB** callback to end the enumeration session.</span></span>

    <span data-ttu-id="888c3-152">El proveedor debe realizar cualquier limpieza que necesite hacer para finalizar la sesión de enumeración, como desasignar la memoria asignada como parte del procesamiento **PRJ_START_DIRECTORY_ENUMERATION_CB**.</span><span class="sxs-lookup"><span data-stu-id="888c3-152">The provider should perform any cleanup it needs to do to end the enumeration session, such as deallocate memory allocated as part of processing **PRJ_START_DIRECTORY_ENUMERATION_CB**.</span></span>
