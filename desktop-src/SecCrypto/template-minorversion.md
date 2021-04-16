---
description: Recupera el número de versión secundaria de la plantilla.
ms.assetid: 3fc51d43-9113-4b4b-88ab-27cf6e5c4fa0
title: Template. MinorVersion (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.MinorVersion
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2a1de0beb41cbe87ca86b443c5cc2145c2058073
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649977"
---
# <a name="templateminorversion-property"></a><span data-ttu-id="9706e-103">Template. MinorVersion (propiedad)</span><span class="sxs-lookup"><span data-stu-id="9706e-103">Template.MinorVersion property</span></span>

<span data-ttu-id="9706e-104">\[La propiedad **MinorVersion** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="9706e-104">\[The **MinorVersion** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9706e-105">En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID de la plantilla de certificado para recuperar la plantilla de extensión de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="9706e-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="9706e-106">La propiedad **MinorVersion** recupera el número de versión secundaria de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="9706e-106">The **MinorVersion** property retrieves the minor version number of the template.</span></span>

## <a name="syntax"></a><span data-ttu-id="9706e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9706e-107">Syntax</span></span>


```VB
Template.MinorVersion As Long
```



## <a name="property-value"></a><span data-ttu-id="9706e-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="9706e-108">Property value</span></span>

<span data-ttu-id="9706e-109">Número de versión secundaria de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="9706e-109">The minor version number of the template.</span></span>

## <a name="requirements"></a><span data-ttu-id="9706e-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9706e-110">Requirements</span></span>



| <span data-ttu-id="9706e-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="9706e-111">Requirement</span></span> | <span data-ttu-id="9706e-112">Value</span><span class="sxs-lookup"><span data-stu-id="9706e-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9706e-113">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="9706e-113">Redistributable</span></span><br/> | <span data-ttu-id="9706e-114">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="9706e-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9706e-115">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9706e-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="9706e-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9706e-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9706e-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="9706e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9706e-118">**Plantilla**</span><span class="sxs-lookup"><span data-stu-id="9706e-118">**Template**</span></span>](template.md)
</dt> </dl>

 

 
