---
description: La función AddMonitor instala un monitor de puerto local y vincula los archivos de configuración, datos y supervisión.
ms.assetid: 6a556422-5360-42d2-b177-dba0498c06d8
title: Función AddMonitor (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddMonitor
- AddMonitorA
- AddMonitorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 40b45c4dc05580837a2cf4a001cf8d18e646e5cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083364"
---
# <a name="addmonitor-function"></a><span data-ttu-id="fd6c6-103">AddMonitor función)</span><span class="sxs-lookup"><span data-stu-id="fd6c6-103">AddMonitor function</span></span>

<span data-ttu-id="fd6c6-104">La función **AddMonitor** instala un monitor de puerto local y vincula los archivos de configuración, datos y supervisión.</span><span class="sxs-lookup"><span data-stu-id="fd6c6-104">The **AddMonitor** function installs a local port monitor and links the configuration, data, and monitor files.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd6c6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fd6c6-105">Syntax</span></span>


```C++
BOOL AddMonitor(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pMonitors
);
```



## <a name="parameters"></a><span data-ttu-id="fd6c6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fd6c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd6c6-107">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fd6c6-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6c6-108">Puntero a una cadena terminada en null que especifica el nombre del servidor en el que debe instalarse el monitor.</span><span class="sxs-lookup"><span data-stu-id="fd6c6-108">A pointer to a null-terminated string that specifies the name of the server on which the monitor should be installed.</span></span> <span data-ttu-id="fd6c6-109">En el caso de los sistemas que solo admiten la instalación local de monitores, esta cadena debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="fd6c6-109">For systems that support only local installation of monitors, this string should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fd6c6-110">*Nivel* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="fd6c6-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6c6-111">Versión de la estructura a la que apunta *pMonitors* .</span><span class="sxs-lookup"><span data-stu-id="fd6c6-111">The version of the structure to which *pMonitors* points.</span></span> <span data-ttu-id="fd6c6-112">Este valor debe ser 2.</span><span class="sxs-lookup"><span data-stu-id="fd6c6-112">This value must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="fd6c6-113">*pMonitors* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fd6c6-113">*pMonitors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6c6-114">Puntero a una estructura de supervisión de la [**\_ información \_ 2**](monitor-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="fd6c6-114">A pointer to a [**MONITOR\_INFO\_2**](monitor-info-2.md) structure.</span></span> <span data-ttu-id="fd6c6-115">Si el miembro **pEnvironment** de la estructura *pMonitors* es **null**, se usa el entorno actual del llamador (cliente), no del destino (servidor).</span><span class="sxs-lookup"><span data-stu-id="fd6c6-115">If the **pEnvironment** member of the *pMonitors* structure is **NULL**, the current environment of the caller (client), not of the destination (server), is used.</span></span>

<span data-ttu-id="fd6c6-116">Tenga en cuenta que se producirá un error en la llamada si el entorno no coincide con el entorno del servidor, es decir, solo puede Agregar un monitor escrito para la arquitectura del servidor.</span><span class="sxs-lookup"><span data-stu-id="fd6c6-116">Note that the call will fail if the environment does not match the environment of the server, that is, you can only add a monitor that was written for the architecture of the server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd6c6-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fd6c6-117">Return value</span></span>

<span data-ttu-id="fd6c6-118">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="fd6c6-118">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="fd6c6-119">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="fd6c6-119">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd6c6-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd6c6-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fd6c6-121">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="fd6c6-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="fd6c6-122">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="fd6c6-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="fd6c6-123">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="fd6c6-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="fd6c6-124">El autor de la llamada debe tener [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="fd6c6-124">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="fd6c6-125">Antes de que una aplicación llame a la función **AddMonitor** , todos los archivos requeridos por el monitor deben copiarse en el directorio system32.</span><span class="sxs-lookup"><span data-stu-id="fd6c6-125">Before an application calls the **AddMonitor** function, all files required by the monitor must be copied to the SYSTEM32 directory.</span></span>

<span data-ttu-id="fd6c6-126">Para determinar los monitores de puerto que están instalados actualmente, llame a la función [**EnumMonitors**](enummonitors.md) .</span><span class="sxs-lookup"><span data-stu-id="fd6c6-126">To determine the port monitors that are currently installed, call the [**EnumMonitors**](enummonitors.md) function.</span></span>

<span data-ttu-id="fd6c6-127">Para quitar un monitor agregado por **AddMonitor**, llame a la función [**DeleteMonitor**](deletemonitor.md) .</span><span class="sxs-lookup"><span data-stu-id="fd6c6-127">To remove a monitor added by **AddMonitor**, call the [**DeleteMonitor**](deletemonitor.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd6c6-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd6c6-128">Requirements</span></span>



| <span data-ttu-id="fd6c6-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd6c6-129">Requirement</span></span> | <span data-ttu-id="fd6c6-130">Value</span><span class="sxs-lookup"><span data-stu-id="fd6c6-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd6c6-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd6c6-131">Minimum supported client</span></span><br/> | <span data-ttu-id="fd6c6-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fd6c6-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fd6c6-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd6c6-133">Minimum supported server</span></span><br/> | <span data-ttu-id="fd6c6-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fd6c6-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fd6c6-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fd6c6-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd6c6-136"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fd6c6-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="fd6c6-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fd6c6-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="fd6c6-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd6c6-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="fd6c6-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fd6c6-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd6c6-140"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="fd6c6-140"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="fd6c6-141">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="fd6c6-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fd6c6-142">**AddMonitorW** (Unicode) y **AddMonitorA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="fd6c6-142">**AddMonitorW** (Unicode) and **AddMonitorA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="fd6c6-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd6c6-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd6c6-144">Impresión</span><span class="sxs-lookup"><span data-stu-id="fd6c6-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="fd6c6-145">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="fd6c6-145">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="fd6c6-146">**DeleteMonitor**</span><span class="sxs-lookup"><span data-stu-id="fd6c6-146">**DeleteMonitor**</span></span>](deletemonitor.md)
</dt> <dt>

[<span data-ttu-id="fd6c6-147">**EnumMonitors**</span><span class="sxs-lookup"><span data-stu-id="fd6c6-147">**EnumMonitors**</span></span>](enummonitors.md)
</dt> <dt>

[<span data-ttu-id="fd6c6-148">**Información de supervisión \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="fd6c6-148">**MONITOR\_INFO\_2**</span></span>](monitor-info-2.md)
</dt> </dl>

 

