---
description: Lo llama CertDeleteCTLFromStore antes de eliminar una CTL del almacén.
ms.assetid: 6cda772f-7e94-414d-99fc-a90451ac0ccf
title: Función de devolución de llamada CertStoreProvDeleteCTL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvDeleteCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: abeea0fdc3b6d77974b2c057d0e2ea98fe11e63a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908970"
---
# <a name="certstoreprovdeletectl-callback-function"></a><span data-ttu-id="9469e-103">Función de devolución de llamada CertStoreProvDeleteCTL</span><span class="sxs-lookup"><span data-stu-id="9469e-103">CertStoreProvDeleteCTL callback function</span></span>

<span data-ttu-id="9469e-104">[**CertDeleteCTLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore) llama a la función de devolución de llamada **CertStoreProvDeleteCTL** antes de eliminar una CTL del almacén.</span><span class="sxs-lookup"><span data-stu-id="9469e-104">The **CertStoreProvDeleteCTL** callback function is called by [**CertDeleteCTLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore) before deleting a CTL from the store.</span></span> <span data-ttu-id="9469e-105">Esta función determina si se puede eliminar una CTL.</span><span class="sxs-lookup"><span data-stu-id="9469e-105">This function determines whether a CTL can be deleted.</span></span>

## <a name="syntax"></a><span data-ttu-id="9469e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9469e-106">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvDeleteCTL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCTL_CONTEXT  pCtlContext,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="9469e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9469e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9469e-108">*hStoreProv* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9469e-108">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9469e-109">Identificador de **HCERTSTOREPROV** de un [*almacén de certificados*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="9469e-109">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="9469e-110">*pCtlContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9469e-110">*pCtlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9469e-111">Puntero a una estructura [**de \_ contexto de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) .</span><span class="sxs-lookup"><span data-stu-id="9469e-111">A pointer to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9469e-112">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9469e-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9469e-113">Los valores de marca necesarios.</span><span class="sxs-lookup"><span data-stu-id="9469e-113">Any needed flag values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9469e-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9469e-114">Return value</span></span>

<span data-ttu-id="9469e-115">Devuelve **true** si se puede eliminar una CTL del almacén.</span><span class="sxs-lookup"><span data-stu-id="9469e-115">Returns **TRUE** if a CTL can be deleted from the store.</span></span>

## <a name="requirements"></a><span data-ttu-id="9469e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9469e-116">Requirements</span></span>



| <span data-ttu-id="9469e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9469e-117">Requirement</span></span> | <span data-ttu-id="9469e-118">Value</span><span class="sxs-lookup"><span data-stu-id="9469e-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9469e-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9469e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9469e-120">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="9469e-120">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="9469e-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9469e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9469e-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9469e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 
