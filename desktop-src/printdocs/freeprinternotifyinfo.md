---
description: La función FreePrinterNotifyInfo libera un búfer asignado por el sistema creado por la función FindNextPrinterChangeNotification.
ms.assetid: e50d4718-3682-486b-9d07-ddddd0b284dc
title: Función FreePrinterNotifyInfo (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreePrinterNotifyInfo
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 8d2cc22971c2645af250a9e92872b89959387163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706307"
---
# <a name="freeprinternotifyinfo-function"></a><span data-ttu-id="93434-103">FreePrinterNotifyInfo función)</span><span class="sxs-lookup"><span data-stu-id="93434-103">FreePrinterNotifyInfo function</span></span>

<span data-ttu-id="93434-104">La función **FreePrinterNotifyInfo** libera un búfer asignado por el sistema creado por la función [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="93434-104">The **FreePrinterNotifyInfo** function frees a system-allocated buffer created by the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="93434-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="93434-105">Syntax</span></span>


```C++
BOOL FreePrinterNotifyInfo(
  _In_ PPRINTER_NOTIFY_INFO pPrinterNotifyInfo
);
```



## <a name="parameters"></a><span data-ttu-id="93434-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="93434-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93434-107">*pPrinterNotifyInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="93434-107">*pPrinterNotifyInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93434-108">Puntero a un búfer de [**\_ \_ información de notificación de impresora**](printer-notify-info.md) devuelto desde una llamada a la función [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="93434-108">Pointer to a [**PRINTER\_NOTIFY\_INFO**](printer-notify-info.md) buffer returned from a call to the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function.</span></span> <span data-ttu-id="93434-109">**FreePrinterNotifyInfo** desasigna este búfer.</span><span class="sxs-lookup"><span data-stu-id="93434-109">**FreePrinterNotifyInfo** deallocates this buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93434-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="93434-110">Return value</span></span>

<span data-ttu-id="93434-111">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="93434-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="93434-112">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="93434-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="93434-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="93434-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="93434-114">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="93434-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="93434-115">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="93434-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="93434-116">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="93434-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="93434-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93434-117">Requirements</span></span>



| <span data-ttu-id="93434-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="93434-118">Requirement</span></span> | <span data-ttu-id="93434-119">Value</span><span class="sxs-lookup"><span data-stu-id="93434-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93434-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93434-120">Minimum supported client</span></span><br/> | <span data-ttu-id="93434-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="93434-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="93434-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93434-122">Minimum supported server</span></span><br/> | <span data-ttu-id="93434-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="93434-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="93434-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="93434-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="93434-125"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="93434-125"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="93434-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="93434-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="93434-127"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93434-127"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="93434-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="93434-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93434-129"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93434-129"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="93434-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="93434-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93434-131">Impresión</span><span class="sxs-lookup"><span data-stu-id="93434-131">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="93434-132">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="93434-132">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="93434-133">**FindNextPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="93434-133">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="93434-134">**\_información de notificación de impresora \_**</span><span class="sxs-lookup"><span data-stu-id="93434-134">**PRINTER\_NOTIFY\_INFO**</span></span>](printer-notify-info.md)
</dt> </dl>

 

 




