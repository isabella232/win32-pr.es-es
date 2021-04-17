---
description: Recupera una propiedad especificada de una CRL.
ms.assetid: b02f4f92-952a-4625-a7d4-6e78e542774e
title: Función de devolución de llamada CertStoreProvGetCRLProperty
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCRLProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: bcf69653f03ccfbb52c8247c9ea459000db55e2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687386"
---
# <a name="certstoreprovgetcrlproperty-callback-function"></a><span data-ttu-id="45d23-103">Función de devolución de llamada CertStoreProvGetCRLProperty</span><span class="sxs-lookup"><span data-stu-id="45d23-103">CertStoreProvGetCRLProperty callback function</span></span>

<span data-ttu-id="45d23-104">La función de devolución de llamada **CertStoreProvGetCRLProperty** recupera una propiedad especificada de una [*CRL*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="45d23-104">The **CertStoreProvGetCRLProperty** callback function retrieves a specified property of a [*CRL*](../secgloss/c-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="45d23-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="45d23-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvGetCRLProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCRL_CONTEXT  pCrlContext,
  _In_    DWORD          dwPropId,
  _In_    DWORD          dwFlags,
  _Out_   void           *pvData,
  _Inout_ DWORD          *pcbData
);
```



## <a name="parameters"></a><span data-ttu-id="45d23-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="45d23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45d23-107">*hStoreProv* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="45d23-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45d23-108">Identificador de **HCERTSTOREPROV** de un [*almacén de certificados*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="45d23-108">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="45d23-109">*pCrlContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="45d23-109">*pCrlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45d23-110">Puntero a una estructura [**de \_ contexto de CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) .</span><span class="sxs-lookup"><span data-stu-id="45d23-110">A pointer to a [**CRL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) structure.</span></span>

</dd> <dt>

<span data-ttu-id="45d23-111">*dwPropId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="45d23-111">*dwPropId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45d23-112">Indica un identificador de propiedad.</span><span class="sxs-lookup"><span data-stu-id="45d23-112">Indicates a property identifier.</span></span>

</dd> <dt>

<span data-ttu-id="45d23-113">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="45d23-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45d23-114">Los valores de marca necesarios.</span><span class="sxs-lookup"><span data-stu-id="45d23-114">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="45d23-115">*pvData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="45d23-115">*pvData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45d23-116">Puntero a un búfer que va a contener el puntero a una estructura de [**\_ contexto de CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) que va a devolver la función.</span><span class="sxs-lookup"><span data-stu-id="45d23-116">A pointer to a buffer to contain the pointer to a [**CRL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) structure to be returned by the function.</span></span> <span data-ttu-id="45d23-117">Se puede establecer en **null** en una primera llamada a la función para obtener el valor de *pcbData* antes de asignar memoria para el búfer.</span><span class="sxs-lookup"><span data-stu-id="45d23-117">May be set to **NULL** on a first call to the function to get the value of *pcbData* before allocating memory for the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="45d23-118">*pcbData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="45d23-118">*pcbData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="45d23-119">Un puntero a un **valor DWORD** que indica la longitud del búfer *pvData* .</span><span class="sxs-lookup"><span data-stu-id="45d23-119">A pointer to a **DWORD** indicating the length of the *pvData* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45d23-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="45d23-120">Return value</span></span>

<span data-ttu-id="45d23-121">Devuelve **true** si la función se ejecuta correctamente o **false** si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="45d23-121">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="45d23-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45d23-122">Requirements</span></span>



| <span data-ttu-id="45d23-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="45d23-123">Requirement</span></span> | <span data-ttu-id="45d23-124">Value</span><span class="sxs-lookup"><span data-stu-id="45d23-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="45d23-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45d23-125">Minimum supported client</span></span><br/> | <span data-ttu-id="45d23-126">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="45d23-126">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="45d23-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45d23-127">Minimum supported server</span></span><br/> | <span data-ttu-id="45d23-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="45d23-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="45d23-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="45d23-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45d23-130">**contexto de CRL \_**</span><span class="sxs-lookup"><span data-stu-id="45d23-130">**CRL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)
</dt> </dl>

 

 
