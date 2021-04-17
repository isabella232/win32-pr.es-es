---
description: Recupera el objeto PolicyInformation que representa la Directiva indizada. Esta es la propiedad predeterminada.
ms.assetid: 0143629a-97cf-43f4-8f96-774f0f5cfeca
title: CertificatePolicies. Item (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4a41cfb88f5f3ad59a8dbf62c85eca2a13c69f34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690960"
---
# <a name="certificatepoliciesitem-property"></a><span data-ttu-id="89eb7-104">CertificatePolicies. Item (propiedad)</span><span class="sxs-lookup"><span data-stu-id="89eb7-104">CertificatePolicies.Item property</span></span>

<span data-ttu-id="89eb7-105">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="89eb7-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="89eb7-106">En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para que las directivas de certificado recuperen las directivas de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="89eb7-106">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to retrieve the certificate policies.\]</span></span>

<span data-ttu-id="89eb7-107">La propiedad **Item** recupera el objeto [**PolicyInformation**](policyinformation.md) que representa la Directiva indizada.</span><span class="sxs-lookup"><span data-stu-id="89eb7-107">The **Item** property retrieves the [**PolicyInformation**](policyinformation.md) object that represents the indexed policy.</span></span> <span data-ttu-id="89eb7-108">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="89eb7-108">This is the default property.</span></span>

<span data-ttu-id="89eb7-109">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="89eb7-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="89eb7-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="89eb7-110">Syntax</span></span>


```VB
CertificatePolicies.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="89eb7-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="89eb7-111">Property value</span></span>

<span data-ttu-id="89eb7-112">Objeto [**PolicyInformation**](policyinformation.md) que representa la Directiva indizada.</span><span class="sxs-lookup"><span data-stu-id="89eb7-112">A [**PolicyInformation**](policyinformation.md) object that represents the indexed policy.</span></span>

## <a name="requirements"></a><span data-ttu-id="89eb7-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89eb7-113">Requirements</span></span>



| <span data-ttu-id="89eb7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="89eb7-114">Requirement</span></span> | <span data-ttu-id="89eb7-115">Value</span><span class="sxs-lookup"><span data-stu-id="89eb7-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="89eb7-116">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="89eb7-116">End of client support</span></span><br/> | <span data-ttu-id="89eb7-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89eb7-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="89eb7-118">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="89eb7-118">End of server support</span></span><br/> | <span data-ttu-id="89eb7-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="89eb7-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="89eb7-120">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="89eb7-120">Redistributable</span></span><br/>       | <span data-ttu-id="89eb7-121">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="89eb7-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="89eb7-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="89eb7-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="89eb7-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89eb7-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
