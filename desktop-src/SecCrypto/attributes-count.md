---
description: Recupera el número de objetos de atributo de la colección.
ms.assetid: d5f9db7d-52a2-4feb-8d35-902caf536510
title: Propiedad Attributes. Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 34a750b34f483342966ed1fcb3831d08b8df8f39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671028"
---
# <a name="attributescount-property"></a><span data-ttu-id="90319-103">Propiedad Attributes. Count</span><span class="sxs-lookup"><span data-stu-id="90319-103">Attributes.Count property</span></span>

<span data-ttu-id="90319-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="90319-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="90319-105">En su lugar, use la [**clase CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="90319-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="90319-106">La propiedad **Count** recupera el número de objetos de [**atributo**](attribute.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="90319-106">The **Count** property retrieves the number of [**Attribute**](attribute.md) objects in the collection.</span></span>

<span data-ttu-id="90319-107">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="90319-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="90319-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="90319-108">Syntax</span></span>


```VB
Attributes.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="90319-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="90319-109">Property value</span></span>

<span data-ttu-id="90319-110">Número de objetos de [**atributo**](attribute.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="90319-110">The number of [**Attribute**](attribute.md) objects in the collection.</span></span> <span data-ttu-id="90319-111">Cada objeto de **atributo** representa un atributo único en la colección.</span><span class="sxs-lookup"><span data-stu-id="90319-111">Each **Attribute** object represents a single attribute in the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="90319-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="90319-112">Remarks</span></span>

<span data-ttu-id="90319-113">La propiedad **Count** se puede usar para especificar el último objeto de [**atributo**](attribute.md) de la colección al recuperar un objeto de **atributo** concreto mediante la propiedad [**Attributes. Item**](attributes-item.md) .</span><span class="sxs-lookup"><span data-stu-id="90319-113">The **Count** property can be used to specify the last [**Attribute**](attribute.md) object in the collection when retrieving a specific **Attribute** object by using the [**Attributes.Item**](attributes-item.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="90319-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90319-114">Requirements</span></span>



| <span data-ttu-id="90319-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="90319-115">Requirement</span></span> | <span data-ttu-id="90319-116">Value</span><span class="sxs-lookup"><span data-stu-id="90319-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="90319-117">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="90319-117">End of client support</span></span><br/> | <span data-ttu-id="90319-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="90319-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="90319-119">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="90319-119">End of server support</span></span><br/> | <span data-ttu-id="90319-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="90319-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="90319-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="90319-121">Redistributable</span></span><br/>       | <span data-ttu-id="90319-122">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="90319-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="90319-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="90319-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="90319-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90319-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90319-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="90319-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90319-126">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="90319-126">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 
