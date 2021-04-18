---
description: Recupera el número de versión principal de la plantilla.
ms.assetid: efde3a7c-48e0-4bfe-9118-3098c7ef8771
title: Template. MajorVersion (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.MajorVersion
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a193a36ed7e914d1ed45d26c21008a7e59a5b8a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671302"
---
# <a name="templatemajorversion-property"></a><span data-ttu-id="94773-103">Template. MajorVersion (propiedad)</span><span class="sxs-lookup"><span data-stu-id="94773-103">Template.MajorVersion property</span></span>

<span data-ttu-id="94773-104">\[La propiedad **MajorVersion** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="94773-104">\[The **MajorVersion** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="94773-105">En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID de la plantilla de certificado para recuperar la plantilla de extensión de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="94773-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="94773-106">La propiedad **MajorVersion** recupera el número de versión principal de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="94773-106">The **MajorVersion** property retrieves the major version number of the template.</span></span>

## <a name="syntax"></a><span data-ttu-id="94773-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="94773-107">Syntax</span></span>


```VB
Template.MajorVersion As Long
```



## <a name="property-value"></a><span data-ttu-id="94773-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="94773-108">Property value</span></span>

<span data-ttu-id="94773-109">Número de versión principal de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="94773-109">The major version number of the template.</span></span>

## <a name="requirements"></a><span data-ttu-id="94773-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94773-110">Requirements</span></span>



| <span data-ttu-id="94773-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="94773-111">Requirement</span></span> | <span data-ttu-id="94773-112">Value</span><span class="sxs-lookup"><span data-stu-id="94773-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="94773-113">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="94773-113">Redistributable</span></span><br/> | <span data-ttu-id="94773-114">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="94773-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="94773-115">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="94773-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="94773-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94773-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94773-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="94773-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94773-118">**Plantilla**</span><span class="sxs-lookup"><span data-stu-id="94773-118">**Template**</span></span>](template.md)
</dt> </dl>

 

 
