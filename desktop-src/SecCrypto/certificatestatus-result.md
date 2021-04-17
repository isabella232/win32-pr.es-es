---
description: La propiedad resultado recupera un valor que indica si el certificado es válido. Esta es la propiedad predeterminada.
ms.assetid: b1edfbde-9d54-4e9c-ba9b-33e4c354c23f
title: CertificateStatus. Result (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.Result
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: df13e9a9fb0454d30ce855b3d272fa521e96e0f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670333"
---
# <a name="certificatestatusresult-property"></a><span data-ttu-id="afbcd-104">CertificateStatus. Result (propiedad)</span><span class="sxs-lookup"><span data-stu-id="afbcd-104">CertificateStatus.Result property</span></span>

<span data-ttu-id="afbcd-105">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="afbcd-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="afbcd-106">En su lugar, use la [**estructura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="afbcd-106">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="afbcd-107">La propiedad **resultado** recupera un valor que indica si el certificado es válido.</span><span class="sxs-lookup"><span data-stu-id="afbcd-107">The **Result** property retrieves a value that indicates whether the certificate is valid.</span></span> <span data-ttu-id="afbcd-108">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="afbcd-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="afbcd-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="afbcd-109">Syntax</span></span>


```VB
CertificateStatus.Result As Boolean
```



## <a name="property-value"></a><span data-ttu-id="afbcd-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="afbcd-110">Property value</span></span>

<span data-ttu-id="afbcd-111">Si es **true**, el certificado es válido.</span><span class="sxs-lookup"><span data-stu-id="afbcd-111">If **true**, the certificate is valid.</span></span> <span data-ttu-id="afbcd-112">La validez del certificado se comprueba con la configuración actual de la propiedad [**CheckFlag**](certificatestatus-checkflag.md) y de las distintas configuraciones de directiva.</span><span class="sxs-lookup"><span data-stu-id="afbcd-112">The certificate's validity is checked using the current setting of the [**CheckFlag**](certificatestatus-checkflag.md) property and the various policy settings.</span></span>

## <a name="requirements"></a><span data-ttu-id="afbcd-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="afbcd-113">Requirements</span></span>



| <span data-ttu-id="afbcd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="afbcd-114">Requirement</span></span> | <span data-ttu-id="afbcd-115">Value</span><span class="sxs-lookup"><span data-stu-id="afbcd-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="afbcd-116">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="afbcd-116">End of client support</span></span><br/> | <span data-ttu-id="afbcd-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="afbcd-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="afbcd-118">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="afbcd-118">End of server support</span></span><br/> | <span data-ttu-id="afbcd-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="afbcd-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="afbcd-120">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="afbcd-120">Redistributable</span></span><br/>       | <span data-ttu-id="afbcd-121">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="afbcd-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="afbcd-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="afbcd-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="afbcd-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afbcd-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
