---
description: La función FindClosePrinterChangeNotification cierra un objeto de notificación de cambios creado llamando a la función FindFirstPrinterChangeNotification.
ms.assetid: 2b4758f8-af0a-494b-8f1b-8ea6ee73c79b
title: Función FindClosePrinterChangeNotification (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindClosePrinterChangeNotification
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 8040944d5890aa521681827bef786201a35da039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082604"
---
# <a name="findcloseprinterchangenotification-function"></a><span data-ttu-id="f1ec2-103">FindClosePrinterChangeNotification función)</span><span class="sxs-lookup"><span data-stu-id="f1ec2-103">FindClosePrinterChangeNotification function</span></span>

<span data-ttu-id="f1ec2-104">La función **FindClosePrinterChangeNotification** cierra un objeto de notificación de cambios creado llamando a la función [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="f1ec2-104">The **FindClosePrinterChangeNotification** function closes a change notification object created by calling the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function.</span></span> <span data-ttu-id="f1ec2-105">Dicho objeto ya no supervisará la impresora o el servidor de impresión asociado al objeto de notificación de cambios.</span><span class="sxs-lookup"><span data-stu-id="f1ec2-105">The printer or print server associated with the change notification object will no longer be monitored by that object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1ec2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f1ec2-106">Syntax</span></span>


```C++
BOOL FindClosePrinterChangeNotification(
  _In_ HANDLE hChange
);
```



## <a name="parameters"></a><span data-ttu-id="f1ec2-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f1ec2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1ec2-108">*hChange* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f1ec2-108">*hChange* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1ec2-109">Identificador del objeto de notificación de cambio que se va a cerrar.</span><span class="sxs-lookup"><span data-stu-id="f1ec2-109">A handle to the change notification object to be closed.</span></span> <span data-ttu-id="f1ec2-110">Se trata de un identificador creado mediante una llamada a la función [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="f1ec2-110">This is a handle created by calling the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1ec2-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f1ec2-111">Return value</span></span>

<span data-ttu-id="f1ec2-112">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="f1ec2-112">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="f1ec2-113">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="f1ec2-113">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1ec2-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f1ec2-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f1ec2-115">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="f1ec2-115">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="f1ec2-116">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="f1ec2-116">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="f1ec2-117">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="f1ec2-117">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="f1ec2-118">Después de llamar a la función **FindClosePrinterChangeNotification** , no se puede usar el identificador *hChange* en llamadas posteriores a [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) o [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md).</span><span class="sxs-lookup"><span data-stu-id="f1ec2-118">After calling the **FindClosePrinterChangeNotification** function, you cannot use the *hChange* handle in subsequent calls to either [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) or [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f1ec2-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1ec2-119">Requirements</span></span>



| <span data-ttu-id="f1ec2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1ec2-120">Requirement</span></span> | <span data-ttu-id="f1ec2-121">Value</span><span class="sxs-lookup"><span data-stu-id="f1ec2-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1ec2-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f1ec2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f1ec2-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f1ec2-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f1ec2-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f1ec2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f1ec2-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f1ec2-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f1ec2-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f1ec2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1ec2-127"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1ec2-127"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f1ec2-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f1ec2-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="f1ec2-129"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1ec2-129"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="f1ec2-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f1ec2-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1ec2-131"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1ec2-131"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="f1ec2-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1ec2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1ec2-133">Impresión</span><span class="sxs-lookup"><span data-stu-id="f1ec2-133">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f1ec2-134">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="f1ec2-134">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="f1ec2-135">**FindFirstPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="f1ec2-135">**FindFirstPrinterChangeNotification**</span></span>](findfirstprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="f1ec2-136">**FindNextPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="f1ec2-136">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> </dl>

 

 




