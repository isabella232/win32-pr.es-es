---
description: Recupera un valor booleano que indica si la extensión de plantilla está marcada como crítica.
ms.assetid: 37e2000a-d3c8-46b5-84e5-a3904fdbaeea
title: Propiedad template. IsCritical
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 66f9dc90828cd474497478872f154adbd3fcd12a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649853"
---
# <a name="templateiscritical-property"></a><span data-ttu-id="937b8-103">Propiedad template. IsCritical</span><span class="sxs-lookup"><span data-stu-id="937b8-103">Template.IsCritical property</span></span>

<span data-ttu-id="937b8-104">\[La propiedad **IsCritical** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="937b8-104">\[The **IsCritical** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="937b8-105">En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID de la plantilla de certificado para recuperar la plantilla de extensión de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="937b8-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="937b8-106">La propiedad **IsCritical** recupera un valor booleano que indica si la extensión de plantilla está marcada como crítica.</span><span class="sxs-lookup"><span data-stu-id="937b8-106">The **IsCritical** property retrieves a Boolean value that indicates whether the template extension is marked critical.</span></span>

## <a name="syntax"></a><span data-ttu-id="937b8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="937b8-107">Syntax</span></span>


```VB
Template.IsCritical As Boolean
```



## <a name="property-value"></a><span data-ttu-id="937b8-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="937b8-108">Property value</span></span>

<span data-ttu-id="937b8-109">Si es **true**, la extensión de plantilla se marca como crítica.</span><span class="sxs-lookup"><span data-stu-id="937b8-109">If **true**, the template extension is marked critical.</span></span>

## <a name="requirements"></a><span data-ttu-id="937b8-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="937b8-110">Requirements</span></span>



| <span data-ttu-id="937b8-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="937b8-111">Requirement</span></span> | <span data-ttu-id="937b8-112">Value</span><span class="sxs-lookup"><span data-stu-id="937b8-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="937b8-113">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="937b8-113">Redistributable</span></span><br/> | <span data-ttu-id="937b8-114">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="937b8-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="937b8-115">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="937b8-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="937b8-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="937b8-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="937b8-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="937b8-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="937b8-118">**Plantilla**</span><span class="sxs-lookup"><span data-stu-id="937b8-118">**Template**</span></span>](template.md)
</dt> </dl>

 

 
