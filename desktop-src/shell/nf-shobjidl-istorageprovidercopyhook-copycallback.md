---
description: Determina si se permitirá que el shell mueva, copie, elimine o cambie el nombre de una carpeta en la raíz de sincronización de un proveedor de nube.
title: IStorageProviderCopyHook::CopyCallback
ms.topic: reference
ms.date: 11/11/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- IStorageProviderCopyHook::CopyCallback
api_type:
- COM
api_location:
- shobjidl.h
ms.openlocfilehash: c7df9296f2261e3907702067ca36265095102f34
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104997985"
---
# <a name="istorageprovidercopyhookcopycallback-method"></a><span data-ttu-id="4e871-103">IStorageProviderCopyHook:: CopyCallback (método)</span><span class="sxs-lookup"><span data-stu-id="4e871-103">IStorageProviderCopyHook::CopyCallback method</span></span>

<span data-ttu-id="4e871-104">Determina si se permitirá que el shell mueva, copie, elimine o cambie el nombre de una carpeta en la raíz de sincronización de un proveedor de nube.</span><span class="sxs-lookup"><span data-stu-id="4e871-104">Determines whether the Shell will be allowed to move, copy, delete, or rename a folder in a cloud provider's sync root.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e871-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e871-105">Syntax</span></span>

```C++
HRESULT CopyCallback( 
    HWND hwnd,
    UINT operation,
    UINT flags,
    LPCWSTR srcFile,
    DWORD srcAttribs,
    LPCWSTR destFile,
    DWORD destAttribs,
    UINT* result
);
```

## <a name="parameters"></a><span data-ttu-id="4e871-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4e871-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e871-107">*hWnd* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e871-107">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e871-108">Identificador de la ventana que el controlador de enlace de copia debe usar como elemento primario para los elementos de la interfaz de usuario que el controlador puede necesitar Mostrar.</span><span class="sxs-lookup"><span data-stu-id="4e871-108">A handle to the window that the copy hook handler should use as the parent for any user interface elements the handler may need to display.</span></span> <span data-ttu-id="4e871-109">Si se especifica **FOF_SILENT** en la *operación*, el método debe omitir este parámetro.</span><span class="sxs-lookup"><span data-stu-id="4e871-109">If **FOF_SILENT** is specified in *operation*, the method should ignore this parameter.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="4e871-110">*operación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4e871-110">*operation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e871-111">Operación que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="4e871-111">The operation to perform.</span></span> <span data-ttu-id="4e871-112">Este parámetro puede ser uno de los valores enumerados en el miembro **wFunc** de la estructura [SHFILEOPSTRUCT](/windows/win32/api/shellapi/ns-shellapi-shfileopstructa) .</span><span class="sxs-lookup"><span data-stu-id="4e871-112">This parameter can be one of the values listed under the **wFunc** member of the [SHFILEOPSTRUCT](/windows/win32/api/shellapi/ns-shellapi-shfileopstructa) structure.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="4e871-113">*marcas* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4e871-113">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e871-114">Marcas que controlan la operación.</span><span class="sxs-lookup"><span data-stu-id="4e871-114">The flags that control the operation.</span></span> <span data-ttu-id="4e871-115">Este parámetro puede ser uno o varios de los valores enumerados en el miembro *fFlags* de la estructura [SHFILEOPSTRUCT](/windows/desktop/api/shellapi/ns-shellapi-shfileopstructa) .</span><span class="sxs-lookup"><span data-stu-id="4e871-115">This parameter can be one or more of the values listed under the *fFlags* member of the [SHFILEOPSTRUCT](/windows/desktop/api/shellapi/ns-shellapi-shfileopstructa) structure.</span></span>

<span data-ttu-id="4e871-116">En el caso de los enlaces de copia de impresora, este valor es uno de los siguientes valores definidos en ShellAPI. h.</span><span class="sxs-lookup"><span data-stu-id="4e871-116">For printer copy hooks, this value is one of the following values defined in shellapi.h.</span></span>

