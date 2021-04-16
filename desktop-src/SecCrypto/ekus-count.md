---
description: Recupera el número de objetos EKU de la colección.
ms.assetid: a38ac480-4f9b-4d69-a7e6-fae4993fe2cf
title: EKU. Count (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKUs.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41e77f3803fa65db1573c6619ebf1265b7418924
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649994"
---
# <a name="ekuscount-property"></a><span data-ttu-id="0a01d-103">EKU. Count (propiedad)</span><span class="sxs-lookup"><span data-stu-id="0a01d-103">EKUs.Count property</span></span>

<span data-ttu-id="0a01d-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0a01d-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="0a01d-105">En su lugar, use la [**clase X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="0a01d-105">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="0a01d-106">La propiedad **Count** recupera el número de objetos [**EKU**](eku.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="0a01d-106">The **Count** property retrieves the number of [**EKU**](eku.md) objects in the collection.</span></span>

<span data-ttu-id="0a01d-107">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0a01d-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a01d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0a01d-108">Syntax</span></span>


```VB
EKUs.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="0a01d-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="0a01d-109">Property value</span></span>

<span data-ttu-id="0a01d-110">Número de objetos [**EKU**](eku.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="0a01d-110">The number of [**EKU**](eku.md) objects in the collection.</span></span> <span data-ttu-id="0a01d-111">Cada objeto **EKU** representa una única propiedad de uso de clave extendida (EKU) de un certificado.</span><span class="sxs-lookup"><span data-stu-id="0a01d-111">Each **EKU** object represents a single extended key usage (EKU) property of a certificate.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a01d-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0a01d-112">Remarks</span></span>

<span data-ttu-id="0a01d-113">La propiedad **Count** se puede usar para especificar el último objeto [**EKU**](eku.md) de una colección al recuperar un objeto **EKU** específico mediante la propiedad [**EKU. Item**](ekus-item.md) .</span><span class="sxs-lookup"><span data-stu-id="0a01d-113">The **Count** property can be used to specify the last [**EKU**](eku.md) object in a collection when retrieving a specific **EKU** object using the [**EKUs.Item**](ekus-item.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a01d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a01d-114">Requirements</span></span>



| <span data-ttu-id="0a01d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a01d-115">Requirement</span></span> | <span data-ttu-id="0a01d-116">Value</span><span class="sxs-lookup"><span data-stu-id="0a01d-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a01d-117">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="0a01d-117">End of client support</span></span><br/> | <span data-ttu-id="0a01d-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0a01d-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0a01d-119">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="0a01d-119">End of server support</span></span><br/> | <span data-ttu-id="0a01d-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0a01d-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0a01d-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="0a01d-121">Redistributable</span></span><br/>       | <span data-ttu-id="0a01d-122">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="0a01d-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0a01d-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0a01d-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="0a01d-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a01d-124"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
