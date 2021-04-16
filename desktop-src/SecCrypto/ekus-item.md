---
description: Recupera el objeto EKU que representa la propiedad de uso mejorado de clave (EKU) indizada.
ms.assetid: b8c12a7a-e836-48c2-958c-937b3723f85b
title: 'IEKUs:: Item (propiedad)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKUs.Item
- IEKUs.get_Item
- EKUs.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e3eaf8d0b303207aae3ef78cc82771e1436b1027
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649993"
---
# <a name="iekusitem-property"></a><span data-ttu-id="ba0e3-103">IEKUs:: Item (propiedad)</span><span class="sxs-lookup"><span data-stu-id="ba0e3-103">IEKUs::Item property</span></span>

<span data-ttu-id="ba0e3-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ba0e3-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="ba0e3-105">En su lugar, use la [**clase X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="ba0e3-105">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="ba0e3-106">La propiedad **Item** recupera el objeto [**EKU**](eku.md) que representa la propiedad de uso mejorado de clave (EKU) indizada.</span><span class="sxs-lookup"><span data-stu-id="ba0e3-106">The **Item** property retrieves the [**EKU**](eku.md) object that represents the indexed extended key usage (EKU) property.</span></span>

<span data-ttu-id="ba0e3-107">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ba0e3-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba0e3-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ba0e3-108">Syntax</span></span>


```VB
EKUs.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="ba0e3-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ba0e3-109">Property value</span></span>

<span data-ttu-id="ba0e3-110">Objeto [**EKU**](eku.md) que representa la propiedad de uso mejorado de clave (EKU) indizada.</span><span class="sxs-lookup"><span data-stu-id="ba0e3-110">An [**EKU**](eku.md) object that represents the indexed extended key usage (EKU) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba0e3-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba0e3-111">Requirements</span></span>



| <span data-ttu-id="ba0e3-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba0e3-112">Requirement</span></span> | <span data-ttu-id="ba0e3-113">Value</span><span class="sxs-lookup"><span data-stu-id="ba0e3-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba0e3-114">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="ba0e3-114">End of client support</span></span><br/> | <span data-ttu-id="ba0e3-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ba0e3-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ba0e3-116">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="ba0e3-116">End of server support</span></span><br/> | <span data-ttu-id="ba0e3-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba0e3-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ba0e3-118">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="ba0e3-118">Redistributable</span></span><br/>       | <span data-ttu-id="ba0e3-119">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="ba0e3-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ba0e3-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ba0e3-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="ba0e3-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba0e3-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba0e3-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba0e3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba0e3-123">**EKU**</span><span class="sxs-lookup"><span data-stu-id="ba0e3-123">**EKUs**</span></span>](ekus.md)
</dt> </dl>

 

 
