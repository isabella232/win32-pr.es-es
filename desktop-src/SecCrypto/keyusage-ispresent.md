---
description: Recupera un valor booleano que indica si la extensión KeyUsage está presente.
ms.assetid: d666049a-4b40-42b6-8c2d-c27a1bb4c48a
title: Propiedad KeyUsage. IsPresent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f70754c15a248cda69f93fcab2a0052bd8351261
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670289"
---
# <a name="keyusageispresent-property"></a><span data-ttu-id="3885b-103">Propiedad KeyUsage. IsPresent</span><span class="sxs-lookup"><span data-stu-id="3885b-103">KeyUsage.IsPresent property</span></span>

<span data-ttu-id="3885b-104">\[La propiedad **IsPresent** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="3885b-104">\[The **IsPresent** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3885b-105">En su lugar, use la [**clase X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="3885b-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="3885b-106">La propiedad **IsPresent** recupera un valor booleano que indica si la extensión [**KeyUsage**](keyusage.md) está presente.</span><span class="sxs-lookup"><span data-stu-id="3885b-106">The **IsPresent** property retrieves a Boolean value that indicates whether the [**KeyUsage**](keyusage.md) extension is present.</span></span>

<span data-ttu-id="3885b-107">Esta propiedad es la propiedad predeterminada del objeto [**KeyUsage**](keyusage.md) .</span><span class="sxs-lookup"><span data-stu-id="3885b-107">This property is the default property of the [**KeyUsage**](keyusage.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3885b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3885b-108">Syntax</span></span>


```VB
KeyUsage.IsPresent As Boolean
```



## <a name="property-value"></a><span data-ttu-id="3885b-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3885b-109">Property value</span></span>

<span data-ttu-id="3885b-110">Si es **true**, la extensión KeyUsage está presente.</span><span class="sxs-lookup"><span data-stu-id="3885b-110">If **true**, the KeyUsage extension is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="3885b-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3885b-111">Requirements</span></span>



| <span data-ttu-id="3885b-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="3885b-112">Requirement</span></span> | <span data-ttu-id="3885b-113">Value</span><span class="sxs-lookup"><span data-stu-id="3885b-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3885b-114">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="3885b-114">Redistributable</span></span><br/> | <span data-ttu-id="3885b-115">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="3885b-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="3885b-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3885b-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="3885b-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3885b-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3885b-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="3885b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3885b-119">**KeyUsage**</span><span class="sxs-lookup"><span data-stu-id="3885b-119">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
