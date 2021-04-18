---
description: Recupera el número de objetos PolicyInformation de la colección.
ms.assetid: d4fb6bd8-4e92-4de8-9430-dd3b6262a806
title: CertificatePolicies. Count (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0ee51e37b3fd4ac66c4e615eaf068edc98a64807
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691004"
---
# <a name="certificatepoliciescount-property"></a><span data-ttu-id="b716c-103">CertificatePolicies. Count (propiedad)</span><span class="sxs-lookup"><span data-stu-id="b716c-103">CertificatePolicies.Count property</span></span>

<span data-ttu-id="b716c-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b716c-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="b716c-105">En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para que las directivas de certificado recuperen las directivas de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="b716c-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to retrieve the certificate policies.\]</span></span>

<span data-ttu-id="b716c-106">La propiedad **Count** recupera el número de objetos [**PolicyInformation**](policyinformation.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="b716c-106">The **Count** property retrieves the number of [**PolicyInformation**](policyinformation.md) objects in the collection.</span></span>

<span data-ttu-id="b716c-107">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b716c-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b716c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b716c-108">Syntax</span></span>


```VB
CertificatePolicies.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="b716c-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b716c-109">Property value</span></span>

<span data-ttu-id="b716c-110">Número de objetos [**PolicyInformation**](policyinformation.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="b716c-110">The number of [**PolicyInformation**](policyinformation.md) objects in the collection.</span></span> <span data-ttu-id="b716c-111">Cada objeto **PolicyInformation** representa una única directiva de certificado en la colección.</span><span class="sxs-lookup"><span data-stu-id="b716c-111">Each **PolicyInformation** object represents a single certificate policy in the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="b716c-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b716c-112">Remarks</span></span>

<span data-ttu-id="b716c-113">La propiedad **Count** se puede usar para especificar el último objeto [**PolicyInformation**](policyinformation.md) de la colección al recuperar un objeto **PolicyInformation** específico mediante la propiedad [**CertificatePolicies. Item**](certificatepolicies-item.md) .</span><span class="sxs-lookup"><span data-stu-id="b716c-113">The **Count** property can be used to specify the last [**PolicyInformation**](policyinformation.md) object in the collection when retrieving a specific **PolicyInformation** object using the [**CertificatePolicies.Item**](certificatepolicies-item.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="b716c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b716c-114">Requirements</span></span>



| <span data-ttu-id="b716c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b716c-115">Requirement</span></span> | <span data-ttu-id="b716c-116">Value</span><span class="sxs-lookup"><span data-stu-id="b716c-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b716c-117">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="b716c-117">End of client support</span></span><br/> | <span data-ttu-id="b716c-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b716c-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b716c-119">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="b716c-119">End of server support</span></span><br/> | <span data-ttu-id="b716c-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b716c-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b716c-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="b716c-121">Redistributable</span></span><br/>       | <span data-ttu-id="b716c-122">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="b716c-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b716c-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b716c-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="b716c-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b716c-124"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
