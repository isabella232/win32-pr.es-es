---
description: Recupera el número de objetos de certificado de la colección.
ms.assetid: 95931721-3b0c-4915-805f-039d1d5510fa
title: Certificates. Count (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a67554530ce8c8dfdc1bfcfba1198cf778397ac2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690447"
---
# <a name="certificatescount-property"></a><span data-ttu-id="7c7ab-103">Certificates. Count (propiedad)</span><span class="sxs-lookup"><span data-stu-id="7c7ab-103">Certificates.Count property</span></span>

<span data-ttu-id="7c7ab-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7c7ab-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="7c7ab-105">En su lugar, use la [**clase X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="7c7ab-105">Instead, use the [**X509Certificate2Collection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="7c7ab-106">La propiedad **Count** recupera el número de objetos de [**certificado**](certificate.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="7c7ab-106">The **Count** property retrieves the number of [**Certificate**](certificate.md) objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c7ab-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7c7ab-107">Syntax</span></span>


```VB
Certificates.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="7c7ab-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="7c7ab-108">Property value</span></span>

<span data-ttu-id="7c7ab-109">Número de objetos de [**certificado**](certificate.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="7c7ab-109">The number of [**Certificate**](certificate.md) objects in the collection.</span></span> <span data-ttu-id="7c7ab-110">Cada objeto de **certificado** representa un único certificado de la colección.</span><span class="sxs-lookup"><span data-stu-id="7c7ab-110">Each **Certificate** object represents a single certificate in the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c7ab-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c7ab-111">Remarks</span></span>

<span data-ttu-id="7c7ab-112">CAPICOM solo admite un único certificado para el almacén de [*tarjetas inteligentes*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="7c7ab-112">CAPICOM only supports a single certificate for the [*smart card*](../secgloss/s-gly.md) store.</span></span> <span data-ttu-id="7c7ab-113">Aunque el almacén de tarjetas inteligentes contenga más de un certificado, esta propiedad contendrá 1.</span><span class="sxs-lookup"><span data-stu-id="7c7ab-113">Even if the smart card store contains more than one certificate, this property will contain 1.</span></span> <span data-ttu-id="7c7ab-114">Para obtener más información acerca del almacén de tarjetas inteligentes, consulte el miembro del **\_ almacén de \_ \_ usuarios \_ de tarjetas inteligentes CAPICOM** de la enumeración de la [**Ubicación del \_ almacén \_ de CAPICOM**](capicom-store-location.md) .</span><span class="sxs-lookup"><span data-stu-id="7c7ab-114">For more information about the smart card store, see the **CAPICOM\_SMART\_CARD\_USER\_STORE** member of the [**CAPICOM\_STORE\_LOCATION**](capicom-store-location.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c7ab-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c7ab-115">Requirements</span></span>



| <span data-ttu-id="7c7ab-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c7ab-116">Requirement</span></span> | <span data-ttu-id="7c7ab-117">Value</span><span class="sxs-lookup"><span data-stu-id="7c7ab-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c7ab-118">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="7c7ab-118">End of client support</span></span><br/> | <span data-ttu-id="7c7ab-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7c7ab-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7c7ab-120">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="7c7ab-120">End of server support</span></span><br/> | <span data-ttu-id="7c7ab-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c7ab-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7c7ab-122">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="7c7ab-122">Redistributable</span></span><br/>       | <span data-ttu-id="7c7ab-123">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="7c7ab-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7c7ab-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7c7ab-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7c7ab-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c7ab-125"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c7ab-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c7ab-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c7ab-127">**Certificados**</span><span class="sxs-lookup"><span data-stu-id="7c7ab-127">**Certificates**</span></span>](certificates.md)
</dt> </dl>

 

 
