---
description: Recupera los creadores de la firma de los datos.
ms.assetid: 3e28f08a-c4d8-4dd7-953a-e1500eb5bee0
title: Propiedad SignedData. Signers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Signers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5f4c58c2a69c483fc38412a6aa8377742d52d39a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690058"
---
# <a name="signeddatasigners-property"></a><span data-ttu-id="1baa0-103">Propiedad SignedData. Signers</span><span class="sxs-lookup"><span data-stu-id="1baa0-103">SignedData.Signers property</span></span>

<span data-ttu-id="1baa0-104">\[La propiedad **signers** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="1baa0-104">\[The **Signers** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1baa0-105">En su lugar, use la [**clase SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="1baa0-105">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="1baa0-106">La propiedad **signers** recupera los creadores de firmas de los datos.</span><span class="sxs-lookup"><span data-stu-id="1baa0-106">The **Signers** property retrieves the signature creators of the data.</span></span>

## <a name="syntax"></a><span data-ttu-id="1baa0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1baa0-107">Syntax</span></span>


```VB
SignedData.Signers As Signers
```



## <a name="property-value"></a><span data-ttu-id="1baa0-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="1baa0-108">Property value</span></span>

<span data-ttu-id="1baa0-109">Colección de [**firmadores**](signers.md) que representa los creadores de firmas de los datos.</span><span class="sxs-lookup"><span data-stu-id="1baa0-109">The [**Signers**](signers.md) collection that represents the signature creators of the data.</span></span>

## <a name="requirements"></a><span data-ttu-id="1baa0-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1baa0-110">Requirements</span></span>



| <span data-ttu-id="1baa0-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="1baa0-111">Requirement</span></span> | <span data-ttu-id="1baa0-112">Value</span><span class="sxs-lookup"><span data-stu-id="1baa0-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1baa0-113">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="1baa0-113">Redistributable</span></span><br/> | <span data-ttu-id="1baa0-114">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="1baa0-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1baa0-115">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1baa0-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="1baa0-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1baa0-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1baa0-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="1baa0-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1baa0-118">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="1baa0-118">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
