---
description: Recupera un valor booleano que indica si la extensión de plantilla está presente.
ms.assetid: cc7f9853-8212-470d-b372-43a4bbd517f7
title: Propiedad template. IsPresent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 23dcd8cc5ee92a689300078d439998e43933af93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649509"
---
# <a name="templateispresent-property"></a><span data-ttu-id="a509d-103">Propiedad template. IsPresent</span><span class="sxs-lookup"><span data-stu-id="a509d-103">Template.IsPresent property</span></span>

<span data-ttu-id="a509d-104">\[La propiedad **IsPresent** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="a509d-104">\[The **IsPresent** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a509d-105">En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID de la plantilla de certificado para recuperar la plantilla de extensión de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="a509d-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="a509d-106">La propiedad **IsPresent** recupera un valor booleano que indica si la extensión de plantilla está presente.</span><span class="sxs-lookup"><span data-stu-id="a509d-106">The **IsPresent** property retrieves a Boolean value that indicates whether the template extension is present.</span></span>

## <a name="syntax"></a><span data-ttu-id="a509d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a509d-107">Syntax</span></span>


```VB
Template.IsPresent As Boolean
```



## <a name="property-value"></a><span data-ttu-id="a509d-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a509d-108">Property value</span></span>

<span data-ttu-id="a509d-109">Si es **true**, la extensión de plantilla está presente.</span><span class="sxs-lookup"><span data-stu-id="a509d-109">If **true**, the template extension is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="a509d-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a509d-110">Requirements</span></span>



| <span data-ttu-id="a509d-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="a509d-111">Requirement</span></span> | <span data-ttu-id="a509d-112">Value</span><span class="sxs-lookup"><span data-stu-id="a509d-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a509d-113">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="a509d-113">Redistributable</span></span><br/> | <span data-ttu-id="a509d-114">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="a509d-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a509d-115">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a509d-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="a509d-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a509d-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a509d-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="a509d-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a509d-118">**Plantilla**</span><span class="sxs-lookup"><span data-stu-id="a509d-118">**Template**</span></span>](template.md)
</dt> </dl>

 

 
