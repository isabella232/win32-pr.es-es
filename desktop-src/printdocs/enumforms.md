---
description: La función EnumForms enumera los formatos admitidos por la impresora especificada.
ms.assetid: b13b515a-c764-4a80-ab85-95fb4abb2a6b
title: Función EnumForms (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumForms
- EnumFormsA
- EnumFormsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 18cd9ad6f8e0491700d5618e29a0a629e8045366
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360659"
---
# <a name="enumforms-function"></a><span data-ttu-id="5d7be-103">EnumForms función)</span><span class="sxs-lookup"><span data-stu-id="5d7be-103">EnumForms function</span></span>

<span data-ttu-id="5d7be-104">La función **EnumForms** enumera los formatos admitidos por la impresora especificada.</span><span class="sxs-lookup"><span data-stu-id="5d7be-104">The **EnumForms** function enumerates the forms supported by the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d7be-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d7be-105">Syntax</span></span>


```C++
BOOL EnumForms(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pForm,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="5d7be-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5d7be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d7be-107">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5d7be-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d7be-108">Identificador de la impresora para la que se deben enumerar los formularios.</span><span class="sxs-lookup"><span data-stu-id="5d7be-108">Handle to the printer for which the forms should be enumerated.</span></span> <span data-ttu-id="5d7be-109">Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="5d7be-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="5d7be-110">*Nivel* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="5d7be-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d7be-111">Especifica la versión de la estructura a la que apunta *pForm* .</span><span class="sxs-lookup"><span data-stu-id="5d7be-111">Specifies the version of the structure to which *pForm* points.</span></span> <span data-ttu-id="5d7be-112">Este valor debe ser 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="5d7be-112">This value must be 1 or 2.</span></span>

</dd> <dt>

<span data-ttu-id="5d7be-113">*pForm* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5d7be-113">*pForm* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d7be-114">Puntero a una o varias estructuras de [**Form \_ info \_ 1**](form-info-1.md) o a una o varias estructuras de [**Form \_ info \_ 2**](form-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="5d7be-114">Pointer to one or more [**FORM\_INFO\_1**](form-info-1.md) structures or to one or more [**FORM\_INFO\_2**](form-info-2.md) structures.</span></span> <span data-ttu-id="5d7be-115">Todas las estructuras tendrán el mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="5d7be-115">All the structures will have the same level.</span></span>

</dd> <dt>

<span data-ttu-id="5d7be-116">*cbBuf* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5d7be-116">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d7be-117">Especifica el tamaño, en bytes, del búfer al que apunta *pForm* .</span><span class="sxs-lookup"><span data-stu-id="5d7be-117">Specifies the size, in bytes, of the buffer to which *pForm* points.</span></span>

</dd> <dt>

<span data-ttu-id="5d7be-118">*pcbNeeded* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5d7be-118">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d7be-119">Puntero a una variable que recibe el número de bytes copiados en la matriz a la que *pForm* apunta (si la operación se realiza correctamente) o el número de bytes necesarios (si se produce un error porque *cbBuf* es demasiado pequeño).</span><span class="sxs-lookup"><span data-stu-id="5d7be-119">Pointer to a variable that receives the number of bytes copied to the array to which *pForm* points (if the operation succeeds) or the number of bytes required (if it fails because *cbBuf* is too small).</span></span>

</dd> <dt>

<span data-ttu-id="5d7be-120">*pcReturned* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5d7be-120">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d7be-121">Puntero a una variable que recibe el número de estructuras copiadas en la matriz a la que apunta *pForm* .</span><span class="sxs-lookup"><span data-stu-id="5d7be-121">Pointer to a variable that receives the number of structures copied into the array to which *pForm* points.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d7be-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5d7be-122">Return value</span></span>

<span data-ttu-id="5d7be-123">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="5d7be-123">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="5d7be-124">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="5d7be-124">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d7be-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5d7be-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5d7be-126">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="5d7be-126">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="5d7be-127">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="5d7be-127">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="5d7be-128">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="5d7be-128">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="5d7be-129">Si el autor de la llamada es remoto y el *nivel* es 2, el valor de **StringType** de las estructuras devueltas de la [**información del formulario \_ \_ 2**](form-info-2.md) será siempre **String \_ LANGPAIR**.</span><span class="sxs-lookup"><span data-stu-id="5d7be-129">If the caller is remote, and the *Level* is 2, the **StringType** value of the returned [**FORM\_INFO\_2**](form-info-2.md) structures will always be **STRING\_LANGPAIR**.</span></span>

<span data-ttu-id="5d7be-130">En Windows Vista, los datos del formulario devueltos por **EnumForms** se recuperan de una caché local cuando *hPrinter* hace referencia a un servidor de impresión remoto o a una impresora hospedada por un servidor de impresión y hay al menos una conexión abierta a una impresora en el servidor de impresión remoto.</span><span class="sxs-lookup"><span data-stu-id="5d7be-130">In Windows Vista, the form data returned by **EnumForms** is retrieved from a local cache when *hPrinter* refers to a remote print server or a printer hosted by a print server and there is at least one open connection to a printer on the remote print server.</span></span> <span data-ttu-id="5d7be-131">En todas las demás configuraciones, se consultan los datos del formulario desde el servidor de impresión remoto.</span><span class="sxs-lookup"><span data-stu-id="5d7be-131">In all other configurations, the form data is queried from the remote print server.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d7be-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d7be-132">Requirements</span></span>



| <span data-ttu-id="5d7be-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d7be-133">Requirement</span></span> | <span data-ttu-id="5d7be-134">Value</span><span class="sxs-lookup"><span data-stu-id="5d7be-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d7be-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d7be-135">Minimum supported client</span></span><br/> | <span data-ttu-id="5d7be-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5d7be-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5d7be-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d7be-137">Minimum supported server</span></span><br/> | <span data-ttu-id="5d7be-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5d7be-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5d7be-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5d7be-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d7be-140"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5d7be-140"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="5d7be-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5d7be-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="5d7be-142"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d7be-142"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="5d7be-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5d7be-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d7be-144"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="5d7be-144"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="5d7be-145">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="5d7be-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5d7be-146">**EnumFormsW** (Unicode) y **EnumFormsA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5d7be-146">**EnumFormsW** (Unicode) and **EnumFormsA** (ANSI)</span></span><br/>                                             |



## <a name="see-also"></a><span data-ttu-id="5d7be-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d7be-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d7be-148">Impresión</span><span class="sxs-lookup"><span data-stu-id="5d7be-148">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="5d7be-149">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="5d7be-149">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="5d7be-150">**AddPrinter (**</span><span class="sxs-lookup"><span data-stu-id="5d7be-150">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="5d7be-151">**Información de formulario \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="5d7be-151">**FORM\_INFO\_1**</span></span>](form-info-1.md)
</dt> <dt>

[<span data-ttu-id="5d7be-152">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="5d7be-152">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




