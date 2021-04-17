---
description: La \_ propiedad NewEnum de calificadores recupera una interfaz IEnumVARIANT en un objeto que se puede utilizar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).
ms.assetid: e51f8ca1-ef1f-475b-8368-e8296fae0f04
title: Propiedad Qualifiers._NewEnum
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 01a4d62604dabacd2d78d5d2f6cbee0db7189196
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690270"
---
# <a name="qualifiers_newenum-property"></a><span data-ttu-id="72801-104">Calificadores. \_ Propiedad NewEnum</span><span class="sxs-lookup"><span data-stu-id="72801-104">Qualifiers.\_NewEnum property</span></span>

<span data-ttu-id="72801-105">\[La propiedad **\_ NewEnum** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="72801-105">\[The **\_NewEnum** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="72801-106">En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para las directivas de certificado para procesar calificadores que formen parte de la información de directivas en la extensión de directivas de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="72801-106">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="72801-107">La propiedad **\_ NewEnum** recupera una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección.</span><span class="sxs-lookup"><span data-stu-id="72801-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="72801-108">Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="72801-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="72801-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="72801-109">Syntax</span></span>


```VB
Qualifiers._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="72801-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="72801-110">Property value</span></span>

<span data-ttu-id="72801-111">Una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección.</span><span class="sxs-lookup"><span data-stu-id="72801-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="72801-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="72801-112">Remarks</span></span>

<span data-ttu-id="72801-113">Esta propiedad se utiliza internamente de forma automática cuando se usa la `For Each In` construcción en Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="72801-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="72801-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72801-114">Requirements</span></span>



| <span data-ttu-id="72801-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="72801-115">Requirement</span></span> | <span data-ttu-id="72801-116">Value</span><span class="sxs-lookup"><span data-stu-id="72801-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="72801-117">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="72801-117">Redistributable</span></span><br/> | <span data-ttu-id="72801-118">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="72801-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="72801-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="72801-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="72801-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72801-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72801-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="72801-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72801-122">**Calificadores**</span><span class="sxs-lookup"><span data-stu-id="72801-122">**Qualifiers**</span></span>](qualifiers.md)
</dt> </dl>

 

 
