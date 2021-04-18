---
description: Se llama cuando no se usó el certificado devuelto por la devolución de llamada CertStoreProvFindCert y, por tanto, se libera, en una llamada subsiguiente a CertStoreProvFindCert.
ms.assetid: be882b56-027c-4540-9426-27d3c2b262e9
title: Función de devolución de llamada CertStoreProvFreeFindCert
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCert
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 320145ebfe95d1e678193ea1b11e7cb0d5294c69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668102"
---
# <a name="certstoreprovfreefindcert-callback-function"></a><span data-ttu-id="7d922-103">Función de devolución de llamada CertStoreProvFreeFindCert</span><span class="sxs-lookup"><span data-stu-id="7d922-103">CertStoreProvFreeFindCert callback function</span></span>

<span data-ttu-id="7d922-104">Se llama a la función de devolución de llamada **CertStoreProvFreeFindCert** cuando no se usó el certificado devuelto por la devolución de llamada [**CertStoreProvFindCert**](certstoreprovfindcert.md) y, por tanto, se libera, en una llamada subsiguiente a **CertStoreProvFindCert**.</span><span class="sxs-lookup"><span data-stu-id="7d922-104">The **CertStoreProvFreeFindCert** callback function is called when the certificate returned by the [**CertStoreProvFindCert**](certstoreprovfindcert.md) callback was not used, and thus released, in a subsequent call to **CertStoreProvFindCert**.</span></span> <span data-ttu-id="7d922-105">Antes de que se llame a la devolución de llamada de cierre, el proveedor debe liberar todos los certificados devueltos por la devolución de llamada de [**CertStoreProvFindCert**](certstoreprovfindcert.md) mediante **CertStoreProvFindCert** o **CertStoreProvFreeFindCert**.</span><span class="sxs-lookup"><span data-stu-id="7d922-105">Before the CLOSE callback is called, all certificates returned by the [**CertStoreProvFindCert**](certstoreprovfindcert.md) callback must be released by the provider using **CertStoreProvFindCert** or **CertStoreProvFreeFindCert**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d922-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7d922-106">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvFreeFindCert(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCERT_CONTEXT pCertContext,
  _In_ void           *pvStoreProvFindInfo,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="7d922-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7d922-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d922-108">*hStoreProv* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7d922-108">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d922-109">Identificador de **HCERTSTOREPROV** de un [*almacén de certificados*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="7d922-109">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d922-110">*pCertContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7d922-110">*pCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d922-111">Un puntero a un [**\_ contexto de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).</span><span class="sxs-lookup"><span data-stu-id="7d922-111">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).</span></span>

</dd> <dt>

<span data-ttu-id="7d922-112">*pvStoreProvFindInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7d922-112">*pvStoreProvFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d922-113">Un puntero a un búfer que contiene información de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="7d922-113">A pointer to a buffer containing find information.</span></span>

</dd> <dt>

<span data-ttu-id="7d922-114">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7d922-114">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d922-115">Los valores de marca necesarios.</span><span class="sxs-lookup"><span data-stu-id="7d922-115">Any needed flag values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d922-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7d922-116">Return value</span></span>

<span data-ttu-id="7d922-117">Devuelve **true** si la función se ejecuta correctamente o **false** si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="7d922-117">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d922-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d922-118">Requirements</span></span>



| <span data-ttu-id="7d922-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d922-119">Requirement</span></span> | <span data-ttu-id="7d922-120">Value</span><span class="sxs-lookup"><span data-stu-id="7d922-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7d922-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7d922-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7d922-122">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="7d922-122">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="7d922-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7d922-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7d922-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7d922-124">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7d922-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d922-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d922-126">**contexto de certificado \_**</span><span class="sxs-lookup"><span data-stu-id="7d922-126">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[<span data-ttu-id="7d922-127">**CertStoreProvFindCert**</span><span class="sxs-lookup"><span data-stu-id="7d922-127">**CertStoreProvFindCert**</span></span>](certstoreprovfindcert.md)
</dt> </dl>

 

 
