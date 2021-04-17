---
description: La propiedad Item recupera un objeto ExtendedProperty de la colección. Esta es la propiedad predeterminada.
ms.assetid: add819e1-6330-483a-8a76-3b7fb8d3f110
title: ExtendedProperties. Item (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 200e36f232c97c1b5a86c8a8a975783469d64a71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670960"
---
# <a name="extendedpropertiesitem-property"></a><span data-ttu-id="a6c93-104">ExtendedProperties. Item (propiedad)</span><span class="sxs-lookup"><span data-stu-id="a6c93-104">ExtendedProperties.Item property</span></span>

<span data-ttu-id="a6c93-105">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a6c93-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="a6c93-106">En su lugar, use servicios de invocación de plataforma (PInvoke) para llamar a la función de la API de Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) y obtener las propiedades.</span><span class="sxs-lookup"><span data-stu-id="a6c93-106">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="a6c93-107">Para obtener información sobre PInvoke, vea [tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="a6c93-107">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="a6c93-108">También pueden resultar útiles las subsecciones de [.net y CryptoAPI a través de p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) y [.net y CryptoAPI a través de p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) de la extensión de la [criptografía de .net con CAPICOM y p/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="a6c93-108">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="a6c93-109">La propiedad **Item** recupera un objeto [**ExtendedProperty**](extendedproperty.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="a6c93-109">The **Item** property retrieves an [**ExtendedProperty**](extendedproperty.md) object from the collection.</span></span> <span data-ttu-id="a6c93-110">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a6c93-110">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6c93-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a6c93-111">Syntax</span></span>


```VB
ExtendedProperties.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="a6c93-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a6c93-112">Property value</span></span>

<span data-ttu-id="a6c93-113">Objeto [**ExtendedProperty**](extendedproperty.md) que representa la propiedad extendida indizada de la colección.</span><span class="sxs-lookup"><span data-stu-id="a6c93-113">An [**ExtendedProperty**](extendedproperty.md) object that represents the indexed extended property of the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6c93-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6c93-114">Requirements</span></span>



| <span data-ttu-id="a6c93-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6c93-115">Requirement</span></span> | <span data-ttu-id="a6c93-116">Value</span><span class="sxs-lookup"><span data-stu-id="a6c93-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6c93-117">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="a6c93-117">End of client support</span></span><br/> | <span data-ttu-id="a6c93-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a6c93-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a6c93-119">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="a6c93-119">End of server support</span></span><br/> | <span data-ttu-id="a6c93-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a6c93-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a6c93-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="a6c93-121">Redistributable</span></span><br/>       | <span data-ttu-id="a6c93-122">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="a6c93-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a6c93-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a6c93-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a6c93-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6c93-124"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
