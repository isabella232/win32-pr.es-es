---
description: Devuelve un objeto ExtendedKeyUsage que indica los usos válidos del certificado.
ms.assetid: e974e9e2-1011-48b7-9ebc-e754e4990286
title: 'ICertificate2:: ExtendedKeyUsage (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.ExtendedKeyUsage
- ICertificate2.ExtendedKeyUsage
- ICertificate.ExtendedKeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6f349b7267d58a9376b9295e3ffd5013954a0872
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670827"
---
# <a name="icertificate2extendedkeyusage-method"></a><span data-ttu-id="83230-103">ICertificate2:: ExtendedKeyUsage (método)</span><span class="sxs-lookup"><span data-stu-id="83230-103">ICertificate2::ExtendedKeyUsage method</span></span>

<span data-ttu-id="83230-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="83230-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="83230-105">En su lugar, use la [**clase X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="83230-105">Instead, use the [**X509Certificate2 Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="83230-106">El método **ExtendedKeyUsage** devuelve un objeto [**ExtendedKeyUsage**](extendedkeyusage.md) que indica los usos válidos del certificado.</span><span class="sxs-lookup"><span data-stu-id="83230-106">The **ExtendedKeyUsage** method returns an [**ExtendedKeyUsage**](extendedkeyusage.md) object that indicates the valid uses of the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="83230-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="83230-107">Syntax</span></span>


```VB
Certificate.ExtendedKeyUsage()
```



## <a name="parameters"></a><span data-ttu-id="83230-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="83230-108">Parameters</span></span>

<span data-ttu-id="83230-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="83230-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="83230-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="83230-110">Return value</span></span>

<span data-ttu-id="83230-111">Objeto [**ExtendedKeyUsage**](extendedkeyusage.md) asociado al certificado.</span><span class="sxs-lookup"><span data-stu-id="83230-111">The [**ExtendedKeyUsage**](extendedkeyusage.md) object that is associated with the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="83230-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83230-112">Requirements</span></span>



| <span data-ttu-id="83230-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="83230-113">Requirement</span></span> | <span data-ttu-id="83230-114">Value</span><span class="sxs-lookup"><span data-stu-id="83230-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="83230-115">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="83230-115">End of client support</span></span><br/> | <span data-ttu-id="83230-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="83230-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="83230-117">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="83230-117">End of server support</span></span><br/> | <span data-ttu-id="83230-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83230-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="83230-119">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="83230-119">Redistributable</span></span><br/>       | <span data-ttu-id="83230-120">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="83230-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="83230-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="83230-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="83230-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83230-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83230-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="83230-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83230-124">Objetos de criptografía</span><span class="sxs-lookup"><span data-stu-id="83230-124">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="83230-125">**Certificado**</span><span class="sxs-lookup"><span data-stu-id="83230-125">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
