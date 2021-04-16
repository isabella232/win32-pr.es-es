---
description: Establece o recupera el valor del atributo.
ms.assetid: aaf0c07c-756f-48c8-b4cd-def40f7cb1a3
title: Attribute. Value (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6b3d2f41c56fc47277bd71354279e75b423d0c0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671333"
---
# <a name="attributevalue-property"></a><span data-ttu-id="31d09-103">Attribute. Value (propiedad)</span><span class="sxs-lookup"><span data-stu-id="31d09-103">Attribute.Value property</span></span>

<span data-ttu-id="31d09-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="31d09-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="31d09-105">En su lugar, use la [**clase CryptographicAttributeObject**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="31d09-105">Instead, use the [**CryptographicAttributeObject Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="31d09-106">La propiedad **Value** establece o recupera el valor del atributo.</span><span class="sxs-lookup"><span data-stu-id="31d09-106">The **Value** property sets or retrieves the value of the attribute.</span></span>

<span data-ttu-id="31d09-107">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="31d09-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="31d09-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="31d09-108">Syntax</span></span>


```VB
Attribute.Value As Variant
```



## <a name="property-value"></a><span data-ttu-id="31d09-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="31d09-109">Property value</span></span>

<span data-ttu-id="31d09-110">Variable de **variante** que contiene el valor del atributo.</span><span class="sxs-lookup"><span data-stu-id="31d09-110">A **Variant** variable that contains the value of the attribute.</span></span> <span data-ttu-id="31d09-111">En el caso de los atributos de **tiempo de \_ \_ \_ firma \_ de atributo de CAPICOM** , el tipo de datos es **Date**.</span><span class="sxs-lookup"><span data-stu-id="31d09-111">For **CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_SIGNING\_TIME** attributes, the data type is **DATE**.</span></span> <span data-ttu-id="31d09-112">Para todos los demás atributos, el valor de la propiedad es una cadena.</span><span class="sxs-lookup"><span data-stu-id="31d09-112">For all other attributes, the property value is a string.</span></span>

## <a name="requirements"></a><span data-ttu-id="31d09-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31d09-113">Requirements</span></span>



| <span data-ttu-id="31d09-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="31d09-114">Requirement</span></span> | <span data-ttu-id="31d09-115">Value</span><span class="sxs-lookup"><span data-stu-id="31d09-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="31d09-116">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="31d09-116">End of client support</span></span><br/> | <span data-ttu-id="31d09-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31d09-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="31d09-118">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="31d09-118">End of server support</span></span><br/> | <span data-ttu-id="31d09-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31d09-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="31d09-120">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="31d09-120">Redistributable</span></span><br/>       | <span data-ttu-id="31d09-121">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="31d09-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="31d09-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="31d09-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="31d09-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31d09-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
