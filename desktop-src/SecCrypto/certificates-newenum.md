---
description: La \_ propiedad NewEnum de certificados recupera una interfaz IEnumVARIANT en un objeto que se puede utilizar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).
ms.assetid: bbe6c82c-1949-4d81-bb87-3f05613efa6d
title: Propiedad Certificates._NewEnum
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 71760f23bbb19d32c3caf8011eb87b8d03941eac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690982"
---
# <a name="certificates_newenum-property"></a><span data-ttu-id="c5767-104">Certificados. \_ Propiedad NewEnum</span><span class="sxs-lookup"><span data-stu-id="c5767-104">Certificates.\_NewEnum property</span></span>

<span data-ttu-id="c5767-105">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c5767-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="c5767-106">En su lugar, use la [**clase X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="c5767-106">Instead, use the [**X509Certificate2Collection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="c5767-107">La propiedad **\_ NewEnum** recupera una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección.</span><span class="sxs-lookup"><span data-stu-id="c5767-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="c5767-108">Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="c5767-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="c5767-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5767-109">Syntax</span></span>


```VB
Certificates._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="c5767-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c5767-110">Property value</span></span>

<span data-ttu-id="c5767-111">Una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección.</span><span class="sxs-lookup"><span data-stu-id="c5767-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5767-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c5767-112">Remarks</span></span>

<span data-ttu-id="c5767-113">Esta propiedad se utiliza internamente de forma automática cuando se usa la `For Each In` construcción en Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="c5767-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5767-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5767-114">Requirements</span></span>



| <span data-ttu-id="c5767-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5767-115">Requirement</span></span> | <span data-ttu-id="c5767-116">Value</span><span class="sxs-lookup"><span data-stu-id="c5767-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5767-117">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="c5767-117">End of client support</span></span><br/> | <span data-ttu-id="c5767-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c5767-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c5767-119">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="c5767-119">End of server support</span></span><br/> | <span data-ttu-id="c5767-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c5767-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c5767-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="c5767-121">Redistributable</span></span><br/>       | <span data-ttu-id="c5767-122">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="c5767-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c5767-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c5767-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="c5767-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5767-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5767-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5767-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5767-126">**Certificados**</span><span class="sxs-lookup"><span data-stu-id="c5767-126">**Certificates**</span></span>](certificates.md)
</dt> </dl>

 

 
