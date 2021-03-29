---
description: La función AddPort agrega el nombre de un puerto a la lista de puertos admitidos. El monitor de Puerto exporta la función AddPort.
ms.assetid: 9191d507-9167-4488-a4b4-286590a8a62a
title: Función AddPort (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPort
- AddPortA
- AddPortW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 00e589b59b15c898887090b12348f23fac57fda3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912962"
---
# <a name="addport-function"></a><span data-ttu-id="8f9fb-104">AddPort función)</span><span class="sxs-lookup"><span data-stu-id="8f9fb-104">AddPort function</span></span>

<span data-ttu-id="8f9fb-105">La función **AddPort** agrega el nombre de un puerto a la lista de puertos admitidos.</span><span class="sxs-lookup"><span data-stu-id="8f9fb-105">The **AddPort** function adds the name of a port to the list of supported ports.</span></span> <span data-ttu-id="8f9fb-106">El monitor de Puerto exporta la función **AddPort** .</span><span class="sxs-lookup"><span data-stu-id="8f9fb-106">The **AddPort** function is exported by the port monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f9fb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8f9fb-107">Syntax</span></span>


```C++
BOOL AddPort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pMonitorName
);
```



## <a name="parameters"></a><span data-ttu-id="8f9fb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8f9fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f9fb-109">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8f9fb-109">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f9fb-110">Puntero a una cadena terminada en cero que especifica el nombre del servidor al que está conectado el puerto.</span><span class="sxs-lookup"><span data-stu-id="8f9fb-110">A pointer to a zero-terminated string that specifies the name of the server to which the port is connected.</span></span> <span data-ttu-id="8f9fb-111">Si este parámetro es **null**, el puerto es local.</span><span class="sxs-lookup"><span data-stu-id="8f9fb-111">If this parameter is **NULL**, the port is local.</span></span>

</dd> <dt>

<span data-ttu-id="8f9fb-112">*hWnd* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8f9fb-112">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f9fb-113">Identificador de la ventana primaria del cuadro de diálogo **AddPort** .</span><span class="sxs-lookup"><span data-stu-id="8f9fb-113">A handle to the parent window of the **AddPort** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="8f9fb-114">*pMonitorName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8f9fb-114">*pMonitorName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f9fb-115">Puntero a una cadena terminada en cero que especifica el monitor asociado al puerto.</span><span class="sxs-lookup"><span data-stu-id="8f9fb-115">A pointer to a zero-terminated string that specifies the monitor associated with the port.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f9fb-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8f9fb-116">Return value</span></span>

<span data-ttu-id="8f9fb-117">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="8f9fb-117">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="8f9fb-118">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="8f9fb-118">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f9fb-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f9fb-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8f9fb-120">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="8f9fb-120">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="8f9fb-121">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="8f9fb-121">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="8f9fb-122">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="8f9fb-122">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="8f9fb-123">La función **AddPort** examina la red para buscar los puertos existentes y muestra un cuadro de diálogo para el usuario.</span><span class="sxs-lookup"><span data-stu-id="8f9fb-123">The **AddPort** function browses the network to find existing ports, and displays a dialog box for the user.</span></span> <span data-ttu-id="8f9fb-124">La función **AddPort** debe validar el nombre de puerto especificado por el usuario mediante una llamada a [**EnumPorts**](enumports.md) para asegurarse de que no existe ningún nombre duplicado.</span><span class="sxs-lookup"><span data-stu-id="8f9fb-124">The **AddPort** function should validate the port name entered by the user by calling [**EnumPorts**](enumports.md) to ensure that no duplicate names exist.</span></span>

<span data-ttu-id="8f9fb-125">El autor de la llamada de la función **AddPort** debe tener acceso al servidor \_ \_ para administrar el acceso al servidor al que está conectado el puerto.</span><span class="sxs-lookup"><span data-stu-id="8f9fb-125">The caller of the **AddPort** function must have SERVER\_ACCESS\_ADMINISTER access to the server to which the port is connected.</span></span>

<span data-ttu-id="8f9fb-126">Para agregar un puerto sin mostrar un cuadro de diálogo, llame a la función **XcvData** en lugar de a **AddPort**.</span><span class="sxs-lookup"><span data-stu-id="8f9fb-126">To add a port without displaying a dialog box, call the **XcvData** function instead of **AddPort**.</span></span> <span data-ttu-id="8f9fb-127">Para obtener más información acerca de **XcvData**, vea el kit de desarrollo de controladores (DDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="8f9fb-127">For more information about **XcvData**, see the Microsoft Windows Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f9fb-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f9fb-128">Requirements</span></span>



| <span data-ttu-id="8f9fb-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f9fb-129">Requirement</span></span> | <span data-ttu-id="8f9fb-130">Value</span><span class="sxs-lookup"><span data-stu-id="8f9fb-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f9fb-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f9fb-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8f9fb-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8f9fb-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8f9fb-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f9fb-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8f9fb-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8f9fb-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8f9fb-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f9fb-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f9fb-136"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8f9fb-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="8f9fb-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8f9fb-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="8f9fb-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f9fb-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="8f9fb-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8f9fb-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f9fb-140"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f9fb-140"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="8f9fb-141">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="8f9fb-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8f9fb-142">**AddPortW** (Unicode) y **AddPortA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8f9fb-142">**AddPortW** (Unicode) and **AddPortA** (ANSI)</span></span><br/>                                                 |



## <a name="see-also"></a><span data-ttu-id="8f9fb-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f9fb-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f9fb-144">Impresión</span><span class="sxs-lookup"><span data-stu-id="8f9fb-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8f9fb-145">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="8f9fb-145">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="8f9fb-146">**DeletePort**</span><span class="sxs-lookup"><span data-stu-id="8f9fb-146">**DeletePort**</span></span>](deleteport.md)
</dt> <dt>

[<span data-ttu-id="8f9fb-147">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="8f9fb-147">**EnumPorts**</span></span>](enumports.md)
</dt> <dt>

[<span data-ttu-id="8f9fb-148">**SetPort**</span><span class="sxs-lookup"><span data-stu-id="8f9fb-148">**SetPort**</span></span>](setport.md)
</dt> </dl>

 

 




