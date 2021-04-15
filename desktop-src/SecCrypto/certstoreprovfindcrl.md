---
description: Enumera o busca la primera o siguiente CRL en un almacén externo que coincida con los criterios especificados.
ms.assetid: caf218f5-f379-4cb6-bb4b-4767b846d45c
title: Función de devolución de llamada CertStoreProvFindCRL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCRL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: b20b7a4b677356e59be9f2f6df47b260c12d2f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546307"
---
# <a name="certstoreprovfindcrl-callback-function"></a><span data-ttu-id="c6708-103">Función de devolución de llamada CertStoreProvFindCRL</span><span class="sxs-lookup"><span data-stu-id="c6708-103">CertStoreProvFindCRL callback function</span></span>

<span data-ttu-id="c6708-104">La función de devolución de llamada **CertStoreProvFindCRL** enumera o busca la primera o la siguiente [*CRL*](../secgloss/c-gly.md) en un [*almacén*](../secgloss/e-gly.md) externo que coincida con los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="c6708-104">The **CertStoreProvFindCRL** callback function enumerates or finds the first or next [*CRL*](../secgloss/c-gly.md) in an external [*store*](../secgloss/e-gly.md) that matches specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6708-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c6708-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvFindCRL(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCRL_CONTEXT               pPrevCrlContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCRL_CONTEXT               *ppProvCrlContext
);
```



## <a name="parameters"></a><span data-ttu-id="c6708-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c6708-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6708-107">*hStoreProv* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c6708-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6708-108">Identificador de **HCERTSTOREPROV** de un [*almacén de certificados*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="c6708-108">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6708-109">*pFindInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c6708-109">*pFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6708-110">Un puntero a una estructura de [**\_ \_ \_ \_ información del Prov del almacén de certificados**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) que contiene todos los parámetros pasados a la función [**CertFindCRLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore) .</span><span class="sxs-lookup"><span data-stu-id="c6708-110">A pointer to a [**CERT\_STORE\_PROV\_FIND\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) structure containing all the parameters passed to the [**CertFindCRLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore) function.</span></span>

</dd> <dt>

<span data-ttu-id="c6708-111">*pPrevCrlContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c6708-111">*pPrevCrlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6708-112">Puntero a una estructura [**de \_ contexto de CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) de la última CRL encontrada.</span><span class="sxs-lookup"><span data-stu-id="c6708-112">A pointer to a [**CRL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) structure of the last CRL found.</span></span> <span data-ttu-id="c6708-113">En la primera llamada a la función, este parámetro debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="c6708-113">On first call to the function, this parameter should be set to **NULL**.</span></span> <span data-ttu-id="c6708-114">En las llamadas posteriores, debe establecerse en el puntero devuelto en el parámetro *ppProvCRLContext* en la última llamada.</span><span class="sxs-lookup"><span data-stu-id="c6708-114">On subsequent calls, it should be set to the pointer returned in the *ppProvCRLContext* parameter on the last call.</span></span> <span data-ttu-id="c6708-115">La función de devolución de llamada libera un puntero no **nulo** que se pasa en este parámetro.</span><span class="sxs-lookup"><span data-stu-id="c6708-115">A non-**NULL** pointer passed in this parameter is freed by the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="c6708-116">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c6708-116">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6708-117">Los valores de marca necesarios.</span><span class="sxs-lookup"><span data-stu-id="c6708-117">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="c6708-118">*ppvStoreProvFindInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c6708-118">*ppvStoreProvFindInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6708-119">Un puntero a un puntero a un búfer para devolver la información del proveedor de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="c6708-119">A pointer to a pointer to a buffer to return the store provider information.</span></span> <span data-ttu-id="c6708-120">Opcionalmente, la devolución de llamada puede devolver un puntero a información interna de búsqueda en este parámetro.</span><span class="sxs-lookup"><span data-stu-id="c6708-120">Optionally, the callback can return a pointer to internal find information in this parameter.</span></span> <span data-ttu-id="c6708-121">Después de la primera llamada, este parámetro se establece en el puntero devuelto por la llamada anterior a la función.</span><span class="sxs-lookup"><span data-stu-id="c6708-121">After the first call, this parameter is set to the pointer returned by the previous call to the function.</span></span>

</dd> <dt>

<span data-ttu-id="c6708-122">*ppProvCrlContext* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c6708-122">*ppProvCrlContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6708-123">Si la búsqueda se realiza correctamente, se devuelve un puntero a la CRL encontrada en este parámetro.</span><span class="sxs-lookup"><span data-stu-id="c6708-123">On a successful find, a pointer to the CRL found is returned in this parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6708-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c6708-124">Return value</span></span>

<span data-ttu-id="c6708-125">Devuelve **true** si la función se ejecuta correctamente o **false** si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="c6708-125">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6708-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6708-126">Requirements</span></span>



| <span data-ttu-id="c6708-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6708-127">Requirement</span></span> | <span data-ttu-id="c6708-128">Value</span><span class="sxs-lookup"><span data-stu-id="c6708-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c6708-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6708-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c6708-130">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="c6708-130">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="c6708-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6708-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c6708-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c6708-132">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c6708-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6708-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6708-134">**información de la búsqueda de almacén de certificados \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c6708-134">**CERT\_STORE\_PROV\_FIND\_INFO**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[<span data-ttu-id="c6708-135">**CertFindCRLInStore**</span><span class="sxs-lookup"><span data-stu-id="c6708-135">**CertFindCRLInStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore)
</dt> <dt>

[<span data-ttu-id="c6708-136">**contexto de CRL \_**</span><span class="sxs-lookup"><span data-stu-id="c6708-136">**CRL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)
</dt> </dl>

 

 
