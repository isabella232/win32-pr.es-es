---
description: Recupera un objeto de certificado que representa el certificado indizado de la colección. Esta es la propiedad predeterminada.
ms.assetid: 733f2b93-c059-4041-b7cd-8c20218f1462
title: Certificates. Item (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: bbafaf20f74910e8ea5eb525f48374a2807fa030
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690959"
---
# <a name="certificatesitem-property"></a><span data-ttu-id="a76bb-104">Certificates. Item (propiedad)</span><span class="sxs-lookup"><span data-stu-id="a76bb-104">Certificates.Item property</span></span>

<span data-ttu-id="a76bb-105">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a76bb-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="a76bb-106">En su lugar, use la [**clase X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="a76bb-106">Instead, use the [**X509Certificate2Collection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="a76bb-107">La propiedad **Item** recupera un objeto de [**certificado**](certificate.md) que representa el certificado indizado de la colección.</span><span class="sxs-lookup"><span data-stu-id="a76bb-107">The **Item** property retrieves a [**Certificate**](certificate.md) object that represents the indexed certificate of the collection.</span></span> <span data-ttu-id="a76bb-108">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a76bb-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="a76bb-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a76bb-109">Syntax</span></span>


```VB
Certificates.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="a76bb-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a76bb-110">Property value</span></span>

<span data-ttu-id="a76bb-111">Objeto de [**certificado**](certificate.md) que representa el certificado indizado.</span><span class="sxs-lookup"><span data-stu-id="a76bb-111">A [**Certificate**](certificate.md) object that represents the indexed certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="a76bb-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a76bb-112">Requirements</span></span>



| <span data-ttu-id="a76bb-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a76bb-113">Requirement</span></span> | <span data-ttu-id="a76bb-114">Value</span><span class="sxs-lookup"><span data-stu-id="a76bb-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a76bb-115">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="a76bb-115">End of client support</span></span><br/> | <span data-ttu-id="a76bb-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a76bb-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a76bb-117">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="a76bb-117">End of server support</span></span><br/> | <span data-ttu-id="a76bb-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a76bb-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a76bb-119">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="a76bb-119">Redistributable</span></span><br/>       | <span data-ttu-id="a76bb-120">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="a76bb-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a76bb-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a76bb-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a76bb-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a76bb-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a76bb-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="a76bb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a76bb-124">**Certificados**</span><span class="sxs-lookup"><span data-stu-id="a76bb-124">**Certificates**</span></span>](certificates.md)
</dt> </dl>

 

 
