---
description: El método LogError registra un error. No es necesario que las aplicaciones llamen a este método. Se llama internamente en respuesta a los errores de representación.
ms.assetid: 08765c8a-21ca-4c40-84a8-d13da87d9c5f
title: 'IAMErrorLog:: LogError (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMErrorLog.LogError
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dc94532639f325b53db850ebe8a5af489a8b3cf2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653526"
---
# <a name="iamerrorloglogerror-method"></a><span data-ttu-id="c070c-105">IAMErrorLog:: LogError (método)</span><span class="sxs-lookup"><span data-stu-id="c070c-105">IAMErrorLog::LogError method</span></span>

> [!Note]  
> <span data-ttu-id="c070c-106">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="c070c-106">\[Deprecated.</span></span> <span data-ttu-id="c070c-107">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c070c-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c070c-108">El método **LogError** registra un error.</span><span class="sxs-lookup"><span data-stu-id="c070c-108">The **LogError** method logs an error.</span></span> <span data-ttu-id="c070c-109">No es necesario que las aplicaciones llamen a este método.</span><span class="sxs-lookup"><span data-stu-id="c070c-109">Applications do not need to call this method.</span></span> <span data-ttu-id="c070c-110">Se llama internamente en respuesta a los errores de representación.</span><span class="sxs-lookup"><span data-stu-id="c070c-110">It is called internally in response to rendering errors.</span></span>

## <a name="syntax"></a><span data-ttu-id="c070c-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c070c-111">Syntax</span></span>


```C++
HRESULT LogError(
       LONG    Severity,
       BSTR    ErrorString,
       LONG    ErrorCode,
       HRESULT hresult,
  [in] VARIANT *pExtraInfo
);
```



## <a name="parameters"></a><span data-ttu-id="c070c-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c070c-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c070c-113">*Gravedad*</span><span class="sxs-lookup"><span data-stu-id="c070c-113">*Severity*</span></span> 
</dt> <dd>

<span data-ttu-id="c070c-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="c070c-114">Reserved.</span></span> <span data-ttu-id="c070c-115">No utilizar.</span><span class="sxs-lookup"><span data-stu-id="c070c-115">Do not use.</span></span>

</dd> <dt>

<span data-ttu-id="c070c-116">*Tal*</span><span class="sxs-lookup"><span data-stu-id="c070c-116">*ErrorString*</span></span> 
</dt> <dd>

<span data-ttu-id="c070c-117">Valor de cadena que contiene el texto del error.</span><span class="sxs-lookup"><span data-stu-id="c070c-117">String value containing the text of the error.</span></span>

</dd> <dt>

<span data-ttu-id="c070c-118">*ErrorCode*</span><span class="sxs-lookup"><span data-stu-id="c070c-118">*ErrorCode*</span></span> 
</dt> <dd>

<span data-ttu-id="c070c-119">Código de error.</span><span class="sxs-lookup"><span data-stu-id="c070c-119">Error code.</span></span>

</dd> <dt>

<span data-ttu-id="c070c-120">*valor*</span><span class="sxs-lookup"><span data-stu-id="c070c-120">*hresult*</span></span> 
</dt> <dd>

<span data-ttu-id="c070c-121">Valor HRESULT devuelto por la llamada al método que produjo el error.</span><span class="sxs-lookup"><span data-stu-id="c070c-121">The HRESULT value that was returned by the method call that caused the error.</span></span>

</dd> <dt>

<span data-ttu-id="c070c-122">*pExtraInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c070c-122">*pExtraInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c070c-123">Puntero a una variante que contiene información adicional sobre el error.</span><span class="sxs-lookup"><span data-stu-id="c070c-123">Pointer to a VARIANT that contains any additional information about the error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c070c-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c070c-124">Return value</span></span>

<span data-ttu-id="c070c-125">Devuelve el valor del parámetro *HRESULT* .</span><span class="sxs-lookup"><span data-stu-id="c070c-125">Return the value of the *hresult* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="c070c-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c070c-126">Remarks</span></span>

<span data-ttu-id="c070c-127">Dentro de este método, no libere la **variante** a la que apunta *pExtraInfo*.</span><span class="sxs-lookup"><span data-stu-id="c070c-127">Within this method, do not free the **VARIANT** pointed to by *pExtraInfo*.</span></span> <span data-ttu-id="c070c-128">Además, la **variante** deja de ser válida una vez devuelto el método, por lo que no intente hacer referencia a ella más adelante.</span><span class="sxs-lookup"><span data-stu-id="c070c-128">Also, the **VARIANT** becomes invalid after the method returns, so do not try to reference it later.</span></span>

<span data-ttu-id="c070c-129">Implemente este método para devolver lo más rápido posible.</span><span class="sxs-lookup"><span data-stu-id="c070c-129">Implement this method to return as quickly as possible.</span></span> <span data-ttu-id="c070c-130">No realice llamadas de función desde dentro de este método que podrían bloquear la ejecución del programa.</span><span class="sxs-lookup"><span data-stu-id="c070c-130">Do not make function calls from inside this method that might block program execution.</span></span> <span data-ttu-id="c070c-131">Por ejemplo, no llame a las funciones que envían mensajes de ventana, bloqueos en eventos o que, de lo contrario, podrían bloquear la ejecución.</span><span class="sxs-lookup"><span data-stu-id="c070c-131">For example, do not call functions that send window messages, block on events, or otherwise might block execution.</span></span> <span data-ttu-id="c070c-132">Esto puede hacer que el equipo deje de responder.</span><span class="sxs-lookup"><span data-stu-id="c070c-132">Doing so could cause the computer to stop responding.</span></span>

<span data-ttu-id="c070c-133">Para obtener una lista de los errores definidos por DES, junto con el significado y el tipo de datos de la **variante** a la que apunta *PExtraInfo*, vea [errores de representación](rendering-errors.md).</span><span class="sxs-lookup"><span data-stu-id="c070c-133">For a list of errors defined by DES, along with the meaning and data type of the **VARIANT** pointed to by *pExtraInfo*, see [Rendering Errors](rendering-errors.md).</span></span>

> [!Note]  
> <span data-ttu-id="c070c-134">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="c070c-134">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c070c-135">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c070c-135">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c070c-136">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c070c-136">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c070c-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c070c-137">Requirements</span></span>



| <span data-ttu-id="c070c-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="c070c-138">Requirement</span></span> | <span data-ttu-id="c070c-139">Value</span><span class="sxs-lookup"><span data-stu-id="c070c-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c070c-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c070c-140">Header</span></span><br/>  | <dl> <span data-ttu-id="c070c-141"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="c070c-141"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c070c-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c070c-142">Library</span></span><br/> | <dl> <span data-ttu-id="c070c-143"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c070c-143"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c070c-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="c070c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c070c-145">**Interfaz IAMErrorLog**</span><span class="sxs-lookup"><span data-stu-id="c070c-145">**IAMErrorLog Interface**</span></span>](iamerrorlog.md)
</dt> <dt>

[<span data-ttu-id="c070c-146">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="c070c-146">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