| <span data-ttu-id="4e871-117">Value</span><span class="sxs-lookup"><span data-stu-id="4e871-117">Value</span></span>       | <span data-ttu-id="4e871-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="4e871-118">Description</span></span> |
|-------------|------------|
|  <span data-ttu-id="4e871-119">**PO_DELETE**</span><span class="sxs-lookup"><span data-stu-id="4e871-119">**PO_DELETE**</span></span>      | <span data-ttu-id="4e871-120">Se está eliminando una impresora.</span><span class="sxs-lookup"><span data-stu-id="4e871-120">A printer is being deleted.</span></span> <span data-ttu-id="4e871-121">El parámetro *srcFile* apunta a la ruta de acceso completa a la impresora especificada.</span><span class="sxs-lookup"><span data-stu-id="4e871-121">The *srcFile* parameter points to the full path to the specified printer.</span></span>           |
|  <span data-ttu-id="4e871-122">**PO_RENAME**</span><span class="sxs-lookup"><span data-stu-id="4e871-122">**PO_RENAME**</span></span>       | <span data-ttu-id="4e871-123">Se va a cambiar el nombre de una impresora.</span><span class="sxs-lookup"><span data-stu-id="4e871-123">A printer is being renamed.</span></span> <span data-ttu-id="4e871-124">El parámetro *srcFile* apunta al nuevo nombre de la impresora.</span><span class="sxs-lookup"><span data-stu-id="4e871-124">The *srcFile* parameter points to the printer's new name.</span></span> <span data-ttu-id="4e871-125">El parámetro *destFile* apunta al nombre anterior.</span><span class="sxs-lookup"><span data-stu-id="4e871-125">The *destFile* parameter points to the old name.</span></span>           |
| <span data-ttu-id="4e871-126">**PO_PORTCHANGE**</span><span class="sxs-lookup"><span data-stu-id="4e871-126">**PO_PORTCHANGE**</span></span>    | <span data-ttu-id="4e871-127">No se admite.</span><span class="sxs-lookup"><span data-stu-id="4e871-127">Not supported.</span></span> <span data-ttu-id="4e871-128">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="4e871-128">Do not use.</span></span>          |
| <span data-ttu-id="4e871-129">**PO_REN_PORT**</span><span class="sxs-lookup"><span data-stu-id="4e871-129">**PO_REN_PORT**</span></span>    | <span data-ttu-id="4e871-130">No se admite.</span><span class="sxs-lookup"><span data-stu-id="4e871-130">Not supported.</span></span> <span data-ttu-id="4e871-131">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="4e871-131">Do not use.</span></span>           |

</dd> </dl>

<dl> <dt>

<span data-ttu-id="4e871-132">*srcFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e871-132">*srcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e871-133">Puntero a una cadena que contiene el nombre de la carpeta de origen.</span><span class="sxs-lookup"><span data-stu-id="4e871-133">A pointer to a string that contains the name of the source folder.</span></span>

</dd> </dl>

<span data-ttu-id="4e871-134">*srcAttribs* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e871-134">*srcAttribs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e871-135">Atributos de la carpeta de origen.</span><span class="sxs-lookup"><span data-stu-id="4e871-135">The attributes of the source folder.</span></span> <span data-ttu-id="4e871-136">Este parámetro puede ser una combinación de cualquiera de las marcas de atributo de archivo (FILE_ATTRIBUTE_ \*) definidas en los archivos de encabezado.</span><span class="sxs-lookup"><span data-stu-id="4e871-136">This parameter can be a combination of any of the file attribute flags (FILE_ATTRIBUTE_\*) defined in the header files.</span></span> <span data-ttu-id="4e871-137">Vea [constantes de atributo de archivo](../fileio/file-attribute-constants.md).</span><span class="sxs-lookup"><span data-stu-id="4e871-137">See [File Attribute Constants](../fileio/file-attribute-constants.md).</span></span>

</dd> </dl>

<span data-ttu-id="4e871-138">*destFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e871-138">*destFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e871-139">Puntero a una cadena que contiene el nombre de la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="4e871-139">A pointer to a string that contains the name of the destination folder.</span></span>

</dd> </dl>

<span data-ttu-id="4e871-140">*destAttribs* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e871-140">*destAttribs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e871-141">Atributos de la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="4e871-141">The attributes of the destination folder.</span></span> <span data-ttu-id="4e871-142">Este parámetro puede ser una combinación de cualquiera de las marcas de atributo de archivo (FILE_ATTRIBUTE_ \*) definidas en los archivos de encabezado.</span><span class="sxs-lookup"><span data-stu-id="4e871-142">This parameter can be a combination of any of the file attribute flags (FILE_ATTRIBUTE_\*) defined in the header files.</span></span> <span data-ttu-id="4e871-143">Vea [constantes de atributo de archivo](../fileio/file-attribute-constants.md).</span><span class="sxs-lookup"><span data-stu-id="4e871-143">See [File Attribute Constants](../fileio/file-attribute-constants.md).</span></span>

</dd> </dl>

<span data-ttu-id="4e871-144">*resultado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4e871-144">*result* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e871-145">Valor entero que indica si el shell debe realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="4e871-145">The integer value that indicates whether the Shell should perform the operation.</span></span> <span data-ttu-id="4e871-146">Uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="4e871-146">One of the following:</span></span>

