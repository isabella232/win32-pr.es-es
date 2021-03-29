---
description: Se llama cuando no se usó el certificado devuelto por la devolución de llamada CertStoreProvFindCRL y, por tanto, se libera, en una llamada subsiguiente a CertStoreProvFindCRL.
ms.assetid: e90609f6-63cd-40eb-bd5a-289473daa5bb
title: Función de devolución de llamada CertStoreProvFreeFindCRL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCRL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: b5f5443d58a86c8bab979d17d64dc693d94ae373
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911786"
---
# <a name="certstoreprovfreefindcrl-callback-function"></a><span data-ttu-id="8ab10-103">Función de devolución de llamada CertStoreProvFreeFindCRL</span><span class="sxs-lookup"><span data-stu-id="8ab10-103">CertStoreProvFreeFindCRL callback function</span></span>

<span data-ttu-id="8ab10-104">Se llama a la función de devolución de llamada **CertStoreProvFreeFindCRL** cuando no se usó el certificado devuelto por la devolución de llamada [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) y, por tanto, se libera, en una llamada subsiguiente a **CertStoreProvFindCRL**.</span><span class="sxs-lookup"><span data-stu-id="8ab10-104">The **CertStoreProvFreeFindCRL** callback function is called when the certificate returned by the [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) callback was not used, and thus released, in a subsequent call to **CertStoreProvFindCRL**.</span></span> <span data-ttu-id="8ab10-105">Antes de que se llame a la devolución de llamada de cierre, el proveedor debe liberar todos los certificados devueltos por la devolución de llamada de [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) mediante **CertStoreProvFindCRL** o **CertStoreProvFreeFindCRL**.</span><span class="sxs-lookup"><span data-stu-id="8ab10-105">Before the CLOSE callback is called, all certificates returned by the [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) callback must be released by the provider using **CertStoreProvFindCRL** or **CertStoreProvFreeFindCRL**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ab10-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ab10-106">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvFreeFindCRL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCRL_CONTEXT  pCrlContext,
  _In_ void           *pvStoreProvFindInfo,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="8ab10-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8ab10-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ab10-108">*hStoreProv* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ab10-108">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ab10-109">Identificador de **HCERTSTOREPROV** de un [*almacén de certificados*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="8ab10-109">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="8ab10-110">*pCrlContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ab10-110">*pCrlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ab10-111">Un puntero a un [**\_ contexto de CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).</span><span class="sxs-lookup"><span data-stu-id="8ab10-111">A pointer to a [**CRL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).</span></span>

</dd> <dt>

<span data-ttu-id="8ab10-112">*pvStoreProvFindInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ab10-112">*pvStoreProvFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ab10-113">Un puntero a un búfer que contiene información de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8ab10-113">A pointer to a buffer containing find information.</span></span>

</dd> <dt>

<span data-ttu-id="8ab10-114">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ab10-114">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ab10-115">Los valores de marca necesarios.</span><span class="sxs-lookup"><span data-stu-id="8ab10-115">Any needed flag values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ab10-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8ab10-116">Return value</span></span>

<span data-ttu-id="8ab10-117">Devuelve **true** si la función se ejecuta correctamente o **false** si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="8ab10-117">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ab10-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ab10-118">Requirements</span></span>



| <span data-ttu-id="8ab10-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ab10-119">Requirement</span></span> | <span data-ttu-id="8ab10-120">Value</span><span class="sxs-lookup"><span data-stu-id="8ab10-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8ab10-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ab10-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8ab10-122">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="8ab10-122">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="8ab10-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ab10-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8ab10-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8ab10-124">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8ab10-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ab10-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ab10-126">**CertStoreProvFindCRL**</span><span class="sxs-lookup"><span data-stu-id="8ab10-126">**CertStoreProvFindCRL**</span></span>](certstoreprovfindcrl.md)
</dt> <dt>

[<span data-ttu-id="8ab10-127">**contexto de CRL \_**</span><span class="sxs-lookup"><span data-stu-id="8ab10-127">**CRL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
