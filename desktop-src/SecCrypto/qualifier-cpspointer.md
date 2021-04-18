---
description: Recupera el URI que señala a una declaración de prácticas de certificación (CPS) publicada por la entidad de certificación (CA).
ms.assetid: fd030c1c-137c-4036-bf13-ae989a9703cc
title: Propiedad Qualifier. CPSPointer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.CPSPointer
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: db16e8faa25fc929e884358fcd885943adc17e32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650033"
---
# <a name="qualifiercpspointer-property"></a><span data-ttu-id="dbf79-103">Propiedad Qualifier. CPSPointer</span><span class="sxs-lookup"><span data-stu-id="dbf79-103">Qualifier.CPSPointer property</span></span>

<span data-ttu-id="dbf79-104">\[La propiedad **CPSPointer** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="dbf79-104">\[The **CPSPointer** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="dbf79-105">En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para las directivas de certificado para procesar calificadores que formen parte de la información de directivas en la extensión de directivas de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="dbf79-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="dbf79-106">La propiedad **CPSPointer** recupera el URI que señala a una declaración de prácticas de certificación (CPS) publicada por la entidad de certificación (CA).</span><span class="sxs-lookup"><span data-stu-id="dbf79-106">The **CPSPointer** property retrieves the URI that points to a Certification Practice Statement (CPS) published by the certification authority (CA).</span></span>

## <a name="syntax"></a><span data-ttu-id="dbf79-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dbf79-107">Syntax</span></span>


```VB
Qualifier.CPSPointer As String
```



## <a name="property-value"></a><span data-ttu-id="dbf79-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="dbf79-108">Property value</span></span>

<span data-ttu-id="dbf79-109">El URI que apunta a una CPS publicada por la CA.</span><span class="sxs-lookup"><span data-stu-id="dbf79-109">The URI that points to a CPS published by the CA.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbf79-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbf79-110">Requirements</span></span>



| <span data-ttu-id="dbf79-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbf79-111">Requirement</span></span> | <span data-ttu-id="dbf79-112">Value</span><span class="sxs-lookup"><span data-stu-id="dbf79-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbf79-113">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="dbf79-113">Redistributable</span></span><br/> | <span data-ttu-id="dbf79-114">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="dbf79-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="dbf79-115">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dbf79-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="dbf79-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbf79-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbf79-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="dbf79-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbf79-118">**Qualifier**</span><span class="sxs-lookup"><span data-stu-id="dbf79-118">**Qualifier**</span></span>](qualifier.md)
</dt> </dl>

 

 
