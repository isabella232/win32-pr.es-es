---
description: Devuelve una colección de OID que representa las directivas de aplicación utilizadas para crear el objeto de cadena.
ms.assetid: dca0acbf-e369-4216-a4f6-44ed965011d0
title: CertificateStatus. ApplicationPolicies, método
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.ApplicationPolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b02503590a64c1c14e3f66dc5d07d9d61034bd60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690170"
---
# <a name="certificatestatusapplicationpolicies-method"></a><span data-ttu-id="7f0a5-103">CertificateStatus. ApplicationPolicies, método</span><span class="sxs-lookup"><span data-stu-id="7f0a5-103">CertificateStatus.ApplicationPolicies method</span></span>

<span data-ttu-id="7f0a5-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7f0a5-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="7f0a5-105">En su lugar, use la [**estructura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="7f0a5-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="7f0a5-106">El método **ApplicationPolicies** devuelve una colección de [**OID**](oids.md) que representa las directivas de aplicación utilizadas para crear el objeto de [**cadena**](chain.md) .</span><span class="sxs-lookup"><span data-stu-id="7f0a5-106">The **ApplicationPolicies** method returns an [**OIDs**](oids.md) collection that represents the application policies used to create the [**Chain**](chain.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f0a5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7f0a5-107">Syntax</span></span>


```VB
CertificateStatus.ApplicationPolicies()
```



## <a name="parameters"></a><span data-ttu-id="7f0a5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7f0a5-108">Parameters</span></span>

<span data-ttu-id="7f0a5-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="7f0a5-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7f0a5-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7f0a5-110">Return value</span></span>

<span data-ttu-id="7f0a5-111">Colección de [**OID**](oids.md) .</span><span class="sxs-lookup"><span data-stu-id="7f0a5-111">An [**OIDs**](oids.md) collection.</span></span> <span data-ttu-id="7f0a5-112">Cada objeto [**OID**](oid.md) de la colección representa un OID de directiva de aplicación.</span><span class="sxs-lookup"><span data-stu-id="7f0a5-112">Each [**OID**](oid.md) object in the collection represents an application policy OID.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f0a5-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7f0a5-113">Remarks</span></span>

<span data-ttu-id="7f0a5-114">Agregue OID de directiva de aplicación a la colección para especificar las directivas de aplicación que se deben usar para generar la cadena de confianza de certificados.</span><span class="sxs-lookup"><span data-stu-id="7f0a5-114">Add application policy OIDs to the collection to specify the application policies that should be used to build the certificate trust chain.</span></span> <span data-ttu-id="7f0a5-115">Si la colección contiene al menos un objeto [**OID**](oid.md) , se omite el objeto [**EKU**](eku.md) devuelto por el método [**CertificateStatus. EKU**](certificatestatus-eku.md) .</span><span class="sxs-lookup"><span data-stu-id="7f0a5-115">If the collection contains at least one [**OID**](oid.md) object, the [**EKU**](eku.md) object returned by the [**CertificateStatus.EKU**](certificatestatus-eku.md) method is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f0a5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f0a5-116">Requirements</span></span>



| <span data-ttu-id="7f0a5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f0a5-117">Requirement</span></span> | <span data-ttu-id="7f0a5-118">Value</span><span class="sxs-lookup"><span data-stu-id="7f0a5-118">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f0a5-119">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="7f0a5-119">End of client support</span></span><br/> | <span data-ttu-id="7f0a5-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7f0a5-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7f0a5-121">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="7f0a5-121">End of server support</span></span><br/> | <span data-ttu-id="7f0a5-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7f0a5-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7f0a5-123">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="7f0a5-123">Redistributable</span></span><br/>       | <span data-ttu-id="7f0a5-124">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="7f0a5-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7f0a5-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7f0a5-125">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7f0a5-126"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f0a5-126"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
