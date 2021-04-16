---
description: Recupera el número de objetos ExtendedProperty de la colección.
ms.assetid: 50bc8485-7285-4704-80db-c2e0d68e8cb0
title: ExtendedProperties. Count (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d4370f7ce5fc215d18b0940d3dbc2edc221af536
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649865"
---
# <a name="extendedpropertiescount-property"></a><span data-ttu-id="9acc0-103">ExtendedProperties. Count (propiedad)</span><span class="sxs-lookup"><span data-stu-id="9acc0-103">ExtendedProperties.Count property</span></span>

<span data-ttu-id="9acc0-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9acc0-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="9acc0-105">En su lugar, use servicios de invocación de plataforma (PInvoke) para llamar a la función de la API de Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) y obtener las propiedades.</span><span class="sxs-lookup"><span data-stu-id="9acc0-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="9acc0-106">Para obtener información sobre PInvoke, vea [tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="9acc0-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="9acc0-107">También pueden resultar útiles las subsecciones de [.net y CryptoAPI a través de p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) y [.net y CryptoAPI a través de p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) de la extensión de la [criptografía de .net con CAPICOM y p/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="9acc0-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="9acc0-108">La propiedad **Count** recupera el número de objetos [**ExtendedProperty**](extendedproperty.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="9acc0-108">The **Count** property retrieves the number of [**ExtendedProperty**](extendedproperty.md) objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="9acc0-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9acc0-109">Syntax</span></span>


```VB
ExtendedProperties.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="9acc0-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="9acc0-110">Property value</span></span>

<span data-ttu-id="9acc0-111">Número de objetos [**ExtendedProperty**](extendedproperty.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="9acc0-111">The number of [**ExtendedProperty**](extendedproperty.md) objects in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="9acc0-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9acc0-112">Requirements</span></span>



| <span data-ttu-id="9acc0-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9acc0-113">Requirement</span></span> | <span data-ttu-id="9acc0-114">Value</span><span class="sxs-lookup"><span data-stu-id="9acc0-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9acc0-115">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="9acc0-115">End of client support</span></span><br/> | <span data-ttu-id="9acc0-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9acc0-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9acc0-117">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="9acc0-117">End of server support</span></span><br/> | <span data-ttu-id="9acc0-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9acc0-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9acc0-119">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="9acc0-119">Redistributable</span></span><br/>       | <span data-ttu-id="9acc0-120">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="9acc0-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9acc0-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9acc0-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="9acc0-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9acc0-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
