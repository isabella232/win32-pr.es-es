---
description: La \_ propiedad NewEnum de ExtendedProperties recupera una interfaz IEnumVARIANT en un objeto que se puede utilizar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).
ms.assetid: 2692f607-3bec-4674-9d8d-3c872d523ace
title: Propiedad ExtendedProperties._NewEnum
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 62f07fe7a1a193f93fc0d3bf4c04fbfc5d76ecf9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670959"
---
# <a name="extendedproperties_newenum-property"></a><span data-ttu-id="7f640-104">ExtendedProperties. \_ Propiedad NewEnum</span><span class="sxs-lookup"><span data-stu-id="7f640-104">ExtendedProperties.\_NewEnum property</span></span>

<span data-ttu-id="7f640-105">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7f640-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="7f640-106">En su lugar, use servicios de invocación de plataforma (PInvoke) para llamar a la función de la API de Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) y obtener las propiedades.</span><span class="sxs-lookup"><span data-stu-id="7f640-106">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="7f640-107">Para obtener información sobre PInvoke, vea [tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="7f640-107">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="7f640-108">También pueden resultar útiles las subsecciones de [.net y CryptoAPI a través de p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) y [.net y CryptoAPI a través de p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) de la extensión de la [criptografía de .net con CAPICOM y p/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="7f640-108">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="7f640-109">La propiedad **\_ NewEnum** recupera una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección.</span><span class="sxs-lookup"><span data-stu-id="7f640-109">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="7f640-110">Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="7f640-110">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="7f640-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7f640-111">Syntax</span></span>


```VB
ExtendedProperties._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="7f640-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="7f640-112">Property value</span></span>

<span data-ttu-id="7f640-113">Una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección.</span><span class="sxs-lookup"><span data-stu-id="7f640-113">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f640-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7f640-114">Remarks</span></span>

<span data-ttu-id="7f640-115">Esta propiedad se utiliza internamente de forma automática cuando se usa la `For Each In` construcción en Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="7f640-115">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f640-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f640-116">Requirements</span></span>



| <span data-ttu-id="7f640-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f640-117">Requirement</span></span> | <span data-ttu-id="7f640-118">Value</span><span class="sxs-lookup"><span data-stu-id="7f640-118">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f640-119">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="7f640-119">End of client support</span></span><br/> | <span data-ttu-id="7f640-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7f640-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7f640-121">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="7f640-121">End of server support</span></span><br/> | <span data-ttu-id="7f640-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7f640-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7f640-123">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="7f640-123">Redistributable</span></span><br/>       | <span data-ttu-id="7f640-124">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="7f640-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7f640-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7f640-125">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7f640-126"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f640-126"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
