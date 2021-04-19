---
description: La función DeleteMonitor quita un monitor de Puerto agregado por la función AddMonitor.
ms.assetid: 32548d4f-830a-471d-8a72-c0f62f43ffa2
title: Función DeleteMonitor (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteMonitor
- DeleteMonitorA
- DeleteMonitorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 0f11504be516f79610200d4f7da9d571ae1cab9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697135"
---
# <a name="deletemonitor-function"></a><span data-ttu-id="436cf-103">DeleteMonitor función)</span><span class="sxs-lookup"><span data-stu-id="436cf-103">DeleteMonitor function</span></span>

<span data-ttu-id="436cf-104">La función **DeleteMonitor** quita un monitor de Puerto agregado por la función [**AddMonitor**](addmonitor.md) .</span><span class="sxs-lookup"><span data-stu-id="436cf-104">The **DeleteMonitor** function removes a port monitor added by the [**AddMonitor**](addmonitor.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="436cf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="436cf-105">Syntax</span></span>


```C++
BOOL DeleteMonitor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pMonitorName
);
```



## <a name="parameters"></a><span data-ttu-id="436cf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="436cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="436cf-107">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="436cf-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="436cf-108">Puntero a una cadena terminada en null que especifica el nombre del servidor desde el que se va a quitar el monitor.</span><span class="sxs-lookup"><span data-stu-id="436cf-108">A pointer to a null-terminated string that specifies the name of the server from which the monitor is to be removed.</span></span> <span data-ttu-id="436cf-109">Si este parámetro es **null**, el monitor de puerto se quita localmente.</span><span class="sxs-lookup"><span data-stu-id="436cf-109">If this parameter is **NULL**, the port monitor is removed locally.</span></span>

</dd> <dt>

<span data-ttu-id="436cf-110">*pEnvironment* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="436cf-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="436cf-111">Puntero a una cadena terminada en null que especifica el entorno desde el que se va a quitar el monitor (por ejemplo, Windows x86, Windows IA64 o Windows x64).</span><span class="sxs-lookup"><span data-stu-id="436cf-111">A pointer to a null-terminated string that specifies the environment from which the monitor is to be removed (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="436cf-112">Si este parámetro es **null**, el monitor se quita del entorno actual de la aplicación que realiza la llamada y del equipo cliente (no de la aplicación de destino y del servidor de impresión).</span><span class="sxs-lookup"><span data-stu-id="436cf-112">If this parameter is **NULL**, the monitor is removed from the current environment of the calling application and client machine (not of the destination application and print server).</span></span>

</dd> <dt>

<span data-ttu-id="436cf-113">*pMonitorName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="436cf-113">*pMonitorName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="436cf-114">Puntero a una cadena terminada en null que especifica el nombre del monitor que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="436cf-114">A pointer to a null-terminated string that specifies the name of the monitor to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="436cf-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="436cf-115">Return value</span></span>

<span data-ttu-id="436cf-116">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="436cf-116">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="436cf-117">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="436cf-117">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="436cf-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="436cf-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="436cf-119">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="436cf-119">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="436cf-120">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="436cf-120">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="436cf-121">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="436cf-121">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="436cf-122">El autor de la llamada debe tener [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="436cf-122">The caller must have [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

## <a name="requirements"></a><span data-ttu-id="436cf-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="436cf-123">Requirements</span></span>



| <span data-ttu-id="436cf-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="436cf-124">Requirement</span></span> | <span data-ttu-id="436cf-125">Value</span><span class="sxs-lookup"><span data-stu-id="436cf-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="436cf-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="436cf-126">Minimum supported client</span></span><br/> | <span data-ttu-id="436cf-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="436cf-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="436cf-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="436cf-128">Minimum supported server</span></span><br/> | <span data-ttu-id="436cf-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="436cf-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="436cf-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="436cf-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="436cf-131"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="436cf-131"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="436cf-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="436cf-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="436cf-133"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="436cf-133"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="436cf-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="436cf-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="436cf-135"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="436cf-135"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="436cf-136">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="436cf-136">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="436cf-137">**DeleteMonitorW** (Unicode) y **DeleteMonitorA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="436cf-137">**DeleteMonitorW** (Unicode) and **DeleteMonitorA** (ANSI)</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="436cf-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="436cf-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="436cf-139">Impresión</span><span class="sxs-lookup"><span data-stu-id="436cf-139">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="436cf-140">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="436cf-140">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="436cf-141">**AddMonitor**</span><span class="sxs-lookup"><span data-stu-id="436cf-141">**AddMonitor**</span></span>](addmonitor.md)
</dt> </dl>

 

