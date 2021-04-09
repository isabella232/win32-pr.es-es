---
description: La función DeleteForm quita un nombre de formulario de la lista de formularios admitidos.
ms.assetid: a2d0345f-2469-46ab-935f-777f2b33b621
title: Función DeleteForm (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteForm
- DeleteFormA
- DeleteFormW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 70ead5026c3b5cf21b28d230f79819bf71eeaf10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082638"
---
# <a name="deleteform-function"></a><span data-ttu-id="4bd0e-103">DeleteForm función)</span><span class="sxs-lookup"><span data-stu-id="4bd0e-103">DeleteForm function</span></span>

<span data-ttu-id="4bd0e-104">La función **DeleteForm** quita un nombre de formulario de la lista de formularios admitidos.</span><span class="sxs-lookup"><span data-stu-id="4bd0e-104">The **DeleteForm** function removes a form name from the list of supported forms.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bd0e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4bd0e-105">Syntax</span></span>


```C++
BOOL DeleteForm(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pFormName
);
```



## <a name="parameters"></a><span data-ttu-id="4bd0e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4bd0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bd0e-107">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4bd0e-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bd0e-108">Indica el identificador de impresora abierto en el que se va a realizar esta función.</span><span class="sxs-lookup"><span data-stu-id="4bd0e-108">Indicates the open printer handle that this function is to be performed upon.</span></span> <span data-ttu-id="4bd0e-109">Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="4bd0e-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="4bd0e-110">*pFormName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4bd0e-110">*pFormName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bd0e-111">Puntero al nombre del formulario que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="4bd0e-111">Pointer to the form name to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bd0e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4bd0e-112">Return value</span></span>

<span data-ttu-id="4bd0e-113">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="4bd0e-113">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="4bd0e-114">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="4bd0e-114">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bd0e-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4bd0e-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4bd0e-116">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="4bd0e-116">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="4bd0e-117">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="4bd0e-117">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="4bd0e-118">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="4bd0e-118">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="4bd0e-119">**DeleteForm** solo puede eliminar nombres de formulario que se agregaron mediante la función [**AddForm**](addform.md) .</span><span class="sxs-lookup"><span data-stu-id="4bd0e-119">**DeleteForm** can only delete form names that were added by using the [**AddForm**](addform.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bd0e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4bd0e-120">Requirements</span></span>



| <span data-ttu-id="4bd0e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bd0e-121">Requirement</span></span> | <span data-ttu-id="4bd0e-122">Value</span><span class="sxs-lookup"><span data-stu-id="4bd0e-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bd0e-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4bd0e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4bd0e-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4bd0e-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4bd0e-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4bd0e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4bd0e-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4bd0e-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4bd0e-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4bd0e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bd0e-128"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4bd0e-128"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="4bd0e-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4bd0e-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="4bd0e-130"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4bd0e-130"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="4bd0e-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4bd0e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bd0e-132"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="4bd0e-132"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="4bd0e-133">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="4bd0e-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4bd0e-134">**DeleteFormW** (Unicode) y **DeleteFormA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4bd0e-134">**DeleteFormW** (Unicode) and **DeleteFormA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="4bd0e-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="4bd0e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bd0e-136">Impresión</span><span class="sxs-lookup"><span data-stu-id="4bd0e-136">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4bd0e-137">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="4bd0e-137">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="4bd0e-138">**AddForm**</span><span class="sxs-lookup"><span data-stu-id="4bd0e-138">**AddForm**</span></span>](addform.md)
</dt> <dt>

[<span data-ttu-id="4bd0e-139">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="4bd0e-139">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




