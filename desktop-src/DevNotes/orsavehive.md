---
description: Escribe el subárbol del registro sin conexión especificado en un archivo.
ms.assetid: 26f2eed9-e6e0-4dc0-8b91-212cde072744
title: Función ORSaveHive (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSaveHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 59df5b191a9bc0cfe98e1681665c5814935aa2c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649545"
---
# <a name="orsavehive-function"></a><span data-ttu-id="0125e-103">ORSaveHive función)</span><span class="sxs-lookup"><span data-stu-id="0125e-103">ORSaveHive function</span></span>

<span data-ttu-id="0125e-104">Escribe el subárbol del registro sin conexión especificado en un archivo.</span><span class="sxs-lookup"><span data-stu-id="0125e-104">Writes the specified offline registry hive to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="0125e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0125e-105">Syntax</span></span>


```C++
DWORD ORSaveHive(
  _In_ ORHKEY Handle,
  _In_ PCWSTR lpHivePath,
  _In_ DWORD  dwOsMajorVersion,
  _In_ DWORD  dwOsMinorVersion
);
```



## <a name="parameters"></a><span data-ttu-id="0125e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0125e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0125e-107">*Identificador* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0125e-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0125e-108">Identificador del subárbol del registro sin conexión que se va a guardar.</span><span class="sxs-lookup"><span data-stu-id="0125e-108">A handle to the offline registry hive to save.</span></span>

</dd> <dt>

<span data-ttu-id="0125e-109">*lpHivePath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0125e-109">*lpHivePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0125e-110">Puntero a una cadena Unicode que especifica el nombre del archivo de subárbol del registro.</span><span class="sxs-lookup"><span data-stu-id="0125e-110">A pointer to a Unicode string that specifies the name of the registry hive file.</span></span> <span data-ttu-id="0125e-111">Este no puede ser el nombre de un archivo existente.</span><span class="sxs-lookup"><span data-stu-id="0125e-111">This cannot be the name of an existing file.</span></span>

</dd> <dt>

<span data-ttu-id="0125e-112">*dwOsMajorVersion* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0125e-112">*dwOsMajorVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0125e-113">Número de versión principal del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0125e-113">The major version number of the operating system.</span></span> <span data-ttu-id="0125e-114">Este miembro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="0125e-114">This member can be one of the following values.</span></span>



| <span data-ttu-id="0125e-115">Value</span><span class="sxs-lookup"><span data-stu-id="0125e-115">Value</span></span>                                                                        | <span data-ttu-id="0125e-116">Significado</span><span class="sxs-lookup"><span data-stu-id="0125e-116">Meaning</span></span>                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0125e-117"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="0125e-117"><dt>5</dt></span></span> </dl> | <span data-ttu-id="0125e-118">Si *dwOsMinorVersion* es 1, el sistema operativo es Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0125e-118">If *dwOsMinorVersion* is 1, the operating system is Windows XP.</span></span><br/> <span data-ttu-id="0125e-119">Si *dwOsMinorVersion* es 2, el sistema operativo es windows Server 2003 R2, windows Server 2003 o Windows XP Professional x64 Edition.</span><span class="sxs-lookup"><span data-stu-id="0125e-119">If *dwOsMinorVersion* is 2, the operating system is Windows Server 2003 R2, Windows Server 2003, or Windows XP Professional x64 Edition.</span></span><br/> |
| <dl> <span data-ttu-id="0125e-120"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="0125e-120"><dt>6</dt></span></span> </dl> | <span data-ttu-id="0125e-121">Si *dwOsMinorVersion* es 0, el sistema operativo es windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0125e-121">If *dwOsMinorVersion* is 0, the operating system is Windows Server 2008 or Windows Vista.</span></span><br/> <span data-ttu-id="0125e-122">Si *dwOsMinorVersion* es 1, el sistema operativo es windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0125e-122">If *dwOsMinorVersion* is 1, the operating system is Windows Server 2008 R2 or Windows 7.</span></span><br/>                       |



 

</dd> <dt>

<span data-ttu-id="0125e-123">*dwOsMinorVersion* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0125e-123">*dwOsMinorVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0125e-124">Número de versión secundaria del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0125e-124">The minor version number of the operating system.</span></span> <span data-ttu-id="0125e-125">Este miembro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="0125e-125">This member can be one of the following values.</span></span>



| <span data-ttu-id="0125e-126">Value</span><span class="sxs-lookup"><span data-stu-id="0125e-126">Value</span></span>                                                                        | <span data-ttu-id="0125e-127">Significado</span><span class="sxs-lookup"><span data-stu-id="0125e-127">Meaning</span></span>                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0125e-128"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0125e-128"><dt>0</dt></span></span> </dl> | <span data-ttu-id="0125e-129">Si *dwOsMajorVersion* es 6, el sistema operativo es windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0125e-129">If *dwOsMajorVersion* is 6, the operating system is Windows Server 2008 or Windows Vista.</span></span><br/>                                                                                                                                          |
| <dl> <span data-ttu-id="0125e-130"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0125e-130"><dt>1</dt></span></span> </dl> | <span data-ttu-id="0125e-131">Si *dwOsMajorVersion* es 5, el sistema operativo es Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0125e-131">If *dwOsMajorVersion* is 5, the operating system is Windows XP.</span></span><br/> <span data-ttu-id="0125e-132">Si *dwOsMajorVersion* es 6, el sistema operativo es windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0125e-132">If *dwOsMajorVersion* is 6, the operating system is Windows Server 2008 R2 or Windows 7.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="0125e-133"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0125e-133"><dt>2</dt></span></span> </dl> | <span data-ttu-id="0125e-134">Si *dwOsMajorVersion* es 5, el sistema operativo es windows Server 2003 R2, windows Server 2003 o Windows XP Professional x64 Edition.</span><span class="sxs-lookup"><span data-stu-id="0125e-134">If *dwOsMajorVersion* is 5, the operating system is Windows Server 2003 R2, Windows Server 2003, or Windows XP Professional x64 Edition.</span></span> <br/> <span data-ttu-id="0125e-135">Si *dwOsMajorVersion* es 6, el parámetro *dwOsMinorVersion* debe ser 0 o 1.</span><span class="sxs-lookup"><span data-stu-id="0125e-135">If *dwOsMajorVersion* is 6, the *dwOsMinorVersion* parameter must be 0 or 1.</span></span> <br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0125e-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0125e-136">Return value</span></span>

<span data-ttu-id="0125e-137">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="0125e-137">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="0125e-138">Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="0125e-138">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="0125e-139">Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la \_ \_ marca de formato mensaje de \_ sistema para obtener una descripción genérica del error.</span><span class="sxs-lookup"><span data-stu-id="0125e-139">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span> <span data-ttu-id="0125e-140">Entre los posibles códigos de error se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="0125e-140">Possible error codes include the following:</span></span>

-   <span data-ttu-id="0125e-141">Si el autor de la llamada no tiene los derechos de acceso necesarios para escribir el archivo, la función devuelve el ERROR \_ acceso \_ denegado.</span><span class="sxs-lookup"><span data-stu-id="0125e-141">If the caller does not have the necessary access rights to write the file, the function returns ERROR\_ACCESS\_DENIED.</span></span>
-   <span data-ttu-id="0125e-142">Si el archivo especificado ya existe, la función devuelve el ERROR \_ ya \_ existe.</span><span class="sxs-lookup"><span data-stu-id="0125e-142">If the specified file already exists, the function returns ERROR\_ALREADY\_EXISTS.</span></span>

## <a name="remarks"></a><span data-ttu-id="0125e-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0125e-143">Remarks</span></span>

<span data-ttu-id="0125e-144">La función **ORSaveHive** se debe usar para guardar los cambios realizados en un subárbol del registro sin conexión.</span><span class="sxs-lookup"><span data-stu-id="0125e-144">The **ORSaveHive** function must be used to save changes made to an offline registry hive.</span></span> <span data-ttu-id="0125e-145">Los cambios no se conservan hasta que se llama a **ORSaveHive** para guardar el subárbol en un archivo.</span><span class="sxs-lookup"><span data-stu-id="0125e-145">Changes are not preserved until **ORSaveHive** is called to save the hive to a file.</span></span>

<span data-ttu-id="0125e-146">Los parámetros *dwOsMajorVersion* y *dwOsMinorVersion* especifican el formato de destino del archivo de subárbol del registro.</span><span class="sxs-lookup"><span data-stu-id="0125e-146">The *dwOsMajorVersion* and *dwOsMinorVersion* parameters together specify the target format of the registry hive file.</span></span> <span data-ttu-id="0125e-147">En la tabla siguiente se resumen los números de versión más recientes del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0125e-147">The following table summarizes the most recent operating system version numbers.</span></span>



| <span data-ttu-id="0125e-148">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="0125e-148">Operating system</span></span>                    | <span data-ttu-id="0125e-149">Número de versión</span><span class="sxs-lookup"><span data-stu-id="0125e-149">Version number</span></span> |
|-------------------------------------|----------------|
| <span data-ttu-id="0125e-150">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0125e-150">Windows Server 2008 R2</span></span>              | <span data-ttu-id="0125e-151">6.1</span><span class="sxs-lookup"><span data-stu-id="0125e-151">6.1</span></span>            |
| <span data-ttu-id="0125e-152">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0125e-152">Windows 7</span></span>                           | <span data-ttu-id="0125e-153">6.1</span><span class="sxs-lookup"><span data-stu-id="0125e-153">6.1</span></span>            |
| <span data-ttu-id="0125e-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0125e-154">Windows Server 2008</span></span>                 | <span data-ttu-id="0125e-155">6.0</span><span class="sxs-lookup"><span data-stu-id="0125e-155">6.0</span></span>            |
| <span data-ttu-id="0125e-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0125e-156">Windows Vista</span></span>                       | <span data-ttu-id="0125e-157">6.0</span><span class="sxs-lookup"><span data-stu-id="0125e-157">6.0</span></span>            |
| <span data-ttu-id="0125e-158">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0125e-158">Windows Server 2003 R2</span></span>              | <span data-ttu-id="0125e-159">5.2</span><span class="sxs-lookup"><span data-stu-id="0125e-159">5.2</span></span>            |
| <span data-ttu-id="0125e-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0125e-160">Windows Server 2003</span></span>                 | <span data-ttu-id="0125e-161">5.2</span><span class="sxs-lookup"><span data-stu-id="0125e-161">5.2</span></span>            |
| <span data-ttu-id="0125e-162">Windows XP Professional x64 Edition</span><span class="sxs-lookup"><span data-stu-id="0125e-162">Windows XP Professional x64 Edition</span></span> | <span data-ttu-id="0125e-163">5.2</span><span class="sxs-lookup"><span data-stu-id="0125e-163">5.2</span></span>            |
| <span data-ttu-id="0125e-164">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0125e-164">Windows XP</span></span>                          | <span data-ttu-id="0125e-165">5,1</span><span class="sxs-lookup"><span data-stu-id="0125e-165">5.1</span></span>            |



 

<span data-ttu-id="0125e-166">Utilice la función [GetVersionEx](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) para recuperar información sobre el sistema operativo actual.</span><span class="sxs-lookup"><span data-stu-id="0125e-166">Use the [GetVersionEx](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) function to retrieve information about the current operating system.</span></span>

<span data-ttu-id="0125e-167">La función **ORSaveHive** bloquea el subárbol del registro mientras escribe el subárbol en el archivo, cierra el archivo y libera el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="0125e-167">The **ORSaveHive** function locks the registry hive while it is writing the hive to the file, then closes the file and releases the lock.</span></span> <span data-ttu-id="0125e-168">El subárbol del registro permanece en memoria hasta que se cierra mediante una llamada a la función [**ORCloseHive**](orclosehive.md) .</span><span class="sxs-lookup"><span data-stu-id="0125e-168">The registry hive remains in memory until it is closed by calling the [**ORCloseHive**](orclosehive.md) function.</span></span> <span data-ttu-id="0125e-169">Es posible realizar más cambios en el subárbol del registro mientras está abierto; sin embargo, para conservar estos cambios, el Hive debe guardarse en un archivo nuevo, ya que la función **ORSaveHive** no sobrescribirá un archivo existente.</span><span class="sxs-lookup"><span data-stu-id="0125e-169">It is possible to make further changes to the registry hive while it is open; however, to preserve these changes the hive must be saved to a new file, because the **ORSaveHive** function will not overwrite an existing file.</span></span>

<span data-ttu-id="0125e-170">La función **ORSaveHive** se puede usar para guardar parte del subárbol del registro sin conexión.</span><span class="sxs-lookup"><span data-stu-id="0125e-170">The **ORSaveHive** function can be used to save part of the offline registry hive.</span></span> <span data-ttu-id="0125e-171">La clave especificada en el parámetro *Handle* se convierte en la clave raíz de un subárbol que consta de la clave especificada y todas sus subclaves.</span><span class="sxs-lookup"><span data-stu-id="0125e-171">The key specified in the *Handle* parameter becomes the root key of a hive that consists of the specified key and all of its subkeys.</span></span>

## <a name="requirements"></a><span data-ttu-id="0125e-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0125e-172">Requirements</span></span>



| <span data-ttu-id="0125e-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="0125e-173">Requirement</span></span> | <span data-ttu-id="0125e-174">Value</span><span class="sxs-lookup"><span data-stu-id="0125e-174">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0125e-175">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="0125e-175">Redistributable</span></span><br/> | <span data-ttu-id="0125e-176">Windows offline Registry Library versión 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="0125e-176">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="0125e-177">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0125e-177">Header</span></span><br/>          | <dl> <span data-ttu-id="0125e-178"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="0125e-178"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="0125e-179">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0125e-179">DLL</span></span><br/>             | <dl> <span data-ttu-id="0125e-180"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0125e-180"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0125e-181">Vea también</span><span class="sxs-lookup"><span data-stu-id="0125e-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0125e-182">GetVersionEx</span><span class="sxs-lookup"><span data-stu-id="0125e-182">GetVersionEx</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)
</dt> <dt>

[<span data-ttu-id="0125e-183">**ORCloseHive**</span><span class="sxs-lookup"><span data-stu-id="0125e-183">**ORCloseHive**</span></span>](orclosehive.md)
</dt> <dt>

[<span data-ttu-id="0125e-184">**OROpenHive**</span><span class="sxs-lookup"><span data-stu-id="0125e-184">**OROpenHive**</span></span>](oropenhive.md)
</dt> </dl>

 

 
