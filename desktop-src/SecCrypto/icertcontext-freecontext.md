---
description: Libera un \_ contexto PCCERT adquirido a través de la propiedad CertContext.
ms.assetid: fcb9e885-d26c-4866-a35d-1c940bfe8162
title: 'ICertContext:: FreeContext (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext.FreeContext
- CertContext.FreeContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e1f4c216f6e417726e60d5f2e2bd67387a51d352
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671060"
---
# <a name="icertcontextfreecontext-method"></a><span data-ttu-id="7a2b2-103">ICertContext:: FreeContext (método)</span><span class="sxs-lookup"><span data-stu-id="7a2b2-103">ICertContext::FreeContext method</span></span>

<span data-ttu-id="7a2b2-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="7a2b2-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="7a2b2-105">El método **FreeContext** libera un \_ contexto PCCERT adquirido a través de la propiedad [**CertContext**](icertcontext-certcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="7a2b2-105">The **FreeContext** method releases a PCCERT\_CONTEXT acquired through the [**CertContext**](icertcontext-certcontext.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a2b2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7a2b2-106">Syntax</span></span>


```VB
CertContext.FreeContext( _
  ByVal pCertContext _
)
```



## <a name="parameters"></a><span data-ttu-id="7a2b2-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7a2b2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a2b2-108">*pCertContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7a2b2-108">*pCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a2b2-109">Contexto de PCCERT \_ que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-109">The PCCERT\_CONTEXT to be released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a2b2-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7a2b2-110">Return value</span></span>

<span data-ttu-id="7a2b2-111">El valor devuelto es **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-111">The return value is an **HRESULT**.</span></span> <span data-ttu-id="7a2b2-112">Un valor de S \_ OK indica que se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-112">A value of S\_OK indicates success.</span></span> <span data-ttu-id="7a2b2-113">Cualquier otro valor indica que se produjo un error en la operación.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-113">Any other value indicates that the operation failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a2b2-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7a2b2-114">Remarks</span></span>

<span data-ttu-id="7a2b2-115">Este método no libera el contexto PCCERT \_ contenido dentro de un objeto de [**certificado**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="7a2b2-115">This method does not release the PCCERT\_CONTEXT contained within a [**Certificate**](certificate.md) object.</span></span> <span data-ttu-id="7a2b2-116">Solo se debe usar para liberar un contexto PCCERT \_ adquirido a través de la propiedad [**CertContext**](icertcontext-certcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="7a2b2-116">It should be used only to release a PCCERT\_CONTEXT acquired through the [**CertContext**](icertcontext-certcontext.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a2b2-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a2b2-117">Requirements</span></span>



| <span data-ttu-id="7a2b2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a2b2-118">Requirement</span></span> | <span data-ttu-id="7a2b2-119">Value</span><span class="sxs-lookup"><span data-stu-id="7a2b2-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a2b2-120">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="7a2b2-120">Redistributable</span></span><br/> | <span data-ttu-id="7a2b2-121">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="7a2b2-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7a2b2-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7a2b2-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="7a2b2-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a2b2-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a2b2-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="7a2b2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a2b2-125">**ICertContext**</span><span class="sxs-lookup"><span data-stu-id="7a2b2-125">**ICertContext**</span></span>](icertcontext.md)
</dt> </dl>

 

 




