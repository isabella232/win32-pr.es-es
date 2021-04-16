---
description: Recupera el nombre de la plantilla.
ms.assetid: f92346bc-89b6-4063-aa66-85e2fb88d67d
title: Propiedad Template.Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 005a9cc961b1d7be0ebda0b8e76307b95d92a6d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671301"
---
# <a name="templatename-property"></a><span data-ttu-id="26a77-103">Propiedad Template.Name</span><span class="sxs-lookup"><span data-stu-id="26a77-103">Template.Name property</span></span>

<span data-ttu-id="26a77-104">\[La propiedad **nombre** está disponible para su uso en los sistemas operativos especificados en la sección requisitos.</span><span class="sxs-lookup"><span data-stu-id="26a77-104">\[The **Name** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="26a77-105">En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID de la plantilla de certificado para recuperar la plantilla de extensión de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="26a77-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="26a77-106">La propiedad **Name** recupera el nombre de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="26a77-106">The **Name** property retrieves the name of the template.</span></span>

## <a name="syntax"></a><span data-ttu-id="26a77-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="26a77-107">Syntax</span></span>


```VB
Template.Name As String
```



## <a name="property-value"></a><span data-ttu-id="26a77-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="26a77-108">Property value</span></span>

<span data-ttu-id="26a77-109">Nombre de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="26a77-109">The name of the template.</span></span>

## <a name="requirements"></a><span data-ttu-id="26a77-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26a77-110">Requirements</span></span>



| <span data-ttu-id="26a77-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="26a77-111">Requirement</span></span> | <span data-ttu-id="26a77-112">Value</span><span class="sxs-lookup"><span data-stu-id="26a77-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="26a77-113">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="26a77-113">Redistributable</span></span><br/> | <span data-ttu-id="26a77-114">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="26a77-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="26a77-115">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="26a77-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="26a77-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26a77-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26a77-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="26a77-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26a77-118">**Plantilla**</span><span class="sxs-lookup"><span data-stu-id="26a77-118">**Template**</span></span>](template.md)
</dt> </dl>

 

 
