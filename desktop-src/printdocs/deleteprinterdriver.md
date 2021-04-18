---
description: La función DeletePrinterDriver quita el nombre del controlador de impresora especificado de la lista de nombres de los controladores admitidos en un servidor.
ms.assetid: b159bd8b-3416-44a5-91bf-c0447ed6b465
title: Función DeletePrinterDriver (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriver
- DeletePrinterDriverA
- DeletePrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 9e84730be0d20100c2da42aa357f35c08cfb0727
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667105"
---
# <a name="deleteprinterdriver-function"></a><span data-ttu-id="ac728-103">DeletePrinterDriver función)</span><span class="sxs-lookup"><span data-stu-id="ac728-103">DeletePrinterDriver function</span></span>

<span data-ttu-id="ac728-104">La función **DeletePrinterDriver** quita el nombre del controlador de impresora especificado de la lista de nombres de los controladores admitidos en un servidor.</span><span class="sxs-lookup"><span data-stu-id="ac728-104">The **DeletePrinterDriver** function removes the specified printer-driver name from the list of names of supported drivers on a server.</span></span>

<span data-ttu-id="ac728-105">Para eliminar los archivos asociados al controlador además de quitar el nombre del controlador de impresora especificado de la lista de nombres de los controladores admitidos para un servidor, utilice la función [**DeletePrinterDriverEx**](deleteprinterdriverex.md) .</span><span class="sxs-lookup"><span data-stu-id="ac728-105">To delete the files associated with the driver in addition to removing the specified printer-driver name from the list of names of supported drivers for a server, use the [**DeletePrinterDriverEx**](deleteprinterdriverex.md) function.</span></span>

<span data-ttu-id="ac728-106">**DeletePrinterDriver** elimina un controlador solo si no se está usando ninguna versión del controlador para el entorno especificado.</span><span class="sxs-lookup"><span data-stu-id="ac728-106">**DeletePrinterDriver** deletes a driver only if no version of the driver is in use for the specified environment.</span></span> <span data-ttu-id="ac728-107">[**DeletePrinterDriverEx**](deleteprinterdriverex.md) puede eliminar versiones específicas del controlador.</span><span class="sxs-lookup"><span data-stu-id="ac728-107">[**DeletePrinterDriverEx**](deleteprinterdriverex.md) can delete specific versions of the driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac728-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ac728-108">Syntax</span></span>


```C++
BOOL DeletePrinterDriver(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pDriverName
);
```



## <a name="parameters"></a><span data-ttu-id="ac728-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ac728-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac728-110">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ac728-110">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac728-111">Puntero a una cadena terminada en null que especifica el nombre del servidor desde el que se va a eliminar el controlador.</span><span class="sxs-lookup"><span data-stu-id="ac728-111">A pointer to a null-terminated string that specifies the name of the server from which the driver is to be deleted.</span></span> <span data-ttu-id="ac728-112">Si este parámetro es **null**, el nombre del controlador de impresora se quitará de forma local.</span><span class="sxs-lookup"><span data-stu-id="ac728-112">If this parameter is **NULL**, the printer-driver name will be removed locally.</span></span>

</dd> <dt>

<span data-ttu-id="ac728-113">*pEnvironment* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ac728-113">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac728-114">Puntero a una cadena terminada en null que especifica el entorno desde el que se va a eliminar el controlador (por ejemplo, Windows x86, Windows IA64 o Windows x64).</span><span class="sxs-lookup"><span data-stu-id="ac728-114">A pointer to a null-terminated string that specifies the environment from which the driver is to be deleted (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="ac728-115">Si este parámetro es **null**, el nombre del controlador se elimina del entorno actual de la aplicación que realiza la llamada y del equipo cliente (no de la aplicación de destino y del servidor de impresión).</span><span class="sxs-lookup"><span data-stu-id="ac728-115">If this parameter is **NULL**, the driver name is deleted from the current environment of the calling application and client machine (not of the destination application and print server).</span></span>

</dd> <dt>

<span data-ttu-id="ac728-116">*pDriverName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ac728-116">*pDriverName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac728-117">Puntero a una cadena terminada en null que especifica el nombre del controlador que se debe eliminar.</span><span class="sxs-lookup"><span data-stu-id="ac728-117">A pointer to a null-terminated string specifying the name of the driver that should be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac728-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ac728-118">Return value</span></span>

<span data-ttu-id="ac728-119">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="ac728-119">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="ac728-120">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="ac728-120">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac728-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ac728-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ac728-122">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="ac728-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="ac728-123">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="ac728-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="ac728-124">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="ac728-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="ac728-125">El autor de la llamada debe tener [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="ac728-125">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="ac728-126">La función **DeletePrinterDriver** no elimina los archivos asociados, simplemente quita el nombre del controlador de la lista devuelta por la función [**EnumPrinterDrivers**](enumprinterdrivers.md) .</span><span class="sxs-lookup"><span data-stu-id="ac728-126">The **DeletePrinterDriver** function does not delete the associated files, it merely removes the driver name from the list returned by the [**EnumPrinterDrivers**](enumprinterdrivers.md) function.</span></span>

<span data-ttu-id="ac728-127">Antes de llamar a **DeletePrinterDriver**, debe eliminar todos los objetos de impresora que utilizan el controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="ac728-127">Before calling **DeletePrinterDriver**, you must delete all printer objects that use the printer driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac728-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac728-128">Requirements</span></span>



| <span data-ttu-id="ac728-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac728-129">Requirement</span></span> | <span data-ttu-id="ac728-130">Value</span><span class="sxs-lookup"><span data-stu-id="ac728-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac728-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac728-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ac728-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ac728-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ac728-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac728-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ac728-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ac728-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ac728-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ac728-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac728-136"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ac728-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ac728-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ac728-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="ac728-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac728-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="ac728-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ac728-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac728-140"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="ac728-140"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="ac728-141">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="ac728-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ac728-142">**DeletePrinterDriverW** (Unicode) y **DeletePrinterDriverA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ac728-142">**DeletePrinterDriverW** (Unicode) and **DeletePrinterDriverA** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="ac728-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac728-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac728-144">Impresión</span><span class="sxs-lookup"><span data-stu-id="ac728-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ac728-145">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="ac728-145">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="ac728-146">**DeletePrinterDriverEx**</span><span class="sxs-lookup"><span data-stu-id="ac728-146">**DeletePrinterDriverEx**</span></span>](deleteprinterdriverex.md)
</dt> <dt>

[<span data-ttu-id="ac728-147">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="ac728-147">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> </dl>

 

