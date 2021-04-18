---
description: Recupera el nombre de la organización asociada al calificador.
ms.assetid: 4ceb2c0f-903d-4fcd-8446-abf3175fe8e0
title: Propiedad Qualifier. NombreOrganización
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.OrganizationName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b1e1ebb2b948d5a933b59e86c8753b6b68a3a94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649877"
---
# <a name="qualifierorganizationname-property"></a><span data-ttu-id="b0f50-103">Propiedad Qualifier. NombreOrganización</span><span class="sxs-lookup"><span data-stu-id="b0f50-103">Qualifier.OrganizationName property</span></span>

<span data-ttu-id="b0f50-104">\[La propiedad **OrganizationName** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="b0f50-104">\[The **OrganizationName** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b0f50-105">En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para las directivas de certificado para procesar calificadores que formen parte de la información de directivas en la extensión de directivas de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="b0f50-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="b0f50-106">La propiedad **NombreDeOrganización** recupera el nombre de la organización asociada con el calificador.</span><span class="sxs-lookup"><span data-stu-id="b0f50-106">The **OrganizationName** property retrieves the name of the organization associated with the qualifier.</span></span> <span data-ttu-id="b0f50-107">Esta propiedad puede estar vacía.</span><span class="sxs-lookup"><span data-stu-id="b0f50-107">This property may be empty.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0f50-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0f50-108">Syntax</span></span>


```VB
Qualifier.OrganizationName As String
```



## <a name="property-value"></a><span data-ttu-id="b0f50-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b0f50-109">Property value</span></span>

<span data-ttu-id="b0f50-110">El nombre de la organización asociada con el calificador.</span><span class="sxs-lookup"><span data-stu-id="b0f50-110">The name of the organization associated with the qualifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0f50-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0f50-111">Requirements</span></span>



| <span data-ttu-id="b0f50-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0f50-112">Requirement</span></span> | <span data-ttu-id="b0f50-113">Value</span><span class="sxs-lookup"><span data-stu-id="b0f50-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0f50-114">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="b0f50-114">Redistributable</span></span><br/> | <span data-ttu-id="b0f50-115">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="b0f50-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b0f50-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b0f50-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="b0f50-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0f50-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0f50-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0f50-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0f50-119">**Qualifier**</span><span class="sxs-lookup"><span data-stu-id="b0f50-119">**Qualifier**</span></span>](qualifier.md)
</dt> </dl>

 

 
