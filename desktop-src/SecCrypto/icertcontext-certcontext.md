---
description: Establece o recupera el contexto PCCERT \_ de un certificado.
ms.assetid: aedd219d-43fa-4722-9af4-36172d2c18b0
title: 'ICertContext:: CertContext (propiedad)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext.CertContext
- ICertContext.get_CertContext
- ICertContext.put_CertContext
- CertContext.CertContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 38bd1c704ca709fc1e4b6072bb68c2105dc5db9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671058"
---
# <a name="icertcontextcertcontext-property"></a><span data-ttu-id="ed347-103">ICertContext:: CertContext (propiedad)</span><span class="sxs-lookup"><span data-stu-id="ed347-103">ICertContext::CertContext property</span></span>

<span data-ttu-id="ed347-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="ed347-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="ed347-105">La propiedad **CertContext** establece o recupera el contexto PCCERT \_ de un certificado.</span><span class="sxs-lookup"><span data-stu-id="ed347-105">The **CertContext** property sets or retrieves the PCCERT\_CONTEXT of a certificate.</span></span>

<span data-ttu-id="ed347-106">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="ed347-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed347-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed347-107">Syntax</span></span>


```VB
CertContext.CertContext As Long
```



## <a name="property-value"></a><span data-ttu-id="ed347-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ed347-108">Property value</span></span>

<span data-ttu-id="ed347-109">Contexto PCCERT \_ del certificado.</span><span class="sxs-lookup"><span data-stu-id="ed347-109">The PCCERT\_CONTEXT of the certificate.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ed347-110">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="ed347-110">Error codes</span></span>

<span data-ttu-id="ed347-111">Si los métodos de acceso de propiedad **colocan \_ CertContext** y **Get \_ CertContext** se ejecutan correctamente, devuelven los valores \_ correctos.</span><span class="sxs-lookup"><span data-stu-id="ed347-111">If the property access methods **put\_CertContext** and **get\_CertContext** succeed, they return S\_OK.</span></span>

<span data-ttu-id="ed347-112">Cualquier otro valor **HRESULT** indica que se produjo un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="ed347-112">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed347-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ed347-113">Remarks</span></span>

<span data-ttu-id="ed347-114">Debe llamar al método [**FreeContext**](icertcontext-freecontext.md) o a la función [**CertFreeCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext) para liberar el contexto.</span><span class="sxs-lookup"><span data-stu-id="ed347-114">You must call either the [**FreeContext**](icertcontext-freecontext.md) method or the [**CertFreeCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext) function to free the context.</span></span>

<span data-ttu-id="ed347-115">Si establece la propiedad **CertContext** , se restablece el estado del objeto de [**certificado**](certificate.md) completo.</span><span class="sxs-lookup"><span data-stu-id="ed347-115">If you set the **CertContext** property, the state of the entire [**Certificate**](certificate.md) object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed347-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed347-116">Requirements</span></span>



| <span data-ttu-id="ed347-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed347-117">Requirement</span></span> | <span data-ttu-id="ed347-118">Value</span><span class="sxs-lookup"><span data-stu-id="ed347-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed347-119">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="ed347-119">Redistributable</span></span><br/> | <span data-ttu-id="ed347-120">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="ed347-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ed347-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ed347-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="ed347-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed347-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed347-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed347-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed347-124">**ICertContext**</span><span class="sxs-lookup"><span data-stu-id="ed347-124">**ICertContext**</span></span>](icertcontext.md)
</dt> </dl>

 

 




