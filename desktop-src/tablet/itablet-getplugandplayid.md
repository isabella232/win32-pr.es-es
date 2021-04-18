---
description: Devuelve una cadena que contiene el identificador de Plug and Play del dispositivo de tableta gráfica.
ms.assetid: a0b6619b-f80c-470b-aa3f-f0b30a9dbda8
title: 'ITablet:: GetPlugAndPlayId (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetPlugAndPlayId
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 3fb6ce7d59cb29aac4b06b7245bc6246b0688a7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720586"
---
# <a name="itabletgetplugandplayid-method"></a><span data-ttu-id="a94fd-103">ITablet:: GetPlugAndPlayId (método)</span><span class="sxs-lookup"><span data-stu-id="a94fd-103">ITablet::GetPlugAndPlayId method</span></span>

<span data-ttu-id="a94fd-104">Devuelve una cadena que contiene el identificador de Plug and Play del dispositivo de tableta gráfica.</span><span class="sxs-lookup"><span data-stu-id="a94fd-104">Returns a string containing the Plug and Play ID for the tablet device.</span></span>

## <a name="syntax"></a><span data-ttu-id="a94fd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a94fd-105">Syntax</span></span>


```C++
HRESULT GetPlugAndPlayId(
  [out] LPWSTR *ppwszPPId
);
```



## <a name="parameters"></a><span data-ttu-id="a94fd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a94fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a94fd-107">*ppwszPPId* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a94fd-107">*ppwszPPId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a94fd-108">Puntero a una cadena que contiene el identificador de Plug and Play del dispositivo de tableta gráfica.</span><span class="sxs-lookup"><span data-stu-id="a94fd-108">Pointer to a string containing the Plug and Play ID for the tablet device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a94fd-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a94fd-109">Return value</span></span>

<span data-ttu-id="a94fd-110">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="a94fd-110">This method can return one of these values.</span></span>



| <span data-ttu-id="a94fd-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a94fd-111">Return code</span></span>                                                                            | <span data-ttu-id="a94fd-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="a94fd-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="a94fd-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="a94fd-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="a94fd-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="a94fd-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="a94fd-115"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="a94fd-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="a94fd-116">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="a94fd-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a94fd-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a94fd-117">Remarks</span></span>

<span data-ttu-id="a94fd-118">Es responsabilidad del llamador liberar la memoria devuelta desde este método mediante [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="a94fd-118">It is the caller's responsibility to free the memory returned from this method by using [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="a94fd-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a94fd-119">Requirements</span></span>



| <span data-ttu-id="a94fd-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a94fd-120">Requirement</span></span> | <span data-ttu-id="a94fd-121">Value</span><span class="sxs-lookup"><span data-stu-id="a94fd-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a94fd-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a94fd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a94fd-123">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a94fd-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a94fd-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a94fd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a94fd-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a94fd-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a94fd-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a94fd-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="a94fd-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a94fd-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a94fd-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="a94fd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a94fd-129">**Interfaz ITablet**</span><span class="sxs-lookup"><span data-stu-id="a94fd-129">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

