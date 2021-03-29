---
description: La función AddPrinterDriver instala un controlador de impresora local o remoto y asocia los archivos de configuración, datos y controlador.
ms.assetid: 0f762800-f5a5-40ea-8be1-7fd8bda23788
title: Función AddPrinterDriver (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterDriver
- AddPrinterDriverA
- AddPrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: de5a9e9d16a47dfe8b9620edc9acdc5c5fd4d552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815502"
---
# <a name="addprinterdriver-function"></a><span data-ttu-id="9ec36-103">AddPrinterDriver función)</span><span class="sxs-lookup"><span data-stu-id="9ec36-103">AddPrinterDriver function</span></span>

<span data-ttu-id="9ec36-104">La función **AddPrinterDriver** instala un controlador de impresora local o remoto y asocia los archivos de configuración, datos y controlador.</span><span class="sxs-lookup"><span data-stu-id="9ec36-104">The **AddPrinterDriver** function installs a local or remote printer driver and associates the configuration, data, and driver files.</span></span>

<span data-ttu-id="9ec36-105">Para obtener más flexibilidad a la hora de instalar o actualizar controladores de impresora, use la función [**AddPrinterDriverEx**](addprinterdriverex.md) porque permite una actualización estricta, una degradación estricta, la copia de archivos más recientes solamente y la copia de todos los archivos (independientemente de las marcas de tiempo de archivo).</span><span class="sxs-lookup"><span data-stu-id="9ec36-105">For more flexibility in installing or upgrading printer drivers, use the [**AddPrinterDriverEx**](addprinterdriverex.md) function because it allows strict upgrade, strict downgrade, copying of newer files only, and copying of all files (regardless of the file time stamps).</span></span>

> [!Note]  
> <span data-ttu-id="9ec36-106">Ya no se recomienda instalar un controlador de impresora sin un paquete de controladores.</span><span class="sxs-lookup"><span data-stu-id="9ec36-106">Installing a printer driver without a driver package is no longer recommended.</span></span> <span data-ttu-id="9ec36-107">Use [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="9ec36-107">Use [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) instead.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="9ec36-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9ec36-108">Syntax</span></span>


```C++
BOOL AddPrinterDriver(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pDriverInfo
);
```



## <a name="parameters"></a><span data-ttu-id="9ec36-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9ec36-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ec36-110">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9ec36-110">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ec36-111">Puntero a una cadena terminada en null que especifica el nombre del servidor en el que se debe instalar el controlador.</span><span class="sxs-lookup"><span data-stu-id="9ec36-111">A pointer to a null-terminated string that specifies the name of the server on which the driver should be installed.</span></span>

<span data-ttu-id="9ec36-112">Si *pName* es **null**, el controlador se instalará localmente.</span><span class="sxs-lookup"><span data-stu-id="9ec36-112">If *pName* is **NULL**, the driver will be installed locally.</span></span>

</dd> <dt>

<span data-ttu-id="9ec36-113">*Nivel* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="9ec36-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ec36-114">Versión de la estructura a la que apunta *pDriverInfo* .</span><span class="sxs-lookup"><span data-stu-id="9ec36-114">The version of the structure to which *pDriverInfo* points.</span></span>

<span data-ttu-id="9ec36-115">Este valor puede ser 2, 3, 4, 6 u 8.</span><span class="sxs-lookup"><span data-stu-id="9ec36-115">This value can be 2, 3, 4, 6, or 8.</span></span>

</dd> <dt>

<span data-ttu-id="9ec36-116">*pDriverInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9ec36-116">*pDriverInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ec36-117">Puntero a una estructura que contiene información del controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="9ec36-117">A pointer to a structure containing printer driver information.</span></span> <span data-ttu-id="9ec36-118">Esto depende del valor de *LEVEL*.</span><span class="sxs-lookup"><span data-stu-id="9ec36-118">This depends on the value of *Level*.</span></span>



| <span data-ttu-id="9ec36-119">Value</span><span class="sxs-lookup"><span data-stu-id="9ec36-119">Value</span></span> | <span data-ttu-id="9ec36-120">Estructura de unidad de impresora</span><span class="sxs-lookup"><span data-stu-id="9ec36-120">Printer Drive Structure</span></span>                  |
|-------|------------------------------------------|
| <span data-ttu-id="9ec36-121">2</span><span class="sxs-lookup"><span data-stu-id="9ec36-121">2</span></span>     | [<span data-ttu-id="9ec36-122">**Información del controlador \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="9ec36-122">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md) |
| <span data-ttu-id="9ec36-123">3</span><span class="sxs-lookup"><span data-stu-id="9ec36-123">3</span></span>     | [<span data-ttu-id="9ec36-124">**Información del controlador \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="9ec36-124">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md) |
| <span data-ttu-id="9ec36-125">4</span><span class="sxs-lookup"><span data-stu-id="9ec36-125">4</span></span>     | [<span data-ttu-id="9ec36-126">**Información del controlador \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="9ec36-126">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md) |
| <span data-ttu-id="9ec36-127">6</span><span class="sxs-lookup"><span data-stu-id="9ec36-127">6</span></span>     | [<span data-ttu-id="9ec36-128">**Información del controlador \_ \_ 6**</span><span class="sxs-lookup"><span data-stu-id="9ec36-128">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md) |
| <span data-ttu-id="9ec36-129">8</span><span class="sxs-lookup"><span data-stu-id="9ec36-129">8</span></span>     | [<span data-ttu-id="9ec36-130">**Información del controlador \_ \_ 8**</span><span class="sxs-lookup"><span data-stu-id="9ec36-130">**DRIVER\_INFO\_8**</span></span>](driver-info-8.md) |



 

<span data-ttu-id="9ec36-131">Si el miembro **pEnvironment** de la estructura a la que apunta *pDriverInfo* es **null**, se usa el entorno actual del llamador o cliente (no del servidor de destino).</span><span class="sxs-lookup"><span data-stu-id="9ec36-131">If the **pEnvironment** member of the structure pointed to by *pDriverInfo* is **NULL**, the current environment of the caller/client (not of the destination/server) is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ec36-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9ec36-132">Return value</span></span>

<span data-ttu-id="9ec36-133">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="9ec36-133">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="9ec36-134">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="9ec36-134">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ec36-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9ec36-135">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9ec36-136">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="9ec36-136">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="9ec36-137">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="9ec36-137">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="9ec36-138">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="9ec36-138">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="9ec36-139">El autor de la llamada debe tener [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="9ec36-139">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="9ec36-140">Antes de que una aplicación llame a la función **AddPrinterDriver** , todos los archivos requeridos por el controlador deben copiarse en el directorio del controlador de impresora del sistema.</span><span class="sxs-lookup"><span data-stu-id="9ec36-140">Before an application calls the **AddPrinterDriver** function, all files required by the driver must be copied to the system's printer-driver directory.</span></span> <span data-ttu-id="9ec36-141">Una aplicación puede recuperar el nombre de este directorio mediante una llamada a la función [**GetPrinterDriverDirectory**](getprinterdriverdirectory.md) .</span><span class="sxs-lookup"><span data-stu-id="9ec36-141">An application can retrieve the name of this directory by calling the [**GetPrinterDriverDirectory**](getprinterdriverdirectory.md) function.</span></span>

<span data-ttu-id="9ec36-142">Una aplicación puede determinar qué controladores de impresora se instalan actualmente mediante una llamada a la función [**EnumPrinterDrivers**](enumprinterdrivers.md) .</span><span class="sxs-lookup"><span data-stu-id="9ec36-142">An application can determine which printer drivers are currently installed by calling the [**EnumPrinterDrivers**](enumprinterdrivers.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ec36-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ec36-143">Requirements</span></span>



| <span data-ttu-id="9ec36-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ec36-144">Requirement</span></span> | <span data-ttu-id="9ec36-145">Value</span><span class="sxs-lookup"><span data-stu-id="9ec36-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ec36-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ec36-146">Minimum supported client</span></span><br/> | <span data-ttu-id="9ec36-147">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9ec36-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9ec36-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ec36-148">Minimum supported server</span></span><br/> | <span data-ttu-id="9ec36-149">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9ec36-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9ec36-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9ec36-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ec36-151"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9ec36-151"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9ec36-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9ec36-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="9ec36-153"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ec36-153"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="9ec36-154">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9ec36-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ec36-155"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="9ec36-155"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="9ec36-156">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="9ec36-156">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9ec36-157">**AddPrinterDriverW** (Unicode) y **AddPrinterDriverA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9ec36-157">**AddPrinterDriverW** (Unicode) and **AddPrinterDriverA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="9ec36-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ec36-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ec36-159">Impresión</span><span class="sxs-lookup"><span data-stu-id="9ec36-159">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9ec36-160">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="9ec36-160">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="9ec36-161">**AddPrinterDriverEx**</span><span class="sxs-lookup"><span data-stu-id="9ec36-161">**AddPrinterDriverEx**</span></span>](addprinterdriverex.md)
</dt> <dt>

[<span data-ttu-id="9ec36-162">**Información del controlador \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="9ec36-162">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)
</dt> <dt>

[<span data-ttu-id="9ec36-163">**Información del controlador \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="9ec36-163">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)
</dt> <dt>

[<span data-ttu-id="9ec36-164">**Información del controlador \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="9ec36-164">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)
</dt> <dt>

[<span data-ttu-id="9ec36-165">**Información del controlador \_ \_ 6**</span><span class="sxs-lookup"><span data-stu-id="9ec36-165">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)
</dt> <dt>

[<span data-ttu-id="9ec36-166">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="9ec36-166">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="9ec36-167">**GetPrinterDriverDirectory**</span><span class="sxs-lookup"><span data-stu-id="9ec36-167">**GetPrinterDriverDirectory**</span></span>](getprinterdriverdirectory.md)
</dt> </dl>

 

