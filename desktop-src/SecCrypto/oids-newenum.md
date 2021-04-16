---
description: La \_ propiedad NewEnum de OID recupera una interfaz IEnumVARIANT en un objeto que se puede utilizar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).
ms.assetid: 7c09fd11-064b-451e-bd6b-e6c13ab228a0
title: Propiedad OIDs._NewEnum
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d20856c17dda18a10b85c01453cbe043144742d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690065"
---
# <a name="oids_newenum-property"></a><span data-ttu-id="61010-104">OID. \_ Propiedad NewEnum</span><span class="sxs-lookup"><span data-stu-id="61010-104">OIDs.\_NewEnum property</span></span>

<span data-ttu-id="61010-105">\[La propiedad **\_ NewEnum** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="61010-105">\[The **\_NewEnum** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="61010-106">En su lugar, use la [**clase OidCollection**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="61010-106">Instead, use the [**OidCollection Class**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="61010-107">La propiedad **\_ NewEnum** recupera una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección.</span><span class="sxs-lookup"><span data-stu-id="61010-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="61010-108">Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="61010-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="61010-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="61010-109">Syntax</span></span>


```VB
OIDs._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="61010-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="61010-110">Property value</span></span>

<span data-ttu-id="61010-111">Una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección.</span><span class="sxs-lookup"><span data-stu-id="61010-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="61010-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="61010-112">Remarks</span></span>

<span data-ttu-id="61010-113">Esta propiedad se utiliza internamente de forma automática cuando se usa la `For Each In` construcción en Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="61010-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="61010-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61010-114">Requirements</span></span>



| <span data-ttu-id="61010-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="61010-115">Requirement</span></span> | <span data-ttu-id="61010-116">Value</span><span class="sxs-lookup"><span data-stu-id="61010-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="61010-117">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="61010-117">Redistributable</span></span><br/> | <span data-ttu-id="61010-118">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="61010-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="61010-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="61010-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="61010-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61010-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61010-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="61010-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61010-122">**OID**</span><span class="sxs-lookup"><span data-stu-id="61010-122">**OIDs**</span></span>](oids.md)
</dt> </dl>

 

 
