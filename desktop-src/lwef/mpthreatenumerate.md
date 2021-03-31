---
title: Función MpThreatEnumerate (MpClient. h)
description: Devuelve información sobre la siguiente amenaza en la lista de enumeración. Se puede llamar a esta función varias veces hasta que se complete la enumeración de todas las amenazas.
ms.assetid: 33244F4F-4FB7-4FA7-BC56-B9A30ABC3644
keywords:
- Función MpThreatEnumerate características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MpThreatEnumerate
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acdbb7971371015a401c1a951ace8c55869fd405
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996759"
---
# <a name="mpthreatenumerate-function"></a><span data-ttu-id="63477-105">MpThreatEnumerate función)</span><span class="sxs-lookup"><span data-stu-id="63477-105">MpThreatEnumerate function</span></span>

<span data-ttu-id="63477-106">Devuelve información sobre la siguiente amenaza en la lista de enumeración.</span><span class="sxs-lookup"><span data-stu-id="63477-106">Returns information about the next threat in the enumeration list.</span></span> <span data-ttu-id="63477-107">Se puede llamar a esta función varias veces hasta que se complete la enumeración de todas las amenazas.</span><span class="sxs-lookup"><span data-stu-id="63477-107">This function can be called repeatedly until the enumeration of all the threats is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="63477-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63477-108">Syntax</span></span>


```C++
HRESULT WINAPI MpThreatEnumerate(
  _In_  MPHANDLE       hThreatEnumHandle,
  _Out_ PMPTHREAT_INFO *ppThreatInfo
);
```



## <a name="parameters"></a><span data-ttu-id="63477-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63477-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63477-110">*hThreatEnumHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="63477-110">*hThreatEnumHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63477-111">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="63477-111">Type: **MPHANDLE**</span></span>

<span data-ttu-id="63477-112">Identificador de un contexto de enumeración de amenazas devuelto por [**MpThreatOpen**](mpthreatopen.md).</span><span class="sxs-lookup"><span data-stu-id="63477-112">Handle to a threat enumeration context returned by [**MpThreatOpen**](mpthreatopen.md).</span></span>

</dd> <dt>

<span data-ttu-id="63477-113">*ppThreatInfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="63477-113">*ppThreatInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63477-114">Tipo: \**PMPTHREAT \_ info \** _</span><span class="sxs-lookup"><span data-stu-id="63477-114">Type: \**PMPTHREAT\_INFO\** _</span></span>

<span data-ttu-id="63477-115">Devuelve un puntero a una estructura de información de amenazas, [_ *MPTHREAT \_ info* \*](mpthreat-info.md).</span><span class="sxs-lookup"><span data-stu-id="63477-115">Returns a pointer to a threat information structure, [_ *MPTHREAT\_INFO*\*](mpthreat-info.md).</span></span> <span data-ttu-id="63477-116">La estructura contiene información como el identificador, el nombre y la gravedad de la amenaza.</span><span class="sxs-lookup"><span data-stu-id="63477-116">The structure contains information such as threat id, name, and severity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63477-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="63477-117">Return value</span></span>

<span data-ttu-id="63477-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="63477-118">Type: **HRESULT**</span></span>

<span data-ttu-id="63477-119">Si la función se ejecuta correctamente, el valor devuelto es **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="63477-119">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="63477-120">Si no hay más elementos para devolver, el valor devuelto es **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="63477-120">If there are no more items to return the return value is **S\_FALSE**.</span></span>

<span data-ttu-id="63477-121">Si se produce un error en la función, el valor devuelto es un código **HRESULT** erróneo.</span><span class="sxs-lookup"><span data-stu-id="63477-121">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="63477-122">El autor de la llamada puede usar la función [**MpErrorMessageFormat**](mperrormessageformat.md) para obtener una descripción genérica del mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="63477-122">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="63477-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63477-123">Requirements</span></span>



| <span data-ttu-id="63477-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="63477-124">Requirement</span></span> | <span data-ttu-id="63477-125">Value</span><span class="sxs-lookup"><span data-stu-id="63477-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63477-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63477-126">Minimum supported client</span></span><br/> | <span data-ttu-id="63477-127">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="63477-127">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="63477-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63477-128">Minimum supported server</span></span><br/> | <span data-ttu-id="63477-129">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="63477-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="63477-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63477-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="63477-131"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="63477-131"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="63477-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="63477-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63477-133"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63477-133"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63477-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="63477-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63477-135">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="63477-135">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="63477-136">**MpThreatOpen**</span><span class="sxs-lookup"><span data-stu-id="63477-136">**MpThreatOpen**</span></span>](mpthreatopen.md)
</dt> <dt>

[<span data-ttu-id="63477-137">**información de MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="63477-137">**MPTHREAT\_INFO**</span></span>](mpthreat-info.md)
</dt> </dl>

 

 





