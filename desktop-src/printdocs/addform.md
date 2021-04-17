---
description: La función AddForm agrega un formulario a la lista de formularios disponibles que se pueden seleccionar para la impresora especificada.
ms.assetid: 17b59019-f93a-4b57-86fb-91c61aecbac4
title: Función AddForm (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddForm
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 2de3ddbdc57a5a41bac048a94a8175cd124df4ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697138"
---
# <a name="addform-function"></a><span data-ttu-id="4b198-103">AddForm función)</span><span class="sxs-lookup"><span data-stu-id="4b198-103">AddForm function</span></span>

<span data-ttu-id="4b198-104">La función **AddForm** agrega un formulario a la lista de formularios disponibles que se pueden seleccionar para la impresora especificada.</span><span class="sxs-lookup"><span data-stu-id="4b198-104">The **AddForm** function adds a form to the list of available forms that can be selected for the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b198-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b198-105">Syntax</span></span>


```C++
BOOL AddForm(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pForm
);
```



## <a name="parameters"></a><span data-ttu-id="4b198-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4b198-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b198-107">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4b198-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b198-108">Identificador de la impresora que admite la impresión con el formato especificado.</span><span class="sxs-lookup"><span data-stu-id="4b198-108">A handle to the printer that supports printing with the specified form.</span></span> <span data-ttu-id="4b198-109">Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="4b198-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="4b198-110">*Nivel* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4b198-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b198-111">Nivel de la estructura a la que apunta *pForm* .</span><span class="sxs-lookup"><span data-stu-id="4b198-111">The level of the structure to which *pForm* points.</span></span> <span data-ttu-id="4b198-112">Este valor debe ser 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="4b198-112">This value must be 1 or 2.</span></span>

</dd> <dt>

<span data-ttu-id="4b198-113">*pForm* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4b198-113">*pForm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b198-114">Puntero a una estructura de [**formulario de \_ información \_ 1**](form-info-1.md) o de [**formulario de \_ información \_ 2**](form-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="4b198-114">A pointer to a [**FORM\_INFO\_1**](form-info-1.md) or [**FORM\_INFO\_2**](form-info-2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b198-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4b198-115">Return value</span></span>

<span data-ttu-id="4b198-116">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="4b198-116">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="4b198-117">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="4b198-117">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b198-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4b198-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4b198-119">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="4b198-119">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="4b198-120">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="4b198-120">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="4b198-121">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="4b198-121">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="4b198-122">Una aplicación puede determinar qué formularios están disponibles para una impresora mediante una llamada a la función [**EnumForms**](enumforms.md) .</span><span class="sxs-lookup"><span data-stu-id="4b198-122">An application can determine which forms are available for a printer by calling the [**EnumForms**](enumforms.md) function.</span></span>

<span data-ttu-id="4b198-123">Si *pForm* señala a un [**formulario de \_ información \_ 2**](form-info-2.md), se producirá un error en **AddForm** si ya existe un formulario con el nombre especificado o si el valor *pKeyword* de la estructura ya existe.</span><span class="sxs-lookup"><span data-stu-id="4b198-123">If *pForm* points to a [**FORM\_INFO\_2**](form-info-2.md), then **AddForm** will fail if either a form with the specified name already exists or the structure's *pKeyword* value already exists.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b198-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b198-124">Requirements</span></span>



| <span data-ttu-id="4b198-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b198-125">Requirement</span></span> | <span data-ttu-id="4b198-126">Value</span><span class="sxs-lookup"><span data-stu-id="4b198-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b198-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b198-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4b198-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4b198-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4b198-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b198-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4b198-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4b198-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4b198-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4b198-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b198-132"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4b198-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="4b198-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4b198-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="4b198-134"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4b198-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="4b198-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4b198-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b198-136"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b198-136"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="4b198-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b198-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b198-138">Impresión</span><span class="sxs-lookup"><span data-stu-id="4b198-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4b198-139">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="4b198-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="4b198-140">**EnumForms**</span><span class="sxs-lookup"><span data-stu-id="4b198-140">**EnumForms**</span></span>](enumforms.md)
</dt> <dt>

[<span data-ttu-id="4b198-141">**Información de formulario \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="4b198-141">**FORM\_INFO\_1**</span></span>](form-info-1.md)
</dt> <dt>

[<span data-ttu-id="4b198-142">**Información de formulario \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="4b198-142">**FORM\_INFO\_2**</span></span>](form-info-2.md)
</dt> <dt>

[<span data-ttu-id="4b198-143">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="4b198-143">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




