---
description: Recupera una propiedad especificada de un certificado.
ms.assetid: 827e0331-1f87-4891-8cc1-de1bcbad2963
title: Función de devolución de llamada CertStoreProvGetCertProperty
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCertProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 50de9a73438e2755e002570f921d15e6086a4b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666985"
---
# <a name="certstoreprovgetcertproperty-callback-function"></a><span data-ttu-id="01731-103">Función de devolución de llamada CertStoreProvGetCertProperty</span><span class="sxs-lookup"><span data-stu-id="01731-103">CertStoreProvGetCertProperty callback function</span></span>

<span data-ttu-id="01731-104">La función de devolución de llamada **CertStoreProvGetCertProperty** recupera una propiedad especificada de un certificado.</span><span class="sxs-lookup"><span data-stu-id="01731-104">The **CertStoreProvGetCertProperty** callback function retrieves a specified property of a certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="01731-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="01731-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvGetCertProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCERT_CONTEXT pCertContext,
  _In_    DWORD          dwPropId,
  _In_    DWORD          dwFlags,
  _Out_   void           *pvData,
  _Inout_ DWORD          *pcbData
);
```



## <a name="parameters"></a><span data-ttu-id="01731-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="01731-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01731-107">*hStoreProv* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="01731-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01731-108">Identificador de **HCERTSTOREPROV** de un [*almacén de certificados*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="01731-108">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="01731-109">*pCertContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="01731-109">*pCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01731-110">Puntero a una estructura [**de \_ contexto de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) .</span><span class="sxs-lookup"><span data-stu-id="01731-110">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure.</span></span>

</dd> <dt>

<span data-ttu-id="01731-111">*dwPropId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="01731-111">*dwPropId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01731-112">Indica un identificador de propiedad.</span><span class="sxs-lookup"><span data-stu-id="01731-112">Indicates a property identifier.</span></span>

</dd> <dt>

<span data-ttu-id="01731-113">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="01731-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01731-114">Los valores de marca necesarios.</span><span class="sxs-lookup"><span data-stu-id="01731-114">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="01731-115">*pvData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="01731-115">*pvData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01731-116">Puntero a un búfer que va a contener el puntero a una estructura de [**\_ contexto de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) que va a devolver la función.</span><span class="sxs-lookup"><span data-stu-id="01731-116">A pointer to a buffer to contain the pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure to be returned by the function.</span></span> <span data-ttu-id="01731-117">Se puede establecer en **null** en una primera llamada a la función para obtener el valor de *pcbData* antes de asignar memoria para el búfer.</span><span class="sxs-lookup"><span data-stu-id="01731-117">May be set to **NULL** on a first call to the function to get the value of *pcbData* before allocating memory for the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="01731-118">*pcbData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="01731-118">*pcbData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="01731-119">Un puntero a un **valor DWORD** que indica la longitud del búfer *pvData* .</span><span class="sxs-lookup"><span data-stu-id="01731-119">A pointer to a **DWORD** indicating the length of the *pvData* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01731-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="01731-120">Return value</span></span>

<span data-ttu-id="01731-121">Devuelve **true** si la función se ejecuta correctamente o **false** si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="01731-121">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="01731-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01731-122">Requirements</span></span>



| <span data-ttu-id="01731-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="01731-123">Requirement</span></span> | <span data-ttu-id="01731-124">Value</span><span class="sxs-lookup"><span data-stu-id="01731-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="01731-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01731-125">Minimum supported client</span></span><br/> | <span data-ttu-id="01731-126">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="01731-126">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="01731-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01731-127">Minimum supported server</span></span><br/> | <span data-ttu-id="01731-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="01731-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="01731-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="01731-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01731-130">**contexto de certificado \_**</span><span class="sxs-lookup"><span data-stu-id="01731-130">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
