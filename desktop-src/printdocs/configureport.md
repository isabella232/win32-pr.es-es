---
description: La función ConfigurePort muestra el cuadro de diálogo de configuración de puerto para un puerto en el servidor especificado.
ms.assetid: a65e9876-d6af-48c2-9e6b-8bd8695db130
title: Función ConfigurePort (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurePort
- ConfigurePortA
- ConfigurePortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 64f9b3f2e0b0896afdc878477c6e45f8916268a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001917"
---
# <a name="configureport-function"></a><span data-ttu-id="791e8-103">ConfigurePort función)</span><span class="sxs-lookup"><span data-stu-id="791e8-103">ConfigurePort function</span></span>

<span data-ttu-id="791e8-104">La función **ConfigurePort** muestra el cuadro de diálogo de configuración de puerto para un puerto en el servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="791e8-104">The **ConfigurePort** function displays the port-configuration dialog box for a port on the specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="791e8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="791e8-105">Syntax</span></span>


```C++
BOOL ConfigurePort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pPortName
);
```



## <a name="parameters"></a><span data-ttu-id="791e8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="791e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="791e8-107">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="791e8-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="791e8-108">Puntero a una cadena terminada en null que especifica el nombre del servidor en el que existe el puerto especificado.</span><span class="sxs-lookup"><span data-stu-id="791e8-108">Pointer to a null-terminated string that specifies the name of the server on which the specified port exists.</span></span> <span data-ttu-id="791e8-109">Si este parámetro es **null**, el puerto es local.</span><span class="sxs-lookup"><span data-stu-id="791e8-109">If this parameter is **NULL**, the port is local.</span></span>

</dd> <dt>

<span data-ttu-id="791e8-110">*hWnd* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="791e8-110">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="791e8-111">Identificador de la ventana primaria del cuadro de diálogo Configuración de puerto.</span><span class="sxs-lookup"><span data-stu-id="791e8-111">Handle to the parent window of the port-configuration dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="791e8-112">*pPortName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="791e8-112">*pPortName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="791e8-113">Puntero a una cadena terminada en null que especifica el nombre del puerto que se va a configurar.</span><span class="sxs-lookup"><span data-stu-id="791e8-113">Pointer to a null-terminated string that specifies the name of the port to be configured.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="791e8-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="791e8-114">Return value</span></span>

<span data-ttu-id="791e8-115">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="791e8-115">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="791e8-116">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="791e8-116">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="791e8-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="791e8-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="791e8-118">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="791e8-118">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="791e8-119">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="791e8-119">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="791e8-120">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="791e8-120">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="791e8-121">Antes de llamar a la función **ConfigurePort** , una aplicación debe llamar a la función [**EnumPorts**](enumports.md) para determinar los nombres de Puerto válidos.</span><span class="sxs-lookup"><span data-stu-id="791e8-121">Before calling the **ConfigurePort** function, an application should call the [**EnumPorts**](enumports.md) function to determine valid port names.</span></span>

## <a name="requirements"></a><span data-ttu-id="791e8-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="791e8-122">Requirements</span></span>



| <span data-ttu-id="791e8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="791e8-123">Requirement</span></span> | <span data-ttu-id="791e8-124">Value</span><span class="sxs-lookup"><span data-stu-id="791e8-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="791e8-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="791e8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="791e8-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="791e8-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="791e8-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="791e8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="791e8-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="791e8-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="791e8-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="791e8-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="791e8-130"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="791e8-130"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="791e8-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="791e8-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="791e8-132"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="791e8-132"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="791e8-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="791e8-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="791e8-134"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="791e8-134"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="791e8-135">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="791e8-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="791e8-136">**ConfigurePortW** (Unicode) y **ConfigurePortA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="791e8-136">**ConfigurePortW** (Unicode) and **ConfigurePortA** (ANSI)</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="791e8-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="791e8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="791e8-138">Impresión</span><span class="sxs-lookup"><span data-stu-id="791e8-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="791e8-139">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="791e8-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="791e8-140">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="791e8-140">**EnumPorts**</span></span>](enumports.md)
</dt> </dl>

 

 




