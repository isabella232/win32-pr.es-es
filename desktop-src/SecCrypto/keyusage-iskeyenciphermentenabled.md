---
description: Recupera un valor booleano que indica si se ha establecido el bit keyEncipherment.
ms.assetid: 2bdce181-3de7-4dc1-8059-1e1ca96c0d2d
title: Propiedad KeyUsage. IsKeyEnciphermentEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsKeyEnciphermentEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: db34737954b0627953758ebc1c5bf7a64b45b1b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670291"
---
# <a name="keyusageiskeyenciphermentenabled-property"></a><span data-ttu-id="1d88a-103">Propiedad KeyUsage. IsKeyEnciphermentEnabled</span><span class="sxs-lookup"><span data-stu-id="1d88a-103">KeyUsage.IsKeyEnciphermentEnabled property</span></span>

<span data-ttu-id="1d88a-104">\[La propiedad **IsKeyEnciphermentEnabled** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="1d88a-104">\[The **IsKeyEnciphermentEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1d88a-105">En su lugar, use la [**clase X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="1d88a-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="1d88a-106">La propiedad **IsKeyEnciphermentEnabled** recupera un valor booleano que indica si se ha establecido el bit keyEncipherment.</span><span class="sxs-lookup"><span data-stu-id="1d88a-106">The **IsKeyEnciphermentEnabled** property retrieves a Boolean value that indicates whether the keyEncipherment bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d88a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d88a-107">Syntax</span></span>


```VB
KeyUsage.IsKeyEnciphermentEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="1d88a-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="1d88a-108">Property value</span></span>

<span data-ttu-id="1d88a-109">Si es **true**, se establece el bit keyEncipherment.</span><span class="sxs-lookup"><span data-stu-id="1d88a-109">If **true**, the keyEncipherment bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d88a-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d88a-110">Requirements</span></span>



| <span data-ttu-id="1d88a-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d88a-111">Requirement</span></span> | <span data-ttu-id="1d88a-112">Value</span><span class="sxs-lookup"><span data-stu-id="1d88a-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d88a-113">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="1d88a-113">Redistributable</span></span><br/> | <span data-ttu-id="1d88a-114">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="1d88a-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1d88a-115">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1d88a-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="1d88a-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d88a-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d88a-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d88a-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d88a-118">**KeyUsage**</span><span class="sxs-lookup"><span data-stu-id="1d88a-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
