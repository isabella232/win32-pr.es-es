---
description: La \_ propiedad NewEnum de los atributos recupera una interfaz IEnumVARIANT en un objeto que se puede utilizar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).
ms.assetid: a90ef28b-3926-4542-bcd2-27f0eda4e339
title: Propiedad Attributes._NewEnum
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9948c55943a8374665fe5e4883013742188665c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671026"
---
# <a name="attributes_newenum-property"></a><span data-ttu-id="6d00e-104">Atributos. \_ Propiedad NewEnum</span><span class="sxs-lookup"><span data-stu-id="6d00e-104">Attributes.\_NewEnum property</span></span>

<span data-ttu-id="6d00e-105">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6d00e-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="6d00e-106">En su lugar, use la [**clase CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="6d00e-106">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="6d00e-107">La propiedad **\_ NewEnum** recupera una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección.</span><span class="sxs-lookup"><span data-stu-id="6d00e-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="6d00e-108">Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="6d00e-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="6d00e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6d00e-109">Syntax</span></span>


```VB
Attributes._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="6d00e-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="6d00e-110">Property value</span></span>

<span data-ttu-id="6d00e-111">Una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección.</span><span class="sxs-lookup"><span data-stu-id="6d00e-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d00e-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6d00e-112">Remarks</span></span>

<span data-ttu-id="6d00e-113">Esta propiedad se utiliza internamente de forma automática cuando se usa la `For Each In` construcción en Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="6d00e-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="6d00e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d00e-114">Requirements</span></span>



| <span data-ttu-id="6d00e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d00e-115">Requirement</span></span> | <span data-ttu-id="6d00e-116">Value</span><span class="sxs-lookup"><span data-stu-id="6d00e-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d00e-117">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="6d00e-117">End of client support</span></span><br/> | <span data-ttu-id="6d00e-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6d00e-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6d00e-119">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="6d00e-119">End of server support</span></span><br/> | <span data-ttu-id="6d00e-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d00e-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6d00e-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="6d00e-121">Redistributable</span></span><br/>       | <span data-ttu-id="6d00e-122">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="6d00e-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6d00e-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6d00e-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="6d00e-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d00e-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d00e-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d00e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d00e-126">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="6d00e-126">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 
