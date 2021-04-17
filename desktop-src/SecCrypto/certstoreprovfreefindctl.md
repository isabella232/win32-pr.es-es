---
description: Se llama cuando no se usó el certificado devuelto por la devolución de llamada CertStoreProvFindCTL y, por tanto, se libera, en una llamada subsiguiente a CertStoreProvFindCTL.
ms.assetid: 04e62a4e-4542-4225-8750-fabbda5adf0d
title: Función de devolución de llamada CertStoreProvFreeFindCTL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: ff0c9c3b7be6b8a4cafd759c3411f5096ee8640b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687387"
---
# <a name="certstoreprovfreefindctl-callback-function"></a><span data-ttu-id="b8040-103">Función de devolución de llamada CertStoreProvFreeFindCTL</span><span class="sxs-lookup"><span data-stu-id="b8040-103">CertStoreProvFreeFindCTL callback function</span></span>

<span data-ttu-id="b8040-104">Se llama a la función de devolución de llamada **CertStoreProvFreeFindCTL** cuando no se usó el certificado devuelto por la devolución de llamada [**CertStoreProvFindCTL**](certstoreprovfindctl.md) y, por tanto, se libera, en una llamada subsiguiente a **CertStoreProvFindCTL**.</span><span class="sxs-lookup"><span data-stu-id="b8040-104">The **CertStoreProvFreeFindCTL** callback function is called when the certificate returned by the [**CertStoreProvFindCTL**](certstoreprovfindctl.md) callback was not used, and thus released, in a subsequent call to **CertStoreProvFindCTL**.</span></span> <span data-ttu-id="b8040-105">Antes de que se llame a la devolución de llamada de cierre, el proveedor debe liberar todos los certificados devueltos por la devolución de llamada de [**CertStoreProvFindCTL**](certstoreprovfindctl.md) mediante **CertStoreProvFindCTL** o **CertStoreProvFreeFindCTL**.</span><span class="sxs-lookup"><span data-stu-id="b8040-105">Before the CLOSE callback is called, all certificates returned by the [**CertStoreProvFindCTL**](certstoreprovfindctl.md) callback must be released by the provider using **CertStoreProvFindCTL** or **CertStoreProvFreeFindCTL**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8040-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8040-106">Syntax</span></span>


```C++
BOOL CertStoreProvFreeFindCTL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCTL_CONTEXT  pCtlContext,
  _In_ void           *pvStoreProvFindInfo,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="b8040-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8040-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8040-108">*hStoreProv* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b8040-108">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8040-109">Identificador de **HCERTSTOREPROV** de un [*almacén de certificados*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b8040-109">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8040-110">*pCtlContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b8040-110">*pCtlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8040-111">Puntero a una estructura [**de \_ contexto de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) .</span><span class="sxs-lookup"><span data-stu-id="b8040-111">A pointer to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b8040-112">*pvStoreProvFindInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b8040-112">*pvStoreProvFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8040-113">Un puntero a un búfer que contiene información de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="b8040-113">A pointer to a buffer containing find information.</span></span>

</dd> <dt>

<span data-ttu-id="b8040-114">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b8040-114">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8040-115">Los valores de marca necesarios.</span><span class="sxs-lookup"><span data-stu-id="b8040-115">Any needed flag values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8040-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b8040-116">Return value</span></span>

<span data-ttu-id="b8040-117">Devuelve **true** si la función se ejecuta correctamente o **false** si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="b8040-117">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8040-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8040-118">Requirements</span></span>



| <span data-ttu-id="b8040-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8040-119">Requirement</span></span> | <span data-ttu-id="b8040-120">Value</span><span class="sxs-lookup"><span data-stu-id="b8040-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b8040-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8040-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b8040-122">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="b8040-122">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="b8040-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8040-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b8040-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b8040-124">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b8040-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8040-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8040-126">**CertStoreProvFindCTL**</span><span class="sxs-lookup"><span data-stu-id="b8040-126">**CertStoreProvFindCTL**</span></span>](certstoreprovfindctl.md)
</dt> <dt>

[<span data-ttu-id="b8040-127">**\_contexto CTL**</span><span class="sxs-lookup"><span data-stu-id="b8040-127">**CTL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
