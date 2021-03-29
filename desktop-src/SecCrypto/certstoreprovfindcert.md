---
description: Enumera o busca el primer certificado o el siguiente en un almacén externo que coincida con los criterios especificados.
ms.assetid: 1129a372-4d7c-454e-969b-26a1d6037bc0
title: Función de devolución de llamada CertStoreProvFindCert
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCert
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 09701991d6b192d27f921642bfc960df819f9140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361014"
---
# <a name="certstoreprovfindcert-callback-function"></a><span data-ttu-id="70ed5-103">Función de devolución de llamada CertStoreProvFindCert</span><span class="sxs-lookup"><span data-stu-id="70ed5-103">CertStoreProvFindCert callback function</span></span>

<span data-ttu-id="70ed5-104">La función de devolución de llamada **CertStoreProvFindCert** enumera o busca el primer certificado o el siguiente en un [*almacén externo*](../secgloss/e-gly.md) que coincida con los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="70ed5-104">The **CertStoreProvFindCert** callback function enumerates or finds the first or next certificate in an [*external store*](../secgloss/e-gly.md) that matches specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="70ed5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="70ed5-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvFindCert(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCERT_CONTEXT              pPrevCertContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCERT_CONTEXT              *ppProvCertContext
);
```



## <a name="parameters"></a><span data-ttu-id="70ed5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="70ed5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70ed5-107">*hStoreProv* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="70ed5-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70ed5-108">Identificador de **HCERTSTOREPROV** de un [*almacén de certificados*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="70ed5-108">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="70ed5-109">*pFindInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="70ed5-109">*pFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70ed5-110">Un puntero a una estructura de [**\_ \_ \_ \_ información del Prov del almacén de certificados**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) que contiene todos los parámetros pasados a la función [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) .</span><span class="sxs-lookup"><span data-stu-id="70ed5-110">A pointer to a [**CERT\_STORE\_PROV\_FIND\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) structure containing all the parameters passed to the [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) function.</span></span>

</dd> <dt>

<span data-ttu-id="70ed5-111">*pPrevCertContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="70ed5-111">*pPrevCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70ed5-112">Un puntero a un [**\_ contexto**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) de certificado del certificado encontrado.</span><span class="sxs-lookup"><span data-stu-id="70ed5-112">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) of the certificate found.</span></span> <span data-ttu-id="70ed5-113">En la primera llamada a la función, este parámetro debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="70ed5-113">On first call to the function, this parameter should be set to **NULL**.</span></span> <span data-ttu-id="70ed5-114">En las llamadas posteriores, debe establecerse en el puntero devuelto en el parámetro *ppProvCertContext* en la última llamada.</span><span class="sxs-lookup"><span data-stu-id="70ed5-114">On subsequent calls, it should be set to the pointer returned in the *ppProvCertContext* parameter on the last call.</span></span> <span data-ttu-id="70ed5-115">La función de devolución de llamada libera un puntero no **nulo** que se pasa en este parámetro.</span><span class="sxs-lookup"><span data-stu-id="70ed5-115">A non-**NULL** pointer passed in this parameter is freed by the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="70ed5-116">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="70ed5-116">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70ed5-117">Los valores de marca necesarios.</span><span class="sxs-lookup"><span data-stu-id="70ed5-117">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="70ed5-118">*ppvStoreProvFindInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="70ed5-118">*ppvStoreProvFindInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="70ed5-119">Un puntero a un puntero a un búfer para devolver la información del proveedor de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="70ed5-119">A pointer to a pointer to a buffer to return the store provider information.</span></span> <span data-ttu-id="70ed5-120">Opcionalmente, la devolución de llamada puede devolver un puntero a información interna de búsqueda en este parámetro.</span><span class="sxs-lookup"><span data-stu-id="70ed5-120">Optionally, the callback can return a pointer to internal find information in this parameter.</span></span> <span data-ttu-id="70ed5-121">Después de la primera llamada, este parámetro se establece en el puntero devuelto por la llamada anterior a la función.</span><span class="sxs-lookup"><span data-stu-id="70ed5-121">After the first call, this parameter is set to the pointer returned by the previous call to the function.</span></span>

</dd> <dt>

<span data-ttu-id="70ed5-122">*ppProvCertContext* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="70ed5-122">*ppProvCertContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="70ed5-123">Si la búsqueda se realiza correctamente, se devuelve un puntero al certificado encontrado en este parámetro.</span><span class="sxs-lookup"><span data-stu-id="70ed5-123">On a successful find, a pointer to the certificate found is returned in this parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70ed5-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="70ed5-124">Return value</span></span>

<span data-ttu-id="70ed5-125">Devuelve **true** si la función se ejecuta correctamente o **false** si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="70ed5-125">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="70ed5-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70ed5-126">Requirements</span></span>



| <span data-ttu-id="70ed5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="70ed5-127">Requirement</span></span> | <span data-ttu-id="70ed5-128">Value</span><span class="sxs-lookup"><span data-stu-id="70ed5-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="70ed5-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70ed5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="70ed5-130">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="70ed5-130">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="70ed5-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70ed5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="70ed5-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="70ed5-132">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="70ed5-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="70ed5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70ed5-134">**contexto de certificado \_**</span><span class="sxs-lookup"><span data-stu-id="70ed5-134">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[<span data-ttu-id="70ed5-135">**información de la búsqueda de almacén de certificados \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="70ed5-135">**CERT\_STORE\_PROV\_FIND\_INFO**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[<span data-ttu-id="70ed5-136">**CertFindCertificateInStore**</span><span class="sxs-lookup"><span data-stu-id="70ed5-136">**CertFindCertificateInStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)
</dt> </dl>

 

 
