---
description: Recupera el identificador de objeto del calificador.
ms.assetid: 58ec2af7-f085-43bc-8ea8-926cb840abe9
title: Propiedad Qualifier. OID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a86aaf7b60b98811e2d1fbef79c520448f1d47f3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690506"
---
# <a name="qualifieroid-property"></a><span data-ttu-id="5e000-103">Propiedad Qualifier. OID</span><span class="sxs-lookup"><span data-stu-id="5e000-103">Qualifier.OID property</span></span>

<span data-ttu-id="5e000-104">\[La propiedad **OID** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="5e000-104">\[The **OID** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5e000-105">En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para las directivas de certificado para procesar calificadores que formen parte de la información de directivas en la extensión de directivas de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="5e000-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="5e000-106">La propiedad **OID** recupera el ID. de objeto del calificador.</span><span class="sxs-lookup"><span data-stu-id="5e000-106">The **OID** property retrieves the object ID of the qualifier.</span></span> <span data-ttu-id="5e000-107">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5e000-107">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e000-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e000-108">Syntax</span></span>


```VB
Qualifier.OID As OID
```



## <a name="property-value"></a><span data-ttu-id="5e000-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="5e000-109">Property value</span></span>

<span data-ttu-id="5e000-110">Objeto [**OID**](oid.md) que identifica el calificador.</span><span class="sxs-lookup"><span data-stu-id="5e000-110">An [**OID**](oid.md) object that identifies the qualifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e000-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e000-111">Requirements</span></span>



| <span data-ttu-id="5e000-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e000-112">Requirement</span></span> | <span data-ttu-id="5e000-113">Value</span><span class="sxs-lookup"><span data-stu-id="5e000-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e000-114">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="5e000-114">Redistributable</span></span><br/> | <span data-ttu-id="5e000-115">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="5e000-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5e000-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5e000-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="5e000-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e000-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e000-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e000-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e000-119">**Qualifier**</span><span class="sxs-lookup"><span data-stu-id="5e000-119">**Qualifier**</span></span>](qualifier.md)
</dt> </dl>

 

 
