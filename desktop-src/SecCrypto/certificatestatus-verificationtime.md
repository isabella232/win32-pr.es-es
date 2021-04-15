---
description: Establece o recupera la hora a la que se ha comprobado el certificado.
ms.assetid: 1bd17df3-2fa1-4b99-ab00-659b4ad5fcd9
title: Propiedad CertificateStatus. VerificationTime
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.VerificationTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 178402861c9830efbea78a31081ae7e8b31800b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689944"
---
# <a name="certificatestatusverificationtime-property"></a><span data-ttu-id="5a931-103">Propiedad CertificateStatus. VerificationTime</span><span class="sxs-lookup"><span data-stu-id="5a931-103">CertificateStatus.VerificationTime property</span></span>

<span data-ttu-id="5a931-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5a931-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="5a931-105">En su lugar, use la [**estructura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="5a931-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="5a931-106">La propiedad **VerificationTime** establece o recupera la hora a la que se ha comprobado el certificado.</span><span class="sxs-lookup"><span data-stu-id="5a931-106">The **VerificationTime** property sets or retrieves the time that the certificate was verified.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a931-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5a931-107">Syntax</span></span>


```VB
CertificateStatus.VerificationTime As Date
```



## <a name="property-value"></a><span data-ttu-id="5a931-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="5a931-108">Property value</span></span>

<span data-ttu-id="5a931-109">La hora a la que se comprobó el certificado.</span><span class="sxs-lookup"><span data-stu-id="5a931-109">The time that the certificate was verified.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a931-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5a931-110">Remarks</span></span>

<span data-ttu-id="5a931-111">Si no se establece esta propiedad, se utiliza la hora actual.</span><span class="sxs-lookup"><span data-stu-id="5a931-111">If this property is not set, the current time is used.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a931-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a931-112">Requirements</span></span>



| <span data-ttu-id="5a931-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a931-113">Requirement</span></span> | <span data-ttu-id="5a931-114">Value</span><span class="sxs-lookup"><span data-stu-id="5a931-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a931-115">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="5a931-115">End of client support</span></span><br/> | <span data-ttu-id="5a931-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5a931-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="5a931-117">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="5a931-117">End of server support</span></span><br/> | <span data-ttu-id="5a931-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5a931-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="5a931-119">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="5a931-119">Redistributable</span></span><br/>       | <span data-ttu-id="5a931-120">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="5a931-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5a931-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5a931-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="5a931-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a931-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
