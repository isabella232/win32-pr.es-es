---
description: Devuelve un objeto KeyUsage que indica el uso de clave válido del certificado.
ms.assetid: e4590e95-ffa2-4953-bfc1-4d7c70271029
title: 'ICertificate2:: KeyUsage (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.KeyUsage
- ICertificate2.KeyUsage
- ICertificate.KeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 85fe008880d9613586d38dba7afaca39bb29f72f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671664"
---
# <a name="icertificate2keyusage-method"></a><span data-ttu-id="014a6-103">ICertificate2:: KeyUsage (método)</span><span class="sxs-lookup"><span data-stu-id="014a6-103">ICertificate2::KeyUsage method</span></span>

<span data-ttu-id="014a6-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="014a6-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="014a6-105">En su lugar, use la [**clase X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="014a6-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="014a6-106">El método **KeyUsage** devuelve un objeto [**KeyUsage**](keyusage.md) que indica el uso de clave válido del certificado.</span><span class="sxs-lookup"><span data-stu-id="014a6-106">The **KeyUsage** method returns a [**KeyUsage**](keyusage.md) object that indicates the valid key usage of the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="014a6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="014a6-107">Syntax</span></span>


```VB
Certificate.KeyUsage()
```



## <a name="parameters"></a><span data-ttu-id="014a6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="014a6-108">Parameters</span></span>

<span data-ttu-id="014a6-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="014a6-109">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="014a6-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="014a6-110">Requirements</span></span>



| <span data-ttu-id="014a6-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="014a6-111">Requirement</span></span> | <span data-ttu-id="014a6-112">Value</span><span class="sxs-lookup"><span data-stu-id="014a6-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="014a6-113">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="014a6-113">End of client support</span></span><br/> | <span data-ttu-id="014a6-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="014a6-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="014a6-115">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="014a6-115">End of server support</span></span><br/> | <span data-ttu-id="014a6-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="014a6-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="014a6-117">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="014a6-117">Redistributable</span></span><br/>       | <span data-ttu-id="014a6-118">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="014a6-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="014a6-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="014a6-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="014a6-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="014a6-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="014a6-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="014a6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="014a6-122">Objetos de criptografía</span><span class="sxs-lookup"><span data-stu-id="014a6-122">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="014a6-123">**Certificado**</span><span class="sxs-lookup"><span data-stu-id="014a6-123">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
