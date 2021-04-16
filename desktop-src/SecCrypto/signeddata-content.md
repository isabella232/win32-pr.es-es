---
description: Establece o recupera los datos que se van a firmar. Esta es la propiedad predeterminada.
ms.assetid: 554ca500-403d-4c2a-868e-9e635d0b358e
title: Propiedad SignedData. Content
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Content
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3c2ac97eeee317b4ec170338f666e5b5d9277861
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671645"
---
# <a name="signeddatacontent-property"></a><span data-ttu-id="377b1-104">Propiedad SignedData. Content</span><span class="sxs-lookup"><span data-stu-id="377b1-104">SignedData.Content property</span></span>

<span data-ttu-id="377b1-105">\[La propiedad de **contenido** está disponible para su uso en los sistemas operativos especificados en la sección requisitos.</span><span class="sxs-lookup"><span data-stu-id="377b1-105">\[The **Content** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="377b1-106">En su lugar, use la [**clase SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="377b1-106">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="377b1-107">La propiedad de **contenido** establece o recupera los datos que se van a firmar.</span><span class="sxs-lookup"><span data-stu-id="377b1-107">The **Content** property sets or retrieves the data to be signed.</span></span> <span data-ttu-id="377b1-108">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="377b1-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="377b1-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="377b1-109">Syntax</span></span>


```VB
SignedData.Content As String
```



## <a name="property-value"></a><span data-ttu-id="377b1-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="377b1-110">Property value</span></span>

<span data-ttu-id="377b1-111">Datos que van a firmar.</span><span class="sxs-lookup"><span data-stu-id="377b1-111">The data to be signed.</span></span>

## <a name="remarks"></a><span data-ttu-id="377b1-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="377b1-112">Remarks</span></span>

<span data-ttu-id="377b1-113">Esta propiedad se debe inicializar antes de que se llame al método [**Sign**](signeddata-sign.md) .</span><span class="sxs-lookup"><span data-stu-id="377b1-113">This property must be initialized before the [**Sign**](signeddata-sign.md) method is called.</span></span> <span data-ttu-id="377b1-114">Cuando el valor de esta propiedad se restablece, directa o indirectamente, se restablece el [*Estado*](../secgloss/s-gly.md) completo del objeto y se pierde cualquier firma asociada al objeto antes de que se cambiara la propiedad.</span><span class="sxs-lookup"><span data-stu-id="377b1-114">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset, and any signature that was associated with the object before the property was changed is lost.</span></span>

## <a name="requirements"></a><span data-ttu-id="377b1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="377b1-115">Requirements</span></span>



| <span data-ttu-id="377b1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="377b1-116">Requirement</span></span> | <span data-ttu-id="377b1-117">Value</span><span class="sxs-lookup"><span data-stu-id="377b1-117">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="377b1-118">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="377b1-118">Redistributable</span></span><br/> | <span data-ttu-id="377b1-119">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="377b1-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="377b1-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="377b1-120">DLL</span></span><br/>             | <dl> <span data-ttu-id="377b1-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="377b1-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="377b1-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="377b1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="377b1-123">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="377b1-123">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
