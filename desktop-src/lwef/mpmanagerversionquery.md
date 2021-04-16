---
title: Función MpManagerVersionQuery (MpClient. h)
description: Devuelve información de versión sobre varios componentes del administrador de protección contra malware de.
ms.assetid: 47DE12BF-D7A4-468B-B0E7-79B5C27E56F5
keywords:
- Función MpManagerVersionQuery características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MpManagerVersionQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a841a83d8ceb828de0a5a9cd80f5f5bdc7f5c914
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686094"
---
# <a name="mpmanagerversionquery-function"></a><span data-ttu-id="bd2f6-104">MpManagerVersionQuery función)</span><span class="sxs-lookup"><span data-stu-id="bd2f6-104">MpManagerVersionQuery function</span></span>

<span data-ttu-id="bd2f6-105">Devuelve información de versión sobre varios componentes del administrador de protección contra malware de.</span><span class="sxs-lookup"><span data-stu-id="bd2f6-105">Returns version information about various components of the malware protection manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd2f6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bd2f6-106">Syntax</span></span>


```C++
HRESULT WINAPI MpManagerVersionQuery(
  _In_  MPHANDLE        hMpHandle,
  _Out_ PMPVERSION_INFO pVersionInfo
);
```



## <a name="parameters"></a><span data-ttu-id="bd2f6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bd2f6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd2f6-108">*hMpHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bd2f6-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd2f6-109">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="bd2f6-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="bd2f6-110">Identificador de la interfaz del administrador de protección contra malware.</span><span class="sxs-lookup"><span data-stu-id="bd2f6-110">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="bd2f6-111">La función [**MpManagerOpen**](mpmanageropen.md) devuelve este identificador.</span><span class="sxs-lookup"><span data-stu-id="bd2f6-111">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="bd2f6-112">*pVersionInfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bd2f6-112">*pVersionInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd2f6-113">Tipo: **PMPVERSION \_ info**</span><span class="sxs-lookup"><span data-stu-id="bd2f6-113">Type: **PMPVERSION\_INFO**</span></span>

<span data-ttu-id="bd2f6-114">Puntero a una estructura que contiene información de versión sobre varios componentes del administrador de protección contra malware de.</span><span class="sxs-lookup"><span data-stu-id="bd2f6-114">Pointer to a structure that contains version information about various components of the malware protection manager.</span></span> <span data-ttu-id="bd2f6-115">Vea [**\_ información de MPVERSION**](mpversion-info.md).</span><span class="sxs-lookup"><span data-stu-id="bd2f6-115">See [**MPVERSION\_INFO**](mpversion-info.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd2f6-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bd2f6-116">Return value</span></span>

<span data-ttu-id="bd2f6-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bd2f6-117">Type: **HRESULT**</span></span>

<span data-ttu-id="bd2f6-118">Si la función se ejecuta correctamente, el valor devuelto es **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bd2f6-118">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="bd2f6-119">Si se produce un error en la función, el valor devuelto es un código **HRESULT** erróneo.</span><span class="sxs-lookup"><span data-stu-id="bd2f6-119">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="bd2f6-120">El autor de la llamada puede usar la función [**MpErrorMessageFormat**](mperrormessageformat.md) para obtener una descripción genérica del mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="bd2f6-120">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd2f6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd2f6-121">Requirements</span></span>



| <span data-ttu-id="bd2f6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd2f6-122">Requirement</span></span> | <span data-ttu-id="bd2f6-123">Value</span><span class="sxs-lookup"><span data-stu-id="bd2f6-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd2f6-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd2f6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bd2f6-125">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="bd2f6-125">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="bd2f6-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd2f6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bd2f6-127">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="bd2f6-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bd2f6-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bd2f6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd2f6-129"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd2f6-129"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="bd2f6-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bd2f6-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd2f6-131"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd2f6-131"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd2f6-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd2f6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd2f6-133">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="bd2f6-133">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="bd2f6-134">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="bd2f6-134">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="bd2f6-135">**información de MPVERSION \_**</span><span class="sxs-lookup"><span data-stu-id="bd2f6-135">**MPVERSION\_INFO**</span></span>](mpversion-info.md)
</dt> </dl>

 

 





