---
description: La propiedad Item recupera una extensión, por índice, de la colección. Esta es la propiedad predeterminada.
ms.assetid: 0242dc14-abf2-49df-b75a-9005b2376cfc
title: Extensions. Item (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extensions.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b2cefe9ac1dd278c17161cc8e2349c051dccabff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690211"
---
# <a name="extensionsitem-property"></a><span data-ttu-id="75ff4-104">Extensions. Item (propiedad)</span><span class="sxs-lookup"><span data-stu-id="75ff4-104">Extensions.Item property</span></span>

<span data-ttu-id="75ff4-105">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="75ff4-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="75ff4-106">En su lugar, use la [**clase X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="75ff4-106">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="75ff4-107">La propiedad **Item** recupera una extensión, por índice, de la colección.</span><span class="sxs-lookup"><span data-stu-id="75ff4-107">The **Item** property retrieves an extension, by index, from the collection.</span></span> <span data-ttu-id="75ff4-108">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="75ff4-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="75ff4-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75ff4-109">Syntax</span></span>


```VB
Extensions.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="75ff4-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="75ff4-110">Property value</span></span>

<span data-ttu-id="75ff4-111">Objeto de [**extensión**](extension.md) que representa la extensión de certificado indizada de la colección.</span><span class="sxs-lookup"><span data-stu-id="75ff4-111">An [**Extension**](extension.md) object that represents the indexed certificate extension of the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="75ff4-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75ff4-112">Requirements</span></span>



| <span data-ttu-id="75ff4-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="75ff4-113">Requirement</span></span> | <span data-ttu-id="75ff4-114">Value</span><span class="sxs-lookup"><span data-stu-id="75ff4-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="75ff4-115">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="75ff4-115">End of client support</span></span><br/> | <span data-ttu-id="75ff4-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="75ff4-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="75ff4-117">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="75ff4-117">End of server support</span></span><br/> | <span data-ttu-id="75ff4-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75ff4-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="75ff4-119">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="75ff4-119">Redistributable</span></span><br/>       | <span data-ttu-id="75ff4-120">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="75ff4-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="75ff4-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="75ff4-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="75ff4-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75ff4-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75ff4-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="75ff4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75ff4-124">**Extensiones**</span><span class="sxs-lookup"><span data-stu-id="75ff4-124">**Extensions**</span></span>](extensions.md)
</dt> </dl>

 

 
