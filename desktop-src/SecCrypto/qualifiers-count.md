---
description: Recupera el número de objetos de calificador de la colección.
ms.assetid: 9dafb83a-ff7f-4317-8ed4-2a46dcebf409
title: Propiedad Qualifiers. Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ffb79941a78602bfda8f5287b0f4df7205d4d86
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691014"
---
# <a name="qualifierscount-property"></a><span data-ttu-id="81b1e-103">Propiedad Qualifiers. Count</span><span class="sxs-lookup"><span data-stu-id="81b1e-103">Qualifiers.Count property</span></span>

<span data-ttu-id="81b1e-104">\[La propiedad **Count** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="81b1e-104">\[The **Count** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="81b1e-105">En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para las directivas de certificado para procesar calificadores que formen parte de la información de directivas en la extensión de directivas de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="81b1e-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="81b1e-106">La propiedad **Count** recupera el número de objetos de [**calificador**](qualifier.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="81b1e-106">The **Count** property retrieves the number of [**Qualifier**](qualifier.md) objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="81b1e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81b1e-107">Syntax</span></span>


```VB
Qualifiers.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="81b1e-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="81b1e-108">Property value</span></span>

<span data-ttu-id="81b1e-109">Número de objetos de [**calificador**](qualifier.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="81b1e-109">Number of [**Qualifier**](qualifier.md) objects in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="81b1e-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81b1e-110">Requirements</span></span>



| <span data-ttu-id="81b1e-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="81b1e-111">Requirement</span></span> | <span data-ttu-id="81b1e-112">Value</span><span class="sxs-lookup"><span data-stu-id="81b1e-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="81b1e-113">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="81b1e-113">Redistributable</span></span><br/> | <span data-ttu-id="81b1e-114">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="81b1e-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="81b1e-115">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="81b1e-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="81b1e-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81b1e-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81b1e-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="81b1e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81b1e-118">**Calificadores**</span><span class="sxs-lookup"><span data-stu-id="81b1e-118">**Qualifiers**</span></span>](qualifiers.md)
</dt> </dl>

 

 
