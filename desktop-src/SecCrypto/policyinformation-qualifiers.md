---
description: Recupera una colección de los calificadores de la Directiva.
ms.assetid: aa5e2225-0a39-40bc-868c-d96f5953edaa
title: PolicyInformation. Qualifiers (propiedad) (iAds. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation.Qualifiers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 89f24e21acd24cbcaa021f7c668fc8c208102c0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690024"
---
# <a name="policyinformationqualifiers-property"></a><span data-ttu-id="de34d-103">PolicyInformation. Qualifiers (propiedad)</span><span class="sxs-lookup"><span data-stu-id="de34d-103">PolicyInformation.Qualifiers property</span></span>

<span data-ttu-id="de34d-104">\[La propiedad **calificadores** está disponible para su uso en los sistemas operativos especificados en la sección requisitos.</span><span class="sxs-lookup"><span data-stu-id="de34d-104">\[The **Qualifiers** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="de34d-105">En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para las directivas de certificado para procesar la información de la Directiva en la extensión de directivas de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="de34d-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process policy information in the Certificate policies extension.\]</span></span>

<span data-ttu-id="de34d-106">La propiedad **calificadores** recupera una colección de los calificadores de la Directiva.</span><span class="sxs-lookup"><span data-stu-id="de34d-106">The **Qualifiers** property retrieves a collection of the policy's qualifiers.</span></span>

## <a name="syntax"></a><span data-ttu-id="de34d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="de34d-107">Syntax</span></span>


```VB
PolicyInformation.Qualifiers As Qualifiers
```



## <a name="property-value"></a><span data-ttu-id="de34d-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="de34d-108">Property value</span></span>

<span data-ttu-id="de34d-109">Calificador del informe de prácticas de certificación (CPS) de la Directiva o calificadores de aviso de usuario, como un objeto de [**calificadores**](qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="de34d-109">The policy's Certification Practice Statement (CPS) pointer or user notice qualifiers, as a [**Qualifiers**](qualifiers.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="de34d-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de34d-110">Requirements</span></span>



| <span data-ttu-id="de34d-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="de34d-111">Requirement</span></span> | <span data-ttu-id="de34d-112">Value</span><span class="sxs-lookup"><span data-stu-id="de34d-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="de34d-113">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="de34d-113">Redistributable</span></span><br/> | <span data-ttu-id="de34d-114">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="de34d-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="de34d-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="de34d-115">Header</span></span><br/>          | <dl> <span data-ttu-id="de34d-116"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="de34d-116"><dt>Iads.h</dt></span></span> </dl>      |
| <span data-ttu-id="de34d-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="de34d-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="de34d-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de34d-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de34d-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="de34d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de34d-120">**PolicyInformation**</span><span class="sxs-lookup"><span data-stu-id="de34d-120">**PolicyInformation**</span></span>](policyinformation.md)
</dt> </dl>

 

 
