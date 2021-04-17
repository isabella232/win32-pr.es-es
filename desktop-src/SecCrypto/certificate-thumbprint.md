---
description: Recupera una cadena hexadecimal que contiene el hash SHA-1 del certificado.
ms.assetid: 6fd6f3ba-f7a9-43a3-a8da-8fd826649a92
title: Propiedad Certificate. Thumbprint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Thumbprint
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c576c46ecf669d215c5bd20a80a0e5a65e3d4706
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690034"
---
# <a name="certificatethumbprint-property"></a><span data-ttu-id="4e466-103">Propiedad Certificate. Thumbprint</span><span class="sxs-lookup"><span data-stu-id="4e466-103">Certificate.Thumbprint property</span></span>

<span data-ttu-id="4e466-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4e466-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="4e466-105">En su lugar, use la [**clase X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="4e466-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="4e466-106">La propiedad **huella digital** recupera una cadena hexadecimal que contiene el hash [*SHA-1*](../secgloss/s-gly.md) del certificado.</span><span class="sxs-lookup"><span data-stu-id="4e466-106">The **Thumbprint** property retrieves a hexadecimal string that contains the [*SHA-1*](../secgloss/s-gly.md) hash of the certificate.</span></span>

<span data-ttu-id="4e466-107">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4e466-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e466-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e466-108">Syntax</span></span>


```VB
Certificate.Thumbprint As String
```



## <a name="property-value"></a><span data-ttu-id="4e466-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="4e466-109">Property value</span></span>

<span data-ttu-id="4e466-110">Cadena hexadecimal que contiene el hash SHA-1 del certificado.</span><span class="sxs-lookup"><span data-stu-id="4e466-110">A hexadecimal string that contains the SHA-1 hash of the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e466-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e466-111">Requirements</span></span>



| <span data-ttu-id="4e466-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e466-112">Requirement</span></span> | <span data-ttu-id="4e466-113">Value</span><span class="sxs-lookup"><span data-stu-id="4e466-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e466-114">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="4e466-114">End of client support</span></span><br/> | <span data-ttu-id="4e466-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4e466-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4e466-116">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="4e466-116">End of server support</span></span><br/> | <span data-ttu-id="4e466-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e466-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4e466-118">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="4e466-118">Redistributable</span></span><br/>       | <span data-ttu-id="4e466-119">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="4e466-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4e466-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4e466-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="4e466-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e466-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e466-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e466-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e466-123">**Certificado**</span><span class="sxs-lookup"><span data-stu-id="4e466-123">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
