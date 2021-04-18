---
description: Determina si el certificado tiene una clave privada asociada. El método determina esto comprobando si \_ \_ \_ \_ \_ está presente la propiedad del ID. de prop de la clave del certificado.
ms.assetid: 80478956-1ed7-4c25-9ae3-d7176649e6d7
title: 'ICertificate2:: HasPrivateKey (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.HasPrivateKey
- ICertificate2.HasPrivateKey
- ICertificate.HasPrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 43110e48a1172977ad979d6ec2d94c5b8e3ffc50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670448"
---
# <a name="icertificate2hasprivatekey-method"></a><span data-ttu-id="f445b-104">ICertificate2:: HasPrivateKey (método)</span><span class="sxs-lookup"><span data-stu-id="f445b-104">ICertificate2::HasPrivateKey method</span></span>

<span data-ttu-id="f445b-105">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f445b-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="f445b-106">En su lugar, use la [**clase X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="f445b-106">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="f445b-107">El método **HasPrivateKey** determina si el [*certificado*](../secgloss/c-gly.md) tiene una [*clave privada*](../secgloss/p-gly.md) asociada.</span><span class="sxs-lookup"><span data-stu-id="f445b-107">The **HasPrivateKey** method determines whether the [*certificate*](../secgloss/c-gly.md) has a [*private key*](../secgloss/p-gly.md) associated with it.</span></span> <span data-ttu-id="f445b-108">El método determina esto comprobando si \_ \_ \_ \_ \_ está presente la propiedad del ID. de prop de la clave del certificado.</span><span class="sxs-lookup"><span data-stu-id="f445b-108">The method determines this by checking whether the CERT\_KEY\_PROV\_INFO\_PROP\_ID property is present.</span></span>

## <a name="syntax"></a><span data-ttu-id="f445b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f445b-109">Syntax</span></span>


```VB
Certificate.HasPrivateKey()
```



## <a name="parameters"></a><span data-ttu-id="f445b-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f445b-110">Parameters</span></span>

<span data-ttu-id="f445b-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f445b-111">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="f445b-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f445b-112">Requirements</span></span>



| <span data-ttu-id="f445b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f445b-113">Requirement</span></span> | <span data-ttu-id="f445b-114">Value</span><span class="sxs-lookup"><span data-stu-id="f445b-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f445b-115">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="f445b-115">End of client support</span></span><br/> | <span data-ttu-id="f445b-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f445b-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f445b-117">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="f445b-117">End of server support</span></span><br/> | <span data-ttu-id="f445b-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f445b-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f445b-119">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="f445b-119">Redistributable</span></span><br/>       | <span data-ttu-id="f445b-120">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="f445b-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f445b-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f445b-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="f445b-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f445b-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f445b-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="f445b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f445b-124">**PrivateKey. Open**</span><span class="sxs-lookup"><span data-stu-id="f445b-124">**PrivateKey.Open**</span></span>](privatekey-open.md)
</dt> <dt>

[<span data-ttu-id="f445b-125">Objetos de criptografía</span><span class="sxs-lookup"><span data-stu-id="f445b-125">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="f445b-126">**Certificado**</span><span class="sxs-lookup"><span data-stu-id="f445b-126">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
