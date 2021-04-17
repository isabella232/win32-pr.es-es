---
description: Enumera el nombre de los proveedores de servicios de cifrado (CSP) disponibles.
ms.assetid: d0dc8a8a-afff-4ccc-96e0-2c52913c3322
title: 'ISCrdEnr:: enumCSPName (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCSPName
- SCrdEnr.enumCSPName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: e7bba587b56300cd02efd81758288d3b77c65a66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546683"
---
# <a name="iscrdenrenumcspname-method"></a><span data-ttu-id="44cc6-103">ISCrdEnr:: enumCSPName (método)</span><span class="sxs-lookup"><span data-stu-id="44cc6-103">ISCrdEnr::enumCSPName method</span></span>

<span data-ttu-id="44cc6-104">El método **enumCSPName** enumera el nombre de los proveedores de [*servicios de cifrado*](../secgloss/c-gly.md) (CSP) disponibles.</span><span class="sxs-lookup"><span data-stu-id="44cc6-104">The **enumCSPName** method enumerates the name of the available [*cryptographic service providers*](../secgloss/c-gly.md) (CSPs).</span></span>

## <a name="syntax"></a><span data-ttu-id="44cc6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44cc6-105">Syntax</span></span>


```C++
HRESULT enumCSPName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCSPName
);
```


```VB

SCrdEnr.enumCSPName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByRef pbstrCSPName _
)
```





## <a name="parameters"></a><span data-ttu-id="44cc6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="44cc6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44cc6-107">*dwIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="44cc6-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44cc6-108">Índice de base cero de la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="44cc6-108">The zero-based index for the enumeration sequence.</span></span>

</dd> <dt>

<span data-ttu-id="44cc6-109">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="44cc6-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44cc6-110">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="44cc6-110">Reserved for future use.</span></span> <span data-ttu-id="44cc6-111">Establezca este valor en cero.</span><span class="sxs-lookup"><span data-stu-id="44cc6-111">Set this value to zero.</span></span>

</dd> <dt>

<span data-ttu-id="44cc6-112">*pbstrCSPName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="44cc6-112">*pbstrCSPName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="44cc6-113">Puntero a una cadena que devuelve el nombre del CSP enumerado.</span><span class="sxs-lookup"><span data-stu-id="44cc6-113">A pointer to a string that returns the name of the enumerated CSP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44cc6-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="44cc6-114">Return value</span></span>

### <a name="c"></a><span data-ttu-id="44cc6-115">C++</span><span class="sxs-lookup"><span data-stu-id="44cc6-115">C++</span></span>

<span data-ttu-id="44cc6-116">Si el método se ejecuta correctamente, el método devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="44cc6-116">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="44cc6-117">Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error.</span><span class="sxs-lookup"><span data-stu-id="44cc6-117">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="44cc6-118">Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="44cc6-118">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="44cc6-119">VB</span><span class="sxs-lookup"><span data-stu-id="44cc6-119">VB</span></span>

<span data-ttu-id="44cc6-120">Cadena que representa el nombre del CSP enumerado.</span><span class="sxs-lookup"><span data-stu-id="44cc6-120">A string that represents the name of the enumerated CSP.</span></span>

## <a name="requirements"></a><span data-ttu-id="44cc6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44cc6-121">Requirements</span></span>



| <span data-ttu-id="44cc6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="44cc6-122">Requirement</span></span> | <span data-ttu-id="44cc6-123">Value</span><span class="sxs-lookup"><span data-stu-id="44cc6-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="44cc6-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44cc6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="44cc6-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="44cc6-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="44cc6-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44cc6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="44cc6-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="44cc6-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="44cc6-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="44cc6-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44cc6-129"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44cc6-129"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="44cc6-130">IID</span><span class="sxs-lookup"><span data-stu-id="44cc6-130">IID</span></span><br/>                      | <span data-ttu-id="44cc6-131">IID \_ ISCrdEnr se define como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="44cc6-131">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="44cc6-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="44cc6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44cc6-133">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="44cc6-133">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="44cc6-134">**ISCrdEnr::CSPCount**</span><span class="sxs-lookup"><span data-stu-id="44cc6-134">**ISCrdEnr::CSPCount**</span></span>](iscrdenr-cspcount.md)
</dt> <dt>

[<span data-ttu-id="44cc6-135">**ISCrdEnr::CSPName**</span><span class="sxs-lookup"><span data-stu-id="44cc6-135">**ISCrdEnr::CSPName**</span></span>](iscrdenr-cspname.md)
</dt> </dl>

 

 
