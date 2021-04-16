---
description: Establece o recupera el nombre para mostrar del identificador.
ms.assetid: 53f84d0d-c189-4fd2-a383-29fd0d22de08
title: OID. FriendlyName (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID.FriendlyName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1976980d1a22f4246f0ace686941cc4bcec87c92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671496"
---
# <a name="oidfriendlyname-property"></a><span data-ttu-id="b8dec-103">OID. FriendlyName (propiedad)</span><span class="sxs-lookup"><span data-stu-id="b8dec-103">OID.FriendlyName property</span></span>

<span data-ttu-id="b8dec-104">\[La propiedad **FriendlyName** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="b8dec-104">\[The **FriendlyName** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b8dec-105">En su lugar, use la [**clase OID**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="b8dec-105">Instead, use the [**Oid Class**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="b8dec-106">La propiedad **FriendlyName** establece o recupera el nombre para mostrar del identificador.</span><span class="sxs-lookup"><span data-stu-id="b8dec-106">The **FriendlyName** property sets or retrieves the display name for the identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8dec-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8dec-107">Syntax</span></span>


```VB
OID.FriendlyName As String
```



## <a name="property-value"></a><span data-ttu-id="b8dec-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b8dec-108">Property value</span></span>

<span data-ttu-id="b8dec-109">Nombre para mostrar del [**OID**](oid.md).</span><span class="sxs-lookup"><span data-stu-id="b8dec-109">The display name for the [**OID**](oid.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b8dec-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8dec-110">Remarks</span></span>

<span data-ttu-id="b8dec-111">Si se establece la propiedad **FriendlyName** , la propiedad [**Value**](oid-value.md) se establece en el valor punteado correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b8dec-111">If the **FriendlyName** property is set, the [**Value**](oid-value.md) property is set to the corresponding dotted value.</span></span> <span data-ttu-id="b8dec-112">Si se establece la propiedad **Value** , la propiedad **FriendlyName** se establece en el nombre para mostrar correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b8dec-112">If the **Value** property is set, the **FriendlyName** property is set to the corresponding display name.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8dec-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8dec-113">Requirements</span></span>



| <span data-ttu-id="b8dec-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8dec-114">Requirement</span></span> | <span data-ttu-id="b8dec-115">Value</span><span class="sxs-lookup"><span data-stu-id="b8dec-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8dec-116">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="b8dec-116">Redistributable</span></span><br/> | <span data-ttu-id="b8dec-117">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="b8dec-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b8dec-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b8dec-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="b8dec-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8dec-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8dec-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8dec-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8dec-121">**OID**</span><span class="sxs-lookup"><span data-stu-id="b8dec-121">**OID**</span></span>](oid.md)
</dt> </dl>

 

 
