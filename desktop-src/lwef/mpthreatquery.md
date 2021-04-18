---
title: Función MpThreatQuery (MpClient. h)
description: Se usa para consultar información estática (como gravedad y categoría) o localizada (como descripción de la categoría y consejos) sobre una amenaza determinada.
ms.assetid: A06854B2-8444-46A4-A53F-FD5FEAFF47B7
keywords:
- Función MpThreatQuery características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MpThreatQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21d38a3734f9d98f3bd61143d4fe58bd606c7508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665963"
---
# <a name="mpthreatquery-function"></a><span data-ttu-id="2f29c-104">MpThreatQuery función)</span><span class="sxs-lookup"><span data-stu-id="2f29c-104">MpThreatQuery function</span></span>

<span data-ttu-id="2f29c-105">Se usa para consultar información estática (como gravedad y categoría) o localizada (como descripción de la categoría y consejos) sobre una amenaza determinada.</span><span class="sxs-lookup"><span data-stu-id="2f29c-105">Used to query static (such as severity and category) or localized (such as category description and advice) information about a particular threat.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f29c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f29c-106">Syntax</span></span>


```C++
HRESULT WINAPI MpThreatQuery(
  _In_      MPHANDLE                 hMpHandle,
  _In_      MPTHREAT_ID              ThreatID,
  _Out_     PMPTHREAT_INFO           *ppThreatInfo,
  _Out_opt_ PMPTHREAT_LOCALIZED_INFO *ppThreatLocalizedInfo
);
```



## <a name="parameters"></a><span data-ttu-id="2f29c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f29c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f29c-108">*hMpHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2f29c-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f29c-109">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="2f29c-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="2f29c-110">Identificador de la interfaz del administrador de protección contra malware.</span><span class="sxs-lookup"><span data-stu-id="2f29c-110">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="2f29c-111">La función [**MpManagerOpen**](mpmanageropen.md) devuelve este identificador.</span><span class="sxs-lookup"><span data-stu-id="2f29c-111">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="2f29c-112">*ThreatID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2f29c-112">*ThreatID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f29c-113">Tipo: **\_ ID. de MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="2f29c-113">Type: **MPTHREAT\_ID**</span></span>

<span data-ttu-id="2f29c-114">Identificador de amenaza para el que se solicita información.</span><span class="sxs-lookup"><span data-stu-id="2f29c-114">Threat identifier for which information is requested.</span></span>

</dd> <dt>

<span data-ttu-id="2f29c-115">*ppThreatInfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2f29c-115">*ppThreatInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f29c-116">Tipo: \**PMPTHREAT \_ info \** _</span><span class="sxs-lookup"><span data-stu-id="2f29c-116">Type: \**PMPTHREAT\_INFO\** _</span></span>

<span data-ttu-id="2f29c-117">Devuelve un puntero a una estructura de información de amenazas, [_ *MPTHREAT \_ info* \*](mpthreat-info.md).</span><span class="sxs-lookup"><span data-stu-id="2f29c-117">Returns a pointer to a threat information structure, [_ *MPTHREAT\_INFO*\*](mpthreat-info.md).</span></span> <span data-ttu-id="2f29c-118">La estructura contiene información como el identificador, el nombre y la gravedad de la amenaza.</span><span class="sxs-lookup"><span data-stu-id="2f29c-118">The structure contains information such as threat id, name, and severity.</span></span>

</dd> <dt>

<span data-ttu-id="2f29c-119">*ppThreatLocalizedInfo* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="2f29c-119">*ppThreatLocalizedInfo* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2f29c-120">Tipo: \**PMPTHREAT \_ \_ información \* localizada* _</span><span class="sxs-lookup"><span data-stu-id="2f29c-120">Type: \**PMPTHREAT\_LOCALIZED\_INFO\** _</span></span>

<span data-ttu-id="2f29c-121">Devuelve un puntero a una estructura que contiene información localizada sobre la amenaza.</span><span class="sxs-lookup"><span data-stu-id="2f29c-121">Returns a pointer to a structure containing localized information about the threat.</span></span> <span data-ttu-id="2f29c-122">Puede pasar _ *null*\* si no está interesado en información localizada sobre la amenaza.</span><span class="sxs-lookup"><span data-stu-id="2f29c-122">You can pass _ *NULL*\* if you are not interested in localized information about the threat.</span></span> <span data-ttu-id="2f29c-123">Consulte [**\_ \_ información localizada de MPTHREAT**](mpthreat-localized-info.md).</span><span class="sxs-lookup"><span data-stu-id="2f29c-123">See [**MPTHREAT\_LOCALIZED\_INFO**](mpthreat-localized-info.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f29c-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f29c-124">Return value</span></span>

<span data-ttu-id="2f29c-125">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2f29c-125">Type: **HRESULT**</span></span>

<span data-ttu-id="2f29c-126">Si la función se ejecuta correctamente, el valor devuelto es **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2f29c-126">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="2f29c-127">Si se produce un error en la función, el valor devuelto es un código **HRESULT** erróneo.</span><span class="sxs-lookup"><span data-stu-id="2f29c-127">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="2f29c-128">El autor de la llamada puede usar la función [**MpErrorMessageFormat**](mperrormessageformat.md) para obtener una descripción genérica del mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="2f29c-128">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f29c-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f29c-129">Requirements</span></span>



| <span data-ttu-id="2f29c-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f29c-130">Requirement</span></span> | <span data-ttu-id="2f29c-131">Value</span><span class="sxs-lookup"><span data-stu-id="2f29c-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f29c-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f29c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2f29c-133">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="2f29c-133">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="2f29c-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f29c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2f29c-135">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="2f29c-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2f29c-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f29c-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f29c-137"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f29c-137"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="2f29c-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2f29c-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f29c-139"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f29c-139"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f29c-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f29c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f29c-141">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="2f29c-141">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="2f29c-142">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="2f29c-142">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="2f29c-143">**información de MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="2f29c-143">**MPTHREAT\_INFO**</span></span>](mpthreat-info.md)
</dt> <dt>

[<span data-ttu-id="2f29c-144">**\_información localizada de MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="2f29c-144">**MPTHREAT\_LOCALIZED\_INFO**</span></span>](mpthreat-localized-info.md)
</dt> </dl>

 

 





