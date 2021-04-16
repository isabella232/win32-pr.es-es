---
description: La \_ propiedad NewEnum de los firmantes recupera una interfaz IEnumVARIANT en un objeto que se puede utilizar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).
ms.assetid: 99d7ddd3-a552-4125-b220-d1b28f20d1ed
title: Propiedad Signers._NewEnum
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 91007e7ce282cb44267927f54ab26f8f930028f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671439"
---
# <a name="signers_newenum-property"></a><span data-ttu-id="7e7dd-104">Los firmantes. \_ Propiedad NewEnum</span><span class="sxs-lookup"><span data-stu-id="7e7dd-104">Signers.\_NewEnum property</span></span>

<span data-ttu-id="7e7dd-105">\[La propiedad **\_ NewEnum** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="7e7dd-105">\[The **\_NewEnum** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7e7dd-106">En su lugar, use una colección de objetos CmsSigner.</span><span class="sxs-lookup"><span data-stu-id="7e7dd-106">Instead, use a collection of CmsSigner objects.</span></span> <span data-ttu-id="7e7dd-107">Para obtener más información, vea la [**clase CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="7e7dd-107">For more information, see the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="7e7dd-108">La propiedad **\_ NewEnum** recupera una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección.</span><span class="sxs-lookup"><span data-stu-id="7e7dd-108">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="7e7dd-109">Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="7e7dd-109">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="7e7dd-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e7dd-110">Syntax</span></span>


```VB
Signers._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="7e7dd-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="7e7dd-111">Property value</span></span>

<span data-ttu-id="7e7dd-112">Una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección.</span><span class="sxs-lookup"><span data-stu-id="7e7dd-112">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e7dd-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e7dd-113">Remarks</span></span>

<span data-ttu-id="7e7dd-114">Esta propiedad se utiliza internamente de forma automática cuando se usa la `For Each In` construcción en Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="7e7dd-114">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="7e7dd-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e7dd-115">Requirements</span></span>



| <span data-ttu-id="7e7dd-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e7dd-116">Requirement</span></span> | <span data-ttu-id="7e7dd-117">Value</span><span class="sxs-lookup"><span data-stu-id="7e7dd-117">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e7dd-118">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="7e7dd-118">Redistributable</span></span><br/> | <span data-ttu-id="7e7dd-119">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="7e7dd-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7e7dd-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7e7dd-120">DLL</span></span><br/>             | <dl> <span data-ttu-id="7e7dd-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e7dd-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e7dd-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e7dd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e7dd-123">**Firmantes**</span><span class="sxs-lookup"><span data-stu-id="7e7dd-123">**Signers**</span></span>](signers.md)
</dt> </dl>

 

 
