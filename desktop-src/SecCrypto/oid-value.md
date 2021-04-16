---
description: Establece o recupera el valor del número de puntos del OID del identificador.
ms.assetid: bb960e65-776e-4ae8-a557-62254dc10558
title: OID. Value (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d8c3c59cfd3eadfb8aec56c6814a2af6ce9ff900
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671787"
---
# <a name="oidvalue-property"></a><span data-ttu-id="803c2-103">OID. Value (propiedad)</span><span class="sxs-lookup"><span data-stu-id="803c2-103">OID.Value property</span></span>

<span data-ttu-id="803c2-104">\[La propiedad **Value** está disponible para su uso en los sistemas operativos especificados en la sección requirements.</span><span class="sxs-lookup"><span data-stu-id="803c2-104">\[The **Value** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="803c2-105">En su lugar, use la [**clase OID**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="803c2-105">Instead, use the [**Oid Class**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="803c2-106">La propiedad **Value** establece o recupera el valor del número de puntos OID del identificador.</span><span class="sxs-lookup"><span data-stu-id="803c2-106">The **Value** property sets or retrieves the value of the OID dotted number of the identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="803c2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="803c2-107">Syntax</span></span>


```VB
OID.Value As String
```



## <a name="property-value"></a><span data-ttu-id="803c2-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="803c2-108">Property value</span></span>

<span data-ttu-id="803c2-109">Valor del número de puntos del OID del identificador.</span><span class="sxs-lookup"><span data-stu-id="803c2-109">The value of the OID dotted number of the identifier.</span></span> <span data-ttu-id="803c2-110">Para obtener los valores posibles, consulte Wincrypt. h.</span><span class="sxs-lookup"><span data-stu-id="803c2-110">For possible values, see Wincrypt.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="803c2-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="803c2-111">Remarks</span></span>

<span data-ttu-id="803c2-112">Si se establece la propiedad **Value** , la propiedad [**FriendlyName**](oid-friendlyname.md) se establece en el nombre para mostrar correspondiente.</span><span class="sxs-lookup"><span data-stu-id="803c2-112">If the **Value** property is set, the [**FriendlyName**](oid-friendlyname.md) property is set to the corresponding display name.</span></span> <span data-ttu-id="803c2-113">Si se establece la propiedad **FriendlyName** , la propiedad **Value** se establece en el valor punteado correspondiente.</span><span class="sxs-lookup"><span data-stu-id="803c2-113">If the **FriendlyName** property is set, the **Value** property is set to the corresponding dotted value.</span></span>

## <a name="requirements"></a><span data-ttu-id="803c2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="803c2-114">Requirements</span></span>



| <span data-ttu-id="803c2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="803c2-115">Requirement</span></span> | <span data-ttu-id="803c2-116">Value</span><span class="sxs-lookup"><span data-stu-id="803c2-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="803c2-117">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="803c2-117">Redistributable</span></span><br/> | <span data-ttu-id="803c2-118">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="803c2-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="803c2-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="803c2-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="803c2-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="803c2-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="803c2-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="803c2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="803c2-122">**OID**</span><span class="sxs-lookup"><span data-stu-id="803c2-122">**OID**</span></span>](oid.md)
</dt> </dl>

 

 