| <span data-ttu-id="4e871-147">Valor</span><span class="sxs-lookup"><span data-stu-id="4e871-147">Value</span></span>       | <span data-ttu-id="4e871-148">Descripción</span><span class="sxs-lookup"><span data-stu-id="4e871-148">Description</span></span> |
|-------------|------------|
| <span data-ttu-id="4e871-149">**IDYES**</span><span class="sxs-lookup"><span data-stu-id="4e871-149">**IDYES**</span></span>       | <span data-ttu-id="4e871-150">Permite la operación.</span><span class="sxs-lookup"><span data-stu-id="4e871-150">Allows the operation.</span></span>           |
| <span data-ttu-id="4e871-151">**IDNO**</span><span class="sxs-lookup"><span data-stu-id="4e871-151">**IDNO**</span></span>        | <span data-ttu-id="4e871-152">Evita la operación en esta carpeta pero continúa con cualquier otra operación que se haya aprobado (por ejemplo, una operación de copia por lotes).</span><span class="sxs-lookup"><span data-stu-id="4e871-152">Prevents the operation on this folder but continues with any other operations that have been approved (for example, a batch copy operation).</span></span>           |
| <span data-ttu-id="4e871-153">**IDCANCEL**</span><span class="sxs-lookup"><span data-stu-id="4e871-153">**IDCANCEL**</span></span>    | <span data-ttu-id="4e871-154">Evita la operación actual y cancela las operaciones pendientes.</span><span class="sxs-lookup"><span data-stu-id="4e871-154">Prevents the current operation and cancels any pending operations.</span></span>           |


</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="4e871-155">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4e871-155">Return value</span></span>

<span data-ttu-id="4e871-156">Devuelve **S_OK** si se realiza correctamente, o un código de error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="4e871-156">Returns **S_OK** if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e871-157">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4e871-157">Remarks</span></span>

<span data-ttu-id="4e871-158">El shell llama al controlador de enlace de copia del proveedor de la nube para cada carpeta en la raíz de sincronización registrada.</span><span class="sxs-lookup"><span data-stu-id="4e871-158">The Shell calls the cloud provider's copy hook handler for every folder under the registered sync root.</span></span> <span data-ttu-id="4e871-159">Para registrar un controlador de enlace de copia para las carpetas en la nube, establezca el valor de **CopyHook** en la clave de **/software/Microsoft/Windows/CurrentVersion/Explorer/syncrootmanager/{syncrootid} HKEY_LOCAL_MACHINE** en el CLSID del objeto de enlace de copia.</span><span class="sxs-lookup"><span data-stu-id="4e871-159">To register a copy hook handler for cloud folders, set the **CopyHook** value under the **HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/Explorer/SyncRootManager/{SyncRootId}** key to the CLSID of the copy hook object.</span></span>

<span data-ttu-id="4e871-160">Cuando se llama al método **CopyCallback** , el shell inicializa la interfaz [IStorageProviderCopyHook](nn-shobjidl-istorageprovidercopyhook.md) directamente sin usar una interfaz [IShellExtInit](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="4e871-160">When the **CopyCallback** method is called, the Shell initializes the [IStorageProviderCopyHook](nn-shobjidl-istorageprovidercopyhook.md) interface directly without using an [IShellExtInit](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface first.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e871-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e871-161">Requirements</span></span>

| <span data-ttu-id="4e871-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e871-162">Requirement</span></span> | <span data-ttu-id="4e871-163">Value</span><span class="sxs-lookup"><span data-stu-id="4e871-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e871-164">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e871-164">Minimum supported client</span></span> | <span data-ttu-id="4e871-165">Compilación 19624 de Windows 10 Insider Preview</span><span class="sxs-lookup"><span data-stu-id="4e871-165">Windows 10 Insider Preview Build 19624</span></span>                                |
| <span data-ttu-id="4e871-166">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4e871-166">Header</span></span>                   | <span data-ttu-id="4e871-167">shobjidl. h</span><span class="sxs-lookup"><span data-stu-id="4e871-167">shobjidl.h</span></span>   |

## <a name="see-also"></a><span data-ttu-id="4e871-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e871-168">See also</span></span>

[<span data-ttu-id="4e871-169">Compilar un motor de sincronización en la nube que admita archivos de marcadores de posición</span><span class="sxs-lookup"><span data-stu-id="4e871-169">Build a Cloud Sync Engine that Supports Placeholder Files</span></span>](../cfapi/build-a-cloud-file-sync-engine.md)