---
description: Recupera una propiedad especificada de una lista de certificados de confianza (CTL).
ms.assetid: 65309715-65b4-4608-960d-3404e68800a2
title: Función de devolución de llamada CertStoreProvGetCTLProperty
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCTLProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: e30a9e735d44fc5681d5cd3932baaf3cc90aa30d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668101"
---
# <a name="certstoreprovgetctlproperty-callback-function"></a><span data-ttu-id="f44a5-103">Función de devolución de llamada CertStoreProvGetCTLProperty</span><span class="sxs-lookup"><span data-stu-id="f44a5-103">CertStoreProvGetCTLProperty callback function</span></span>

<span data-ttu-id="f44a5-104">La función de devolución de llamada **CertStoreProvGetCTLProperty** recupera una propiedad especificada de una [*lista de certificados de confianza*](../secgloss/c-gly.md) (CTL).</span><span class="sxs-lookup"><span data-stu-id="f44a5-104">The **CertStoreProvGetCTLProperty** callback function retrieves a specified property of a [*certificate trust list*](../secgloss/c-gly.md) (CTL).</span></span>

## <a name="syntax"></a><span data-ttu-id="f44a5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f44a5-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvGetCTLProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCTL_CONTEXT  pCtlContext,
  _In_    DWORD          dwPropId,
  _In_    DWORD          dwFlags,
  _Out_   void           *pvData,
  _Inout_ DWORD          *pcbData
);
```



## <a name="parameters"></a><span data-ttu-id="f44a5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f44a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f44a5-107">*hStoreProv* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f44a5-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f44a5-108">Identificador de **HCERTSTOREPROV** de un [*almacén de certificados*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f44a5-108">A **HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="f44a5-109">*pCtlContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f44a5-109">*pCtlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f44a5-110">Puntero a una estructura [**de \_ contexto de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) .</span><span class="sxs-lookup"><span data-stu-id="f44a5-110">A pointer to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f44a5-111">*dwPropId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f44a5-111">*dwPropId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f44a5-112">Indica un identificador de propiedad.</span><span class="sxs-lookup"><span data-stu-id="f44a5-112">Indicates a property identifier.</span></span>

</dd> <dt>

<span data-ttu-id="f44a5-113">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f44a5-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f44a5-114">Los valores de marca necesarios.</span><span class="sxs-lookup"><span data-stu-id="f44a5-114">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="f44a5-115">*pvData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f44a5-115">*pvData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f44a5-116">Puntero a un búfer que va a contener el puntero a una estructura de [**\_ contexto de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) que va a devolver la función.</span><span class="sxs-lookup"><span data-stu-id="f44a5-116">A pointer to a buffer to contain the pointer to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) structure to be returned by the function.</span></span> <span data-ttu-id="f44a5-117">Para obtener el valor de *pcbData* antes de asignar memoria para el búfer, este parámetro se puede establecer en **null** en una primera llamada a la función.</span><span class="sxs-lookup"><span data-stu-id="f44a5-117">To get the value of *pcbData* before allocating memory for the buffer, this parameter can be set to **NULL** on a first call to the function.</span></span>

</dd> <dt>

<span data-ttu-id="f44a5-118">*pcbData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f44a5-118">*pcbData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f44a5-119">Un puntero a un **valor DWORD** que indica la longitud del búfer *pvData* .</span><span class="sxs-lookup"><span data-stu-id="f44a5-119">A pointer to a **DWORD** that indicates the length of the *pvData* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f44a5-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f44a5-120">Return value</span></span>

<span data-ttu-id="f44a5-121">Si la función se ejecuta correctamente, la función devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="f44a5-121">If the function succeeds, the function returns nonzero.</span></span>

<span data-ttu-id="f44a5-122">Si se produce un error en la función, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="f44a5-122">If the function fails, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="f44a5-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f44a5-123">Requirements</span></span>



| <span data-ttu-id="f44a5-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f44a5-124">Requirement</span></span> | <span data-ttu-id="f44a5-125">Value</span><span class="sxs-lookup"><span data-stu-id="f44a5-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f44a5-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f44a5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f44a5-127">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f44a5-127">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="f44a5-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f44a5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f44a5-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f44a5-129">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f44a5-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="f44a5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f44a5-131">**\_contexto CTL**</span><span class="sxs-lookup"><span data-stu-id="f44a5-131">**CTL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
