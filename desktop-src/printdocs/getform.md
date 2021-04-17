---
description: La función GetForm recupera información sobre un formulario especificado.
ms.assetid: 10b25748-6d7c-46ab-bd2c-9b6126a1d7d1
title: Función GetForm (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetForm
- GetFormA
- GetFormW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 6b6ea9753e1b335936778e17562f6f26467b3083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697334"
---
# <a name="getform-function"></a><span data-ttu-id="98c37-103">GetForm función)</span><span class="sxs-lookup"><span data-stu-id="98c37-103">GetForm function</span></span>

<span data-ttu-id="98c37-104">La función **GetForm** recupera información sobre un formulario especificado.</span><span class="sxs-lookup"><span data-stu-id="98c37-104">The **GetForm** function retrieves information about a specified form.</span></span>

## <a name="syntax"></a><span data-ttu-id="98c37-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98c37-105">Syntax</span></span>


```C++
BOOL GetForm(
  _In_  HANDLE  hPrinter,
  _In_  LPTSTR  pFormName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pForm,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="98c37-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98c37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98c37-107">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="98c37-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98c37-108">Identificador de la impresora.</span><span class="sxs-lookup"><span data-stu-id="98c37-108">A handle to the printer.</span></span> <span data-ttu-id="98c37-109">Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="98c37-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="98c37-110">*pFormName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="98c37-110">*pFormName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98c37-111">Puntero a una cadena terminada en null que especifica el nombre del formulario.</span><span class="sxs-lookup"><span data-stu-id="98c37-111">A pointer to a null-terminated string that specifies the name of the form.</span></span> <span data-ttu-id="98c37-112">Para obtener los nombres de los formatos admitidos por la impresora, llame a la función [**EnumForms**](enumforms.md) .</span><span class="sxs-lookup"><span data-stu-id="98c37-112">To get the names of the forms supported by the printer, call the [**EnumForms**](enumforms.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="98c37-113">*Nivel* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="98c37-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98c37-114">Versión de la estructura a la que apunta *pForm* .</span><span class="sxs-lookup"><span data-stu-id="98c37-114">The version of the structure to which *pForm* points.</span></span> <span data-ttu-id="98c37-115">Este valor debe ser 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="98c37-115">This value must be 1 or 2.</span></span>

</dd> <dt>

<span data-ttu-id="98c37-116">*pForm* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="98c37-116">*pForm* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98c37-117">Puntero a una matriz de bytes que recibe la estructura de la [**información de formulario inicializada \_ \_ 1**](form-info-1.md) o la estructura de [**Form \_ info \_ 2**](form-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="98c37-117">A pointer to an array of bytes that receives the initialized [**FORM\_INFO\_1**](form-info-1.md) or [**FORM\_INFO\_2**](form-info-2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="98c37-118">*cbBuf* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="98c37-118">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98c37-119">Tamaño, en bytes, de la matriz *pForm* .</span><span class="sxs-lookup"><span data-stu-id="98c37-119">The size, in bytes, of the *pForm* array.</span></span>

</dd> <dt>

<span data-ttu-id="98c37-120">*pcbNeeded* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="98c37-120">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98c37-121">Un puntero a un valor que especifica el número de bytes copiados si la función se ejecuta correctamente o el número de bytes necesarios si *cbBuf* es demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="98c37-121">A pointer to a value that specifies the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98c37-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98c37-122">Return value</span></span>

<span data-ttu-id="98c37-123">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="98c37-123">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="98c37-124">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="98c37-124">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="98c37-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98c37-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="98c37-126">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="98c37-126">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="98c37-127">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="98c37-127">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="98c37-128">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="98c37-128">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="98c37-129">Si el autor de la llamada es remoto y el *nivel* es 2, el valor de **StringType** de [**la \_ información \_ de formato**](form-info-2.md) devuelto será siempre la cadena \_ LANGPAIR.</span><span class="sxs-lookup"><span data-stu-id="98c37-129">If the caller is remote, and the *Level* is 2, the **StringType** value of the returned [**FORM\_INFO\_2**](form-info-2.md) will always be STRING\_LANGPAIR.</span></span>

## <a name="requirements"></a><span data-ttu-id="98c37-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98c37-130">Requirements</span></span>



| <span data-ttu-id="98c37-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="98c37-131">Requirement</span></span> | <span data-ttu-id="98c37-132">Value</span><span class="sxs-lookup"><span data-stu-id="98c37-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98c37-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98c37-133">Minimum supported client</span></span><br/> | <span data-ttu-id="98c37-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="98c37-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="98c37-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98c37-135">Minimum supported server</span></span><br/> | <span data-ttu-id="98c37-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="98c37-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="98c37-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98c37-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="98c37-138"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="98c37-138"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="98c37-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="98c37-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="98c37-140"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="98c37-140"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="98c37-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="98c37-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98c37-142"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="98c37-142"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="98c37-143">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="98c37-143">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="98c37-144">**GetFormW** (Unicode) y **GetFormA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="98c37-144">**GetFormW** (Unicode) and **GetFormA** (ANSI)</span></span><br/>                                                 |



## <a name="see-also"></a><span data-ttu-id="98c37-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="98c37-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98c37-146">Impresión</span><span class="sxs-lookup"><span data-stu-id="98c37-146">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="98c37-147">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="98c37-147">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="98c37-148">**AddForm**</span><span class="sxs-lookup"><span data-stu-id="98c37-148">**AddForm**</span></span>](addform.md)
</dt> <dt>

[<span data-ttu-id="98c37-149">**DeleteForm**</span><span class="sxs-lookup"><span data-stu-id="98c37-149">**DeleteForm**</span></span>](deleteform.md)
</dt> <dt>

[<span data-ttu-id="98c37-150">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="98c37-150">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="98c37-151">**SetForm**</span><span class="sxs-lookup"><span data-stu-id="98c37-151">**SetForm**</span></span>](setform.md)
</dt> </dl>

 

 




