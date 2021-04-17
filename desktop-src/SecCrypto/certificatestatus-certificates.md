---
description: Establece o recupera la colección de certificados que se puede utilizar para generar la cadena de certificados.
ms.assetid: cdf378f9-0d71-4dd9-93cc-85f09a51c5fc
title: Propiedad CertificateStatus. Certificates
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 325b5c45fc6ae626363de286a6e131f1782cb83f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670615"
---
# <a name="certificatestatuscertificates-property"></a><span data-ttu-id="dc4ab-103">Propiedad CertificateStatus. Certificates</span><span class="sxs-lookup"><span data-stu-id="dc4ab-103">CertificateStatus.Certificates property</span></span>

<span data-ttu-id="dc4ab-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="dc4ab-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="dc4ab-105">En su lugar, use la [**estructura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="dc4ab-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="dc4ab-106">La propiedad **Certificates** establece o recupera la colección de certificados que se puede utilizar para generar la cadena de certificados.</span><span class="sxs-lookup"><span data-stu-id="dc4ab-106">The **Certificates** property sets or retrieves the collection of certificates that can be used to build the certificate chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc4ab-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc4ab-107">Syntax</span></span>


```VB
CertificateStatus.Certificates As Certificates
```



## <a name="property-value"></a><span data-ttu-id="dc4ab-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="dc4ab-108">Property value</span></span>

<span data-ttu-id="dc4ab-109">Objeto de [**certificados**](certificates.md) que representa la colección de certificados que se puede utilizar para generar la cadena de certificados.</span><span class="sxs-lookup"><span data-stu-id="dc4ab-109">A [**Certificates**](certificates.md) object that represents the collection of certificates that can be used to build the certificate chain.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc4ab-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc4ab-110">Requirements</span></span>



| <span data-ttu-id="dc4ab-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc4ab-111">Requirement</span></span> | <span data-ttu-id="dc4ab-112">Value</span><span class="sxs-lookup"><span data-stu-id="dc4ab-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc4ab-113">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="dc4ab-113">End of client support</span></span><br/> | <span data-ttu-id="dc4ab-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dc4ab-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="dc4ab-115">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="dc4ab-115">End of server support</span></span><br/> | <span data-ttu-id="dc4ab-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc4ab-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="dc4ab-117">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="dc4ab-117">Redistributable</span></span><br/>       | <span data-ttu-id="dc4ab-118">CAPICOM 2,1 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="dc4ab-118">CAPICOM 2.1 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="dc4ab-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dc4ab-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="dc4ab-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc4ab-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
