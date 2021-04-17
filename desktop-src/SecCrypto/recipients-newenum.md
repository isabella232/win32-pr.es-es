---
description: La \_ propiedad NewEnum de Recipients recupera una interfaz IEnumVARIANT en un objeto que se puede utilizar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).
ms.assetid: affdc695-b78c-48b5-b66d-5f94e1a86ff2
title: Propiedad Recipients._NewEnum
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a4a1e7db31ceead23509604edddee05ec64380ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670651"
---
# <a name="recipients_newenum-property"></a><span data-ttu-id="fa1ba-104">Destinatarios. \_ Propiedad NewEnum</span><span class="sxs-lookup"><span data-stu-id="fa1ba-104">Recipients.\_NewEnum property</span></span>

<span data-ttu-id="fa1ba-105">\[La propiedad **\_ NewEnum** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="fa1ba-105">\[The **\_NewEnum** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fa1ba-106">En su lugar, use la [**clase CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="fa1ba-106">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="fa1ba-107">La propiedad **\_ NewEnum** recupera una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección.</span><span class="sxs-lookup"><span data-stu-id="fa1ba-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="fa1ba-108">Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="fa1ba-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="fa1ba-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fa1ba-109">Syntax</span></span>


```VB
Recipients._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="fa1ba-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="fa1ba-110">Property value</span></span>

<span data-ttu-id="fa1ba-111">Una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección.</span><span class="sxs-lookup"><span data-stu-id="fa1ba-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa1ba-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fa1ba-112">Remarks</span></span>

<span data-ttu-id="fa1ba-113">Esta propiedad se utiliza internamente de forma automática cuando se usa la `For Each In` construcción en Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="fa1ba-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="fa1ba-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa1ba-114">Requirements</span></span>



| <span data-ttu-id="fa1ba-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa1ba-115">Requirement</span></span> | <span data-ttu-id="fa1ba-116">Value</span><span class="sxs-lookup"><span data-stu-id="fa1ba-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa1ba-117">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="fa1ba-117">Redistributable</span></span><br/> | <span data-ttu-id="fa1ba-118">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="fa1ba-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="fa1ba-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fa1ba-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="fa1ba-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa1ba-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa1ba-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa1ba-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa1ba-122">**Recipients**</span><span class="sxs-lookup"><span data-stu-id="fa1ba-122">**Recipients**</span></span>](recipients.md)
</dt> </dl>

 

 
