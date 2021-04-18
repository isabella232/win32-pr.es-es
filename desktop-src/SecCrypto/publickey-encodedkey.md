---
description: Recupera el valor de la clave pública.
ms.assetid: d9846ebe-44df-4ee0-8f15-cc96883d9d53
title: Propiedad PublicKey. EncodedKey
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.EncodedKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: de2c7b2bfbbdaf28345ae29e260bfd30c5754ffd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690934"
---
# <a name="publickeyencodedkey-property"></a><span data-ttu-id="bf200-103">Propiedad PublicKey. EncodedKey</span><span class="sxs-lookup"><span data-stu-id="bf200-103">PublicKey.EncodedKey property</span></span>

<span data-ttu-id="bf200-104">\[La propiedad **EncodedKey** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="bf200-104">\[The **EncodedKey** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bf200-105">En su lugar, use la [**propiedad X509Certificate2. publickey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="bf200-105">Instead, use the [**X509Certificate2.PublicKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="bf200-106">La propiedad **EncodedKey** recupera el valor de la clave pública.</span><span class="sxs-lookup"><span data-stu-id="bf200-106">The **EncodedKey** property retrieves the value of the public key.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf200-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bf200-107">Syntax</span></span>


```VB
PublicKey.EncodedKey As EncodedData
```



## <a name="property-value"></a><span data-ttu-id="bf200-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="bf200-108">Property value</span></span>

<span data-ttu-id="bf200-109">Un objeto [**EncodedData**](encodeddata.md) que proporciona acceso al valor de la clave pública.</span><span class="sxs-lookup"><span data-stu-id="bf200-109">An [**EncodedData**](encodeddata.md) object that provides access to the value of the public key.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf200-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf200-110">Requirements</span></span>



| <span data-ttu-id="bf200-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf200-111">Requirement</span></span> | <span data-ttu-id="bf200-112">Value</span><span class="sxs-lookup"><span data-stu-id="bf200-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf200-113">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="bf200-113">Redistributable</span></span><br/> | <span data-ttu-id="bf200-114">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="bf200-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="bf200-115">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bf200-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="bf200-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf200-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf200-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf200-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf200-118">**PublicKey**</span><span class="sxs-lookup"><span data-stu-id="bf200-118">**PublicKey**</span></span>](publickey.md)
</dt> </dl>

 

 
