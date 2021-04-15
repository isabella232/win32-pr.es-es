---
description: Establece o recupera el período de tiempo antes de que se determine una dirección URL como inaccesible.
ms.assetid: f39dafc4-6017-463c-aeee-948b6173862a
title: Propiedad CertificateStatus. UrlRetrievalTimeout
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.UrlRetrievalTimeout
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: fcaaafa1f2e870195b612eb225696f2c23a80ee1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689947"
---
# <a name="certificatestatusurlretrievaltimeout-property"></a><span data-ttu-id="f36ca-103">Propiedad CertificateStatus. UrlRetrievalTimeout</span><span class="sxs-lookup"><span data-stu-id="f36ca-103">CertificateStatus.UrlRetrievalTimeout property</span></span>

<span data-ttu-id="f36ca-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f36ca-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="f36ca-105">En su lugar, use la [**estructura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="f36ca-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="f36ca-106">La propiedad **UrlRetrievalTimeout** establece o recupera el período de tiempo antes de que se determine que una dirección URL no es accesible.</span><span class="sxs-lookup"><span data-stu-id="f36ca-106">The **UrlRetrievalTimeout** property sets or retrieves the length of time before a URL is determined to be unreachable.</span></span>

## <a name="syntax"></a><span data-ttu-id="f36ca-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f36ca-107">Syntax</span></span>


```VB
CertificateStatus.UrlRetrievalTimeout As Long
```



## <a name="property-value"></a><span data-ttu-id="f36ca-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f36ca-108">Property value</span></span>

<span data-ttu-id="f36ca-109">El número de segundos antes de que se determine una dirección URL como inaccesible.</span><span class="sxs-lookup"><span data-stu-id="f36ca-109">The number of seconds before a URL is determined to be unreachable.</span></span>

## <a name="remarks"></a><span data-ttu-id="f36ca-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f36ca-110">Remarks</span></span>

<span data-ttu-id="f36ca-111">Si no se establece esta propiedad, el tiempo de espera predeterminado es de 15 segundos.</span><span class="sxs-lookup"><span data-stu-id="f36ca-111">If this property is not set, the default time-out is 15 seconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="f36ca-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f36ca-112">Requirements</span></span>



| <span data-ttu-id="f36ca-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f36ca-113">Requirement</span></span> | <span data-ttu-id="f36ca-114">Value</span><span class="sxs-lookup"><span data-stu-id="f36ca-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f36ca-115">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="f36ca-115">End of client support</span></span><br/> | <span data-ttu-id="f36ca-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f36ca-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f36ca-117">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="f36ca-117">End of server support</span></span><br/> | <span data-ttu-id="f36ca-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f36ca-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f36ca-119">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="f36ca-119">Redistributable</span></span><br/>       | <span data-ttu-id="f36ca-120">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="f36ca-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f36ca-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f36ca-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="f36ca-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f36ca-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
