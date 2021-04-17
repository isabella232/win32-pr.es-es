---
description: Crea una cadena de comprobación de certificados para un certificado y devuelve un objeto CertificateStatus que contiene el estado de validez del certificado.
ms.assetid: 4463e4ac-60a5-4845-93b3-35d2f83bd86e
title: 'ICertificate2:: IsValid (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.IsValid
- ICertificate2.IsValid
- ICertificate.IsValid
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 39fec7c1bd2b369ee512834ed1b58b59871d8ae5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670485"
---
# <a name="icertificate2isvalid-method"></a><span data-ttu-id="b79be-103">ICertificate2:: IsValid (método)</span><span class="sxs-lookup"><span data-stu-id="b79be-103">ICertificate2::IsValid method</span></span>

<span data-ttu-id="b79be-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b79be-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="b79be-105">En su lugar, use la [**clase X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="b79be-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="b79be-106">El método **IsValid** crea una cadena de comprobación de certificados para un certificado y devuelve un objeto [**CertificateStatus**](certificatestatus.md) que contiene el estado de validez del certificado.</span><span class="sxs-lookup"><span data-stu-id="b79be-106">The **IsValid** method builds a certificate verification chain for a certificate and returns a [**CertificateStatus**](certificatestatus.md) object that contains the validity status of the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="b79be-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b79be-107">Syntax</span></span>


```VB
Certificate.IsValid()
```



## <a name="parameters"></a><span data-ttu-id="b79be-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b79be-108">Parameters</span></span>

<span data-ttu-id="b79be-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="b79be-109">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="b79be-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b79be-110">Requirements</span></span>



| <span data-ttu-id="b79be-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="b79be-111">Requirement</span></span> | <span data-ttu-id="b79be-112">Value</span><span class="sxs-lookup"><span data-stu-id="b79be-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b79be-113">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="b79be-113">End of client support</span></span><br/> | <span data-ttu-id="b79be-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b79be-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b79be-115">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="b79be-115">End of server support</span></span><br/> | <span data-ttu-id="b79be-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b79be-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b79be-117">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="b79be-117">Redistributable</span></span><br/>       | <span data-ttu-id="b79be-118">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="b79be-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b79be-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b79be-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="b79be-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b79be-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b79be-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="b79be-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b79be-122">Objetos de criptografía</span><span class="sxs-lookup"><span data-stu-id="b79be-122">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="b79be-123">**Certificado**</span><span class="sxs-lookup"><span data-stu-id="b79be-123">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
