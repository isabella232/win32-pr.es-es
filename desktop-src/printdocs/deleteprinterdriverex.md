---
description: La función DeletePrinterDriverEx quita el nombre del controlador de impresora especificado de la lista de nombres de los controladores admitidos en un servidor y elimina los archivos asociados con el controlador. Esta función también puede eliminar versiones específicas del controlador.
ms.assetid: 1a3d7c7f-1d45-4877-a8f7-a77f40e3c319
title: Función DeletePrinterDriverEx (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriverEx
- DeletePrinterDriverExA
- DeletePrinterDriverExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: b88ef38236961286875a1885dad9dde936887d13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706428"
---
# <a name="deleteprinterdriverex-function"></a><span data-ttu-id="0ebd5-104">DeletePrinterDriverEx función)</span><span class="sxs-lookup"><span data-stu-id="0ebd5-104">DeletePrinterDriverEx function</span></span>

<span data-ttu-id="0ebd5-105">La función **DeletePrinterDriverEx** quita el nombre del controlador de impresora especificado de la lista de nombres de los controladores admitidos en un servidor y elimina los archivos asociados con el controlador.</span><span class="sxs-lookup"><span data-stu-id="0ebd5-105">The **DeletePrinterDriverEx** function removes the specified printer-driver name from the list of names of supported drivers on a server and deletes the files associated with the driver.</span></span> <span data-ttu-id="0ebd5-106">Esta función también puede eliminar versiones específicas del controlador.</span><span class="sxs-lookup"><span data-stu-id="0ebd5-106">This function can also delete specific versions of the driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ebd5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0ebd5-107">Syntax</span></span>


```C++
BOOL DeletePrinterDriverEx(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pDriverName,
  _In_ DWORD  dwDeleteFlag,
  _In_ DWORD  dwVersionFlag
);
```



## <a name="parameters"></a><span data-ttu-id="0ebd5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0ebd5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ebd5-109">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0ebd5-109">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ebd5-110">Puntero a una cadena terminada en null que especifica el nombre del servidor desde el que se va a eliminar el controlador.</span><span class="sxs-lookup"><span data-stu-id="0ebd5-110">A pointer to a null-terminated string that specifies the name of the server from which the driver is to be deleted.</span></span> <span data-ttu-id="0ebd5-111">Si este parámetro es **null**, la función elimina el controlador de impresora del equipo local.</span><span class="sxs-lookup"><span data-stu-id="0ebd5-111">If this parameter is **NULL**, the function deletes the printer-driver from the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="0ebd5-112">*pEnvironment* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0ebd5-112">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ebd5-113">Puntero a una cadena terminada en null que especifica el entorno desde el que se va a eliminar el controlador (por ejemplo, Windows NT x86, Windows IA64 o Windows x64).</span><span class="sxs-lookup"><span data-stu-id="0ebd5-113">A pointer to a null-terminated string that specifies the environment from which the driver is to be deleted (for example, Windows NT x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="0ebd5-114">Si este parámetro es **null**, el nombre del controlador se elimina del entorno actual de la aplicación que realiza la llamada y del equipo cliente (no de la aplicación de destino y del servidor de impresión).</span><span class="sxs-lookup"><span data-stu-id="0ebd5-114">If this parameter is **NULL**, the driver name is deleted from the current environment of the calling application and client computer (not of the destination application and print server).</span></span>

</dd> <dt>

<span data-ttu-id="0ebd5-115">*pDriverName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0ebd5-115">*pDriverName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ebd5-116">Puntero a una cadena terminada en null que especifica el nombre del controlador que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="0ebd5-116">A pointer to a null-terminated string specifying the name of the driver to delete.</span></span>

</dd> <dt>

<span data-ttu-id="0ebd5-117">*dwDeleteFlag* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0ebd5-117">*dwDeleteFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ebd5-118">Opciones para eliminar archivos y versiones del controlador.</span><span class="sxs-lookup"><span data-stu-id="0ebd5-118">The options for deleting files and versions of the driver.</span></span> <span data-ttu-id="0ebd5-119">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="0ebd5-119">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="0ebd5-120">Value</span><span class="sxs-lookup"><span data-stu-id="0ebd5-120">Value</span></span>                                                                                                                                                                                                     | <span data-ttu-id="0ebd5-121">Significado</span><span class="sxs-lookup"><span data-stu-id="0ebd5-121">Meaning</span></span>                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DPD_DELETE_SPECIFIC_VERSION"></span><span id="dpd_delete_specific_version"></span><dl> <span data-ttu-id="0ebd5-122"><dt>**DPD \_ eliminar \_ \_ versión específica**</dt></span><span class="sxs-lookup"><span data-stu-id="0ebd5-122"><dt>**DPD\_DELETE\_SPECIFIC\_VERSION**</dt></span></span> </dl> | <span data-ttu-id="0ebd5-123">Elimina la versión especificada en *dwVersionFlag*.</span><span class="sxs-lookup"><span data-stu-id="0ebd5-123">Deletes the version specified in *dwVersionFlag*.</span></span> <span data-ttu-id="0ebd5-124">Esto no garantiza que el controlador se quite de la lista de controladores admitidos para el servidor.</span><span class="sxs-lookup"><span data-stu-id="0ebd5-124">This does not ensure that the driver will be removed from the list of supported drivers for the server.</span></span><br/>                  |
| <span id="DPD_DELETE_UNUSED_FILES"></span><span id="dpd_delete_unused_files"></span><dl> <span data-ttu-id="0ebd5-125"><dt>**DPD \_ eliminar \_ archivos no usados \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0ebd5-125"><dt>**DPD\_DELETE\_UNUSED\_FILES**</dt></span></span> </dl>             | <span data-ttu-id="0ebd5-126">Quita los archivos de controlador no usados.</span><span class="sxs-lookup"><span data-stu-id="0ebd5-126">Removes any unused driver files.</span></span><br/>                                                                                                                                           |
| <span id="DPD_DELETE_ALL_FILES"></span><span id="dpd_delete_all_files"></span><dl> <span data-ttu-id="0ebd5-127"><dt>**DPD \_ eliminar \_ todos \_ los archivos**</dt></span><span class="sxs-lookup"><span data-stu-id="0ebd5-127"><dt>**DPD\_DELETE\_ALL\_FILES**</dt></span></span> </dl>                      | <span data-ttu-id="0ebd5-128">Elimina el controlador solo si se pueden quitar todos los archivos asociados.</span><span class="sxs-lookup"><span data-stu-id="0ebd5-128">Deletes the driver only if all its associated files can be removed.</span></span> <span data-ttu-id="0ebd5-129">Se produce un error en la operación de eliminación si algún otro controlador instalado está utilizando alguno de los archivos del controlador.</span><span class="sxs-lookup"><span data-stu-id="0ebd5-129">The delete operation fails if any of the driver's files are being used by some other installed driver.</span></span><br/> |



 

<span data-ttu-id="0ebd5-130">Si \_ \_ \_ no se especifica DPD Delete specific version, la función elimina todas las versiones del controlador si ninguna de ellas está en uso.</span><span class="sxs-lookup"><span data-stu-id="0ebd5-130">If DPD\_DELETE\_SPECIFIC\_VERSION is not specified, the function deletes all versions of the driver if none of them is in use.</span></span> <span data-ttu-id="0ebd5-131">Si \_ \_ \_ no se especifica DPD eliminar archivos no usados ni DPD \_ eliminar \_ todos los \_ archivos, la función no elimina los archivos de controlador.</span><span class="sxs-lookup"><span data-stu-id="0ebd5-131">If neither DPD\_DELETE\_UNUSED\_FILES nor DPD\_DELETE\_ALL\_FILES is specified, the function does not delete driver files.</span></span>

</dd> <dt>

<span data-ttu-id="0ebd5-132">*dwVersionFlag* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0ebd5-132">*dwVersionFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ebd5-133">Versión del controlador que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="0ebd5-133">The version of the driver to be deleted.</span></span> <span data-ttu-id="0ebd5-134">Este parámetro puede ser 0, 1, 2 ó 3.</span><span class="sxs-lookup"><span data-stu-id="0ebd5-134">This parameter can be 0, 1, 2 or 3.</span></span> <span data-ttu-id="0ebd5-135">Este parámetro solo se usa si *dwDeleteFlag* incluye la \_ marca DPD Delete \_ specific \_ version.</span><span class="sxs-lookup"><span data-stu-id="0ebd5-135">This parameter is used only if *dwDeleteFlag* includes the DPD\_DELETE\_SPECIFIC\_VERSION flag.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ebd5-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0ebd5-136">Return value</span></span>

<span data-ttu-id="0ebd5-137">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="0ebd5-137">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="0ebd5-138">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="0ebd5-138">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ebd5-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0ebd5-139">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0ebd5-140">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="0ebd5-140">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="0ebd5-141">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="0ebd5-141">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="0ebd5-142">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="0ebd5-142">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="0ebd5-143">Antes de que la función elimine los archivos del controlador, llama a la función **DrvDriverEvent** del controlador, lo que permite que el controlador Quite los archivos privados que no se usen.</span><span class="sxs-lookup"><span data-stu-id="0ebd5-143">Before the function deletes the driver files, it calls the driver's **DrvDriverEvent** function, allowing the driver to remove any private files that are not used.</span></span> <span data-ttu-id="0ebd5-144">Para obtener más información acerca de **DrvDriverEvent**, vea el kit de desarrollo de controladores (DDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="0ebd5-144">For more information about **DrvDriverEvent**, see the Microsoft Windows Driver Development Kit (DDK).</span></span>

<span data-ttu-id="0ebd5-145">Si los archivos de controlador están cargados actualmente, la función los mueve a un directorio temporal y los marca para su eliminación al reiniciarse.</span><span class="sxs-lookup"><span data-stu-id="0ebd5-145">If the driver files are currently loaded, the function moves them to a temp directory and marks them for deletion on restart.</span></span>

<span data-ttu-id="0ebd5-146">Antes de llamar a **DeletePrinterDriverEx**, debe eliminar todos los objetos de impresora que utilizan el controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="0ebd5-146">Before calling **DeletePrinterDriverEx**, you must delete all printer objects that use the printer driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ebd5-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ebd5-147">Requirements</span></span>



| <span data-ttu-id="0ebd5-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ebd5-148">Requirement</span></span> | <span data-ttu-id="0ebd5-149">Value</span><span class="sxs-lookup"><span data-stu-id="0ebd5-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ebd5-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ebd5-150">Minimum supported client</span></span><br/> | <span data-ttu-id="0ebd5-151">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0ebd5-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0ebd5-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ebd5-152">Minimum supported server</span></span><br/> | <span data-ttu-id="0ebd5-153">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0ebd5-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0ebd5-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0ebd5-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ebd5-155"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ebd5-155"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="0ebd5-156">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0ebd5-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="0ebd5-157"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ebd5-157"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="0ebd5-158">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0ebd5-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ebd5-159"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="0ebd5-159"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="0ebd5-160">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="0ebd5-160">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0ebd5-161">**DeletePrinterDriverExW** (Unicode) y **DeletePrinterDriverExA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0ebd5-161">**DeletePrinterDriverExW** (Unicode) and **DeletePrinterDriverExA** (ANSI)</span></span><br/>                     |



## <a name="see-also"></a><span data-ttu-id="0ebd5-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ebd5-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ebd5-163">Impresión</span><span class="sxs-lookup"><span data-stu-id="0ebd5-163">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="0ebd5-164">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="0ebd5-164">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="0ebd5-165">**AddPrinterDriverEx**</span><span class="sxs-lookup"><span data-stu-id="0ebd5-165">**AddPrinterDriverEx**</span></span>](addprinterdriverex.md)
</dt> </dl>

 

 




