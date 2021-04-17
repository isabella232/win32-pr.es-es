---
description: Recupera el contenido del aviso de usuario.
ms.assetid: dcf73357-253d-4160-be4e-f826296f5eaa
title: Propiedad Qualifier. ExplicitText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.ExplicitText
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7d2ba5e6bbf6bb46e28c5dbb6fa9754c72b66dd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690272"
---
# <a name="qualifierexplicittext-property"></a><span data-ttu-id="80494-103">Propiedad Qualifier. ExplicitText</span><span class="sxs-lookup"><span data-stu-id="80494-103">Qualifier.ExplicitText property</span></span>

<span data-ttu-id="80494-104">\[La propiedad **ExplicitText** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="80494-104">\[The **ExplicitText** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="80494-105">En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para las directivas de certificado para procesar calificadores que formen parte de la información de directivas en la extensión de directivas de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="80494-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="80494-106">La propiedad **ExplicitText** recupera el contenido del aviso de usuario.</span><span class="sxs-lookup"><span data-stu-id="80494-106">The **ExplicitText** property retrieves the content of the user notice.</span></span> <span data-ttu-id="80494-107">Esta propiedad puede estar vacía.</span><span class="sxs-lookup"><span data-stu-id="80494-107">This property may be empty.</span></span>

## <a name="syntax"></a><span data-ttu-id="80494-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="80494-108">Syntax</span></span>


```VB
Qualifier.ExplicitText As String
```



## <a name="property-value"></a><span data-ttu-id="80494-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="80494-109">Property value</span></span>

<span data-ttu-id="80494-110">El contenido del aviso de usuario.</span><span class="sxs-lookup"><span data-stu-id="80494-110">The content of the user notice.</span></span>

## <a name="requirements"></a><span data-ttu-id="80494-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80494-111">Requirements</span></span>



| <span data-ttu-id="80494-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="80494-112">Requirement</span></span> | <span data-ttu-id="80494-113">Value</span><span class="sxs-lookup"><span data-stu-id="80494-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="80494-114">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="80494-114">Redistributable</span></span><br/> | <span data-ttu-id="80494-115">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="80494-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="80494-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="80494-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="80494-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80494-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80494-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="80494-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80494-119">**Qualifier**</span><span class="sxs-lookup"><span data-stu-id="80494-119">**Qualifier**</span></span>](qualifier.md)
</dt> </dl>

 

 
