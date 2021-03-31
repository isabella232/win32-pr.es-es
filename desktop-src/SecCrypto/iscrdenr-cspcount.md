---
description: Recupera el número de proveedores de servicios de cifrado (CSP).
ms.assetid: 7e0c1613-85ad-4f25-837e-d7b0f11e654a
title: 'ISCrdEnr:: CSPCount (propiedad)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.CSPCount
- ISCrdEnr.get_CSPCount
- SCrdEnr.CSPCount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: b2aea22db3c804ae4808996002b68efdcb6cf9a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361302"
---
# <a name="iscrdenrcspcount-property"></a><span data-ttu-id="7db6e-103">ISCrdEnr:: CSPCount (propiedad)</span><span class="sxs-lookup"><span data-stu-id="7db6e-103">ISCrdEnr::CSPCount property</span></span>

<span data-ttu-id="7db6e-104">La propiedad **CSPCount** recupera el número de [*proveedores de servicios de cifrado*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="7db6e-104">The **CSPCount** property retrieves the number of [*cryptographic service providers*](../secgloss/c-gly.md) (CSPs).</span></span>

<span data-ttu-id="7db6e-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7db6e-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7db6e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7db6e-106">Syntax</span></span>


```C++
HRESULT get_CSPCount(
   LONG *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="7db6e-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="7db6e-107">Property value</span></span>

<span data-ttu-id="7db6e-108">Número de CSP.</span><span class="sxs-lookup"><span data-stu-id="7db6e-108">The number of CSPs.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7db6e-109">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="7db6e-109">Error codes</span></span>

<span data-ttu-id="7db6e-110">Si el método se ejecuta correctamente, el método devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="7db6e-110">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="7db6e-111">Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error.</span><span class="sxs-lookup"><span data-stu-id="7db6e-111">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="7db6e-112">Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="7db6e-112">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7db6e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7db6e-113">Requirements</span></span>



| <span data-ttu-id="7db6e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7db6e-114">Requirement</span></span> | <span data-ttu-id="7db6e-115">Value</span><span class="sxs-lookup"><span data-stu-id="7db6e-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7db6e-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7db6e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7db6e-117">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7db6e-117">None supported</span></span><br/>                                                               |
| <span data-ttu-id="7db6e-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7db6e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7db6e-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7db6e-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7db6e-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7db6e-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7db6e-121"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7db6e-121"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="7db6e-122">IID</span><span class="sxs-lookup"><span data-stu-id="7db6e-122">IID</span></span><br/>                      | <span data-ttu-id="7db6e-123">IID \_ ISCrdEnr se define como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="7db6e-123">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="7db6e-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="7db6e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7db6e-125">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="7db6e-125">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="7db6e-126">**ISCrdEnr::CSPName**</span><span class="sxs-lookup"><span data-stu-id="7db6e-126">**ISCrdEnr::CSPName**</span></span>](iscrdenr-cspname.md)
</dt> <dt>

[<span data-ttu-id="7db6e-127">**ISCrdEnr::enumCSPName**</span><span class="sxs-lookup"><span data-stu-id="7db6e-127">**ISCrdEnr::enumCSPName**</span></span>](iscrdenr-enumcspname.md)
</dt> </dl>

 

 
