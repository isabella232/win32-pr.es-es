---
description: La función SetForm establece la información del formulario para la impresora especificada.
ms.assetid: 05d5d495-952c-4a1d-8694-1004d0c2bcf6
title: Función SetForm (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetForm
- SetFormA
- SetFormW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 93848afa0f36032bb972f8f4a7c6c3d5eb8c42ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360655"
---
# <a name="setform-function"></a><span data-ttu-id="6389e-103">SetForm función)</span><span class="sxs-lookup"><span data-stu-id="6389e-103">SetForm function</span></span>

<span data-ttu-id="6389e-104">La función **SetForm** establece la información del formulario para la impresora especificada.</span><span class="sxs-lookup"><span data-stu-id="6389e-104">The **SetForm** function sets the form information for the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="6389e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6389e-105">Syntax</span></span>


```C++
BOOL SetForm(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pFormName,
  _In_ DWORD  Level,
  _In_ LPTSTR pForm
);
```



## <a name="parameters"></a><span data-ttu-id="6389e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6389e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6389e-107">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6389e-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6389e-108">Identificador de la impresora para la que se establece la información del formulario.</span><span class="sxs-lookup"><span data-stu-id="6389e-108">A handle to the printer for which the form information is set.</span></span> <span data-ttu-id="6389e-109">Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="6389e-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="6389e-110">*pFormName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6389e-110">*pFormName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6389e-111">Puntero a una cadena terminada en null que especifica el nombre del formulario para el que se establece la información del formulario.</span><span class="sxs-lookup"><span data-stu-id="6389e-111">A pointer to a null-terminated string that specifies the form name for which the form information is set.</span></span>

</dd> <dt>

<span data-ttu-id="6389e-112">*Nivel* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6389e-112">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6389e-113">Versión de la estructura a la que apunta *pForm* .</span><span class="sxs-lookup"><span data-stu-id="6389e-113">The version of the structure to which *pForm* points.</span></span> <span data-ttu-id="6389e-114">Este valor debe ser 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="6389e-114">This value must be 1 or 2.</span></span>

</dd> <dt>

<span data-ttu-id="6389e-115">*pForm* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6389e-115">*pForm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6389e-116">Puntero a una estructura de [**formulario de \_ información \_ 1**](form-info-1.md) o de [**formulario de \_ información \_ 2**](form-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="6389e-116">A pointer to a [**FORM\_INFO\_1**](form-info-1.md) or [**FORM\_INFO\_2**](form-info-2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6389e-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6389e-117">Return value</span></span>

<span data-ttu-id="6389e-118">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="6389e-118">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="6389e-119">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="6389e-119">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6389e-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6389e-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6389e-121">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="6389e-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="6389e-122">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="6389e-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="6389e-123">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="6389e-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="6389e-124">Se puede llamar a **SetForm** varias veces para un [**formulario existente \_ info \_ 2**](form-info-2.md), cada llamada agrega pares adicionales de valores **pDisplayName** y **wLangId** .</span><span class="sxs-lookup"><span data-stu-id="6389e-124">**SetForm** can be called multiple times for an existing [**FORM\_INFO\_2**](form-info-2.md), each call adding additional pairs of **pDisplayName** and **wLangId** values.</span></span> <span data-ttu-id="6389e-125">Todas las versiones de idioma del formulario obtendrán los valores de **tamaño** y **ImageableArea** del **formulario de \_ información \_ 2** en la llamada más reciente a **SetForm**.</span><span class="sxs-lookup"><span data-stu-id="6389e-125">All languages versions of the form will get the **Size** and **ImageableArea** values of the **FORM\_INFO\_2** in the most recent call to **SetForm**.</span></span>

<span data-ttu-id="6389e-126">Si el autor de la llamada es remoto y el *nivel* es 2, el valor **StringType** de la [**forma \_ info \_ 2**](form-info-2.md) no puede ser String \_ MUIDLL.</span><span class="sxs-lookup"><span data-stu-id="6389e-126">If the caller is remote and the *Level* is 2, the **StringType** value of the [**FORM\_INFO\_2**](form-info-2.md) cannot be STRING\_MUIDLL.</span></span>

## <a name="requirements"></a><span data-ttu-id="6389e-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6389e-127">Requirements</span></span>



| <span data-ttu-id="6389e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6389e-128">Requirement</span></span> | <span data-ttu-id="6389e-129">Value</span><span class="sxs-lookup"><span data-stu-id="6389e-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6389e-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6389e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6389e-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6389e-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6389e-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6389e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6389e-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6389e-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6389e-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6389e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="6389e-135"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6389e-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="6389e-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6389e-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="6389e-137"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6389e-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="6389e-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6389e-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6389e-139"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="6389e-139"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="6389e-140">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="6389e-140">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6389e-141">**SetFormW** (Unicode) y **SetFormA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6389e-141">**SetFormW** (Unicode) and **SetFormA** (ANSI)</span></span><br/>                                                 |



## <a name="see-also"></a><span data-ttu-id="6389e-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="6389e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6389e-143">Impresión</span><span class="sxs-lookup"><span data-stu-id="6389e-143">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="6389e-144">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="6389e-144">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="6389e-145">**GetForm**</span><span class="sxs-lookup"><span data-stu-id="6389e-145">**GetForm**</span></span>](getform.md)
</dt> <dt>

[<span data-ttu-id="6389e-146">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="6389e-146">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="6389e-147">**Información de formulario \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="6389e-147">**FORM\_INFO\_1**</span></span>](form-info-1.md)
</dt> <dt>

[<span data-ttu-id="6389e-148">**Información de formulario \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="6389e-148">**FORM\_INFO\_2**</span></span>](form-info-2.md)
</dt> </dl>

 

 




