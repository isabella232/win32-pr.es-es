---
description: Devuelve una colección de OID que representa las directivas de certificado utilizadas para crear el objeto de cadena.
ms.assetid: 7fe7d3ea-28fc-4c0a-9b43-a97518ac65db
title: CertificateStatus. CertificatePolicies, método
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.CertificatePolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 98c9e22c0cad40252cc9eebebf9aa32dc4d89b65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670779"
---
# <a name="certificatestatuscertificatepolicies-method"></a><span data-ttu-id="69fbf-103">CertificateStatus. CertificatePolicies, método</span><span class="sxs-lookup"><span data-stu-id="69fbf-103">CertificateStatus.CertificatePolicies method</span></span>

<span data-ttu-id="69fbf-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="69fbf-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="69fbf-105">En su lugar, use la [**estructura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="69fbf-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="69fbf-106">El método **CertificatePolicies** devuelve una colección de [**OID**](oids.md) que representa las directivas de certificado utilizadas para crear el objeto de [**cadena**](chain.md) .</span><span class="sxs-lookup"><span data-stu-id="69fbf-106">The **CertificatePolicies** method returns an [**OIDs**](oids.md) collection that represents the certificate policies used to create the [**Chain**](chain.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="69fbf-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69fbf-107">Syntax</span></span>


```VB
CertificateStatus.CertificatePolicies()
```



## <a name="parameters"></a><span data-ttu-id="69fbf-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69fbf-108">Parameters</span></span>

<span data-ttu-id="69fbf-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="69fbf-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="69fbf-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69fbf-110">Return value</span></span>

<span data-ttu-id="69fbf-111">Colección de [**OID**](oids.md) .</span><span class="sxs-lookup"><span data-stu-id="69fbf-111">An [**OIDs**](oids.md) collection.</span></span> <span data-ttu-id="69fbf-112">Cada objeto [**OID**](oid.md) de la colección representa un OID de la Directiva de certificado.</span><span class="sxs-lookup"><span data-stu-id="69fbf-112">Each [**OID**](oid.md) object in the collection represents a certificate policy OID.</span></span>

## <a name="remarks"></a><span data-ttu-id="69fbf-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69fbf-113">Remarks</span></span>

<span data-ttu-id="69fbf-114">Agregue OID de directiva de certificados a la colección para especificar las directivas de certificado que se deben usar para generar la cadena de confianza de certificados.</span><span class="sxs-lookup"><span data-stu-id="69fbf-114">Add certificate policy OIDs to the collection to specify the certificate policies that should be used to build the certificate trust chain.</span></span>

## <a name="requirements"></a><span data-ttu-id="69fbf-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69fbf-115">Requirements</span></span>



| <span data-ttu-id="69fbf-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="69fbf-116">Requirement</span></span> | <span data-ttu-id="69fbf-117">Value</span><span class="sxs-lookup"><span data-stu-id="69fbf-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="69fbf-118">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="69fbf-118">End of client support</span></span><br/> | <span data-ttu-id="69fbf-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="69fbf-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="69fbf-120">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="69fbf-120">End of server support</span></span><br/> | <span data-ttu-id="69fbf-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69fbf-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="69fbf-122">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="69fbf-122">Redistributable</span></span><br/>       | <span data-ttu-id="69fbf-123">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="69fbf-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="69fbf-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="69fbf-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="69fbf-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69fbf-125"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
