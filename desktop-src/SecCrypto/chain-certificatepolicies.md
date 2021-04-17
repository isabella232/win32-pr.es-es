---
description: Devuelve una colección de OID que representa los OID de directiva de certificado válidos para la cadena.
ms.assetid: 18200003-f4f1-4cf3-af9a-bc223151ff68
title: 'IChain2:: CertificatePolicies (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.CertificatePolicies
- IChain2.CertificatePolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e37abce9ea1aec5eb8adaf1d8eceeb3fac284fa3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689924"
---
# <a name="ichain2certificatepolicies-method"></a><span data-ttu-id="96e44-103">IChain2:: CertificatePolicies (método)</span><span class="sxs-lookup"><span data-stu-id="96e44-103">IChain2::CertificatePolicies method</span></span>

<span data-ttu-id="96e44-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="96e44-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="96e44-105">En su lugar, use la [**clase X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="96e44-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="96e44-106">El método **CertificatePolicies** devuelve una colección [**OID**](oids.md) que representa los OID de directiva de certificado válidos para la cadena.</span><span class="sxs-lookup"><span data-stu-id="96e44-106">The **CertificatePolicies** method returns an [**OIDs**](oids.md) collection that represents the certificate policy OIDs valid for the chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="96e44-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="96e44-107">Syntax</span></span>


```VB
Chain.CertificatePolicies()
```



## <a name="parameters"></a><span data-ttu-id="96e44-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="96e44-108">Parameters</span></span>

<span data-ttu-id="96e44-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="96e44-109">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="96e44-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96e44-110">Requirements</span></span>



| <span data-ttu-id="96e44-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="96e44-111">Requirement</span></span> | <span data-ttu-id="96e44-112">Value</span><span class="sxs-lookup"><span data-stu-id="96e44-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="96e44-113">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="96e44-113">End of client support</span></span><br/> | <span data-ttu-id="96e44-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="96e44-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="96e44-115">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="96e44-115">End of server support</span></span><br/> | <span data-ttu-id="96e44-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="96e44-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="96e44-117">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="96e44-117">Redistributable</span></span><br/>       | <span data-ttu-id="96e44-118">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="96e44-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="96e44-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="96e44-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="96e44-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96e44-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
