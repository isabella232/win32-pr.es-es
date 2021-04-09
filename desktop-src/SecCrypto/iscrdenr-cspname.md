---
description: Establece o recupera el nombre del proveedor de servicios criptográficos (CSP).
ms.assetid: 34fde7b0-747d-4592-a89a-207f82369f52
title: 'ISCrdEnr:: CSPName (propiedad)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.CSPName
- ISCrdEnr.get_CSPName
- ISCrdEnr.put_CSPName
- SCrdEnr.CSPName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 363f2f9120d3b0a202335d0e8e450464cbc1f118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083300"
---
# <a name="iscrdenrcspname-property"></a><span data-ttu-id="ff00b-103">ISCrdEnr:: CSPName (propiedad)</span><span class="sxs-lookup"><span data-stu-id="ff00b-103">ISCrdEnr::CSPName property</span></span>

<span data-ttu-id="ff00b-104">La propiedad **CSPName** establece o recupera el nombre del proveedor de [*servicios criptográficos*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="ff00b-104">The **CSPName** property sets or retrieves the name of the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

<span data-ttu-id="ff00b-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="ff00b-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff00b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ff00b-106">Syntax</span></span>


```C++
HRESULT put_CSPName(
   BSTR newVal
);

HRESULT get_CSPName(
   BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="ff00b-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ff00b-107">Property value</span></span>

<span data-ttu-id="ff00b-108">Nombre del CSP.</span><span class="sxs-lookup"><span data-stu-id="ff00b-108">The name of the CSP.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ff00b-109">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="ff00b-109">Error codes</span></span>

<span data-ttu-id="ff00b-110">Si el método se ejecuta correctamente, el método devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="ff00b-110">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="ff00b-111">Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error.</span><span class="sxs-lookup"><span data-stu-id="ff00b-111">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="ff00b-112">Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="ff00b-112">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ff00b-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ff00b-113">Remarks</span></span>

<span data-ttu-id="ff00b-114">Establezca esta propiedad para especificar el nombre del CSP que se va a usar con el control de inscripción de tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="ff00b-114">Set this property to specify the name of the CSP to use with the Smart Card Enrollment Control.</span></span> <span data-ttu-id="ff00b-115">Obtenga esta propiedad para recuperar el nombre del CSP especificado.</span><span class="sxs-lookup"><span data-stu-id="ff00b-115">Get this property to retrieve the name of the specified CSP.</span></span> <span data-ttu-id="ff00b-116">Si no especifica un valor para esta propiedad, la propiedad **CSPName** tiene como valor predeterminado el nombre de la lista de CSP disponible.</span><span class="sxs-lookup"><span data-stu-id="ff00b-116">If you do not specify a value for this property, the **CSPName** property defaults to the first name in the available list of CSPs.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff00b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff00b-117">Requirements</span></span>



| <span data-ttu-id="ff00b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff00b-118">Requirement</span></span> | <span data-ttu-id="ff00b-119">Value</span><span class="sxs-lookup"><span data-stu-id="ff00b-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff00b-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff00b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ff00b-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ff00b-121">None supported</span></span><br/>                                                               |
| <span data-ttu-id="ff00b-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff00b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ff00b-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ff00b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ff00b-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ff00b-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff00b-125"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff00b-125"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="ff00b-126">IID</span><span class="sxs-lookup"><span data-stu-id="ff00b-126">IID</span></span><br/>                      | <span data-ttu-id="ff00b-127">IID \_ ISCrdEnr se define como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="ff00b-127">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="ff00b-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff00b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff00b-129">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="ff00b-129">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="ff00b-130">**ISCrdEnr::CSPCount**</span><span class="sxs-lookup"><span data-stu-id="ff00b-130">**ISCrdEnr::CSPCount**</span></span>](iscrdenr-cspcount.md)
</dt> <dt>

[<span data-ttu-id="ff00b-131">**ISCrdEnr::enumCSPName**</span><span class="sxs-lookup"><span data-stu-id="ff00b-131">**ISCrdEnr::enumCSPName**</span></span>](iscrdenr-enumcspname.md)
</dt> </dl>

 

 
