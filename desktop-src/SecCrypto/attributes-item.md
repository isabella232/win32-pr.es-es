---
description: Recupera el objeto de atributo que representa el atributo indizado.
ms.assetid: 35c54c5f-f83f-40eb-b341-129c1aac6181
title: Attributes. Item (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 208e36fd8d4d7e3effc2c0f59b7db921fed76d79
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671027"
---
# <a name="attributesitem-property"></a><span data-ttu-id="a5033-103">Attributes. Item (propiedad)</span><span class="sxs-lookup"><span data-stu-id="a5033-103">Attributes.Item property</span></span>

<span data-ttu-id="a5033-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a5033-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="a5033-105">En su lugar, use la [**clase CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="a5033-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="a5033-106">La propiedad **Item** recupera el objeto de [**atributo**](attribute.md) que representa el atributo indizado.</span><span class="sxs-lookup"><span data-stu-id="a5033-106">The **Item** property retrieves the [**Attribute**](attribute.md) object that represents the indexed attribute.</span></span> <span data-ttu-id="a5033-107">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a5033-107">This is the default property.</span></span>

<span data-ttu-id="a5033-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a5033-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5033-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a5033-109">Syntax</span></span>


```VB
Attributes.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="a5033-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a5033-110">Property value</span></span>

<span data-ttu-id="a5033-111">Objeto de [**atributo**](attribute.md) que representa el atributo indizado.</span><span class="sxs-lookup"><span data-stu-id="a5033-111">An [**Attribute**](attribute.md) object that represents the indexed attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5033-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5033-112">Requirements</span></span>



| <span data-ttu-id="a5033-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5033-113">Requirement</span></span> | <span data-ttu-id="a5033-114">Value</span><span class="sxs-lookup"><span data-stu-id="a5033-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5033-115">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="a5033-115">End of client support</span></span><br/> | <span data-ttu-id="a5033-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a5033-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a5033-117">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="a5033-117">End of server support</span></span><br/> | <span data-ttu-id="a5033-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a5033-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a5033-119">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="a5033-119">Redistributable</span></span><br/>       | <span data-ttu-id="a5033-120">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="a5033-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a5033-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a5033-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a5033-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5033-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
