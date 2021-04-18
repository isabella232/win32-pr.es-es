---
description: Recupera el objeto de firmante que representa el firmante indizado.
ms.assetid: a95f4e33-ab92-44e1-91ab-2c5335a04f05
title: Propiedad signers. Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9b0b4179c1ea7e2ded5d945f64f03124eb864fdc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691054"
---
# <a name="signersitem-property"></a><span data-ttu-id="49abf-103">Propiedad signers. Item</span><span class="sxs-lookup"><span data-stu-id="49abf-103">Signers.Item property</span></span>

<span data-ttu-id="49abf-104">\[La propiedad **Item** está disponible para su uso en los sistemas operativos especificados en la sección requirements.</span><span class="sxs-lookup"><span data-stu-id="49abf-104">\[The **Item** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="49abf-105">En su lugar, use una colección de objetos CmsSigner.</span><span class="sxs-lookup"><span data-stu-id="49abf-105">Instead, use a collection of CmsSigner objects.</span></span> <span data-ttu-id="49abf-106">Para obtener más información, vea la [**clase CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="49abf-106">For more information, see the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="49abf-107">La propiedad **Item** recupera el objeto de [**firmante**](signer.md) que representa el firmante indizado.</span><span class="sxs-lookup"><span data-stu-id="49abf-107">The **Item** property retrieves the [**Signer**](signer.md) object that represents the indexed signer.</span></span> <span data-ttu-id="49abf-108">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="49abf-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="49abf-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="49abf-109">Syntax</span></span>


```VB
Signers.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="49abf-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="49abf-110">Property value</span></span>

<span data-ttu-id="49abf-111">Objeto de [**firmante**](signer.md) que representa el firmante indizado.</span><span class="sxs-lookup"><span data-stu-id="49abf-111">The [**Signer**](signer.md) object that represents the indexed signer.</span></span>

## <a name="requirements"></a><span data-ttu-id="49abf-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49abf-112">Requirements</span></span>



| <span data-ttu-id="49abf-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="49abf-113">Requirement</span></span> | <span data-ttu-id="49abf-114">Value</span><span class="sxs-lookup"><span data-stu-id="49abf-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="49abf-115">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="49abf-115">Redistributable</span></span><br/> | <span data-ttu-id="49abf-116">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="49abf-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="49abf-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="49abf-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="49abf-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49abf-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49abf-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="49abf-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49abf-120">**Firmantes**</span><span class="sxs-lookup"><span data-stu-id="49abf-120">**Signers**</span></span>](signers.md)
</dt> </dl>

 

 
