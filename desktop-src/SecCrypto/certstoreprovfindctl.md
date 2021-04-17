---
description: Enumera o busca la primera o siguiente CTL en un almacén externo que coincida con los criterios especificados.
ms.assetid: 0b465e6e-fb5c-4621-a968-c2cdcab0ea15
title: Función de devolución de llamada CertStoreProvFindCTL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 9454f918c9cbc5b6f90642d46fbb33573b70457f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668103"
---
# <a name="certstoreprovfindctl-callback-function"></a><span data-ttu-id="7761d-103">Función de devolución de llamada CertStoreProvFindCTL</span><span class="sxs-lookup"><span data-stu-id="7761d-103">CertStoreProvFindCTL callback function</span></span>

<span data-ttu-id="7761d-104">La función de devolución de llamada **CertStoreProvFindCTL** enumera o encuentra la primera o siguiente [*CTL*](../secgloss/c-gly.md) en un [*almacén externo*](../secgloss/e-gly.md) que coincide con los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="7761d-104">The **CertStoreProvFindCTL** callback function enumerates or finds the first or next [*CTL*](../secgloss/c-gly.md) in an [*external store*](../secgloss/e-gly.md) that matches specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="7761d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7761d-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvFindCTL(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCTL_CONTEXT               pPrevCtlContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCTL_CONTEXT               *ppProvCtlContext
);
```



## <a name="parameters"></a><span data-ttu-id="7761d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7761d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7761d-107">*hStoreProv* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7761d-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7761d-108">Identificador de **HCERTSTOREPROV** de un [*almacén de certificados*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="7761d-108">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="7761d-109">*pFindInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7761d-109">*pFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7761d-110">Un puntero a una estructura de [**\_ \_ \_ \_ información de Prov del almacén de certificados**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) que contiene todos los parámetros pasados a [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).</span><span class="sxs-lookup"><span data-stu-id="7761d-110">A pointer to a [**CERT\_STORE\_PROV\_FIND\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) structure containing all the parameters passed to the [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).</span></span> <span data-ttu-id="7761d-111">.</span><span class="sxs-lookup"><span data-stu-id="7761d-111">function.</span></span>

</dd> <dt>

<span data-ttu-id="7761d-112">*pPrevCtlContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7761d-112">*pPrevCtlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7761d-113">Puntero a una estructura [**de \_ contexto de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) de la última CTL encontrada.</span><span class="sxs-lookup"><span data-stu-id="7761d-113">A pointer to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) structure of the last CTL found.</span></span> <span data-ttu-id="7761d-114">En la primera llamada a la función, este parámetro debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="7761d-114">On first call to the function, this parameter should be set to **NULL**.</span></span> <span data-ttu-id="7761d-115">En las llamadas posteriores, debe establecerse en el puntero devuelto en el parámetro *ppProvCTLContext* en la última llamada.</span><span class="sxs-lookup"><span data-stu-id="7761d-115">On subsequent calls, it should be set to the pointer returned in the *ppProvCTLContext* parameter on the last call.</span></span> <span data-ttu-id="7761d-116">La función de devolución de llamada libera un puntero no **nulo** que se pasa en este parámetro.</span><span class="sxs-lookup"><span data-stu-id="7761d-116">A non-**NULL** pointer passed in this parameter is freed by the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="7761d-117">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7761d-117">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7761d-118">Los valores de marca necesarios.</span><span class="sxs-lookup"><span data-stu-id="7761d-118">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="7761d-119">*ppvStoreProvFindInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7761d-119">*ppvStoreProvFindInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7761d-120">Un puntero a un puntero a un búfer para devolver la información del proveedor de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="7761d-120">A pointer to a pointer to buffer to return the store provider information.</span></span> <span data-ttu-id="7761d-121">Opcionalmente, la devolución de llamada puede devolver un puntero a información interna de búsqueda en este parámetro.</span><span class="sxs-lookup"><span data-stu-id="7761d-121">Optionally, the callback can return a pointer to internal find information in this parameter.</span></span> <span data-ttu-id="7761d-122">Después de la primera llamada, este parámetro se establece en el puntero devuelto por la llamada anterior a la función.</span><span class="sxs-lookup"><span data-stu-id="7761d-122">After the first call, this parameter is set to the pointer returned by the previous call to the function.</span></span>

</dd> <dt>

<span data-ttu-id="7761d-123">*ppProvCtlContext* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7761d-123">*ppProvCtlContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7761d-124">Si la búsqueda se realiza correctamente, se devuelve un puntero a la CTL encontrada en este parámetro.</span><span class="sxs-lookup"><span data-stu-id="7761d-124">On a successful find, a pointer to the CTL found is returned in this parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7761d-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7761d-125">Return value</span></span>

<span data-ttu-id="7761d-126">Devuelve **true** si la función se ejecuta correctamente o **false** si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="7761d-126">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="7761d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7761d-127">Requirements</span></span>



| <span data-ttu-id="7761d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="7761d-128">Requirement</span></span> | <span data-ttu-id="7761d-129">Value</span><span class="sxs-lookup"><span data-stu-id="7761d-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7761d-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7761d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7761d-131">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="7761d-131">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="7761d-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7761d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7761d-133">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7761d-133">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7761d-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="7761d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7761d-135">**información de la búsqueda de almacén de certificados \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7761d-135">**CERT\_STORE\_PROV\_FIND\_INFO**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[<span data-ttu-id="7761d-136">**CertFindCTLInStore**</span><span class="sxs-lookup"><span data-stu-id="7761d-136">**CertFindCTLInStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore)
</dt> <dt>

[<span data-ttu-id="7761d-137">**\_contexto CTL**</span><span class="sxs-lookup"><span data-stu-id="7761d-137">**CTL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
