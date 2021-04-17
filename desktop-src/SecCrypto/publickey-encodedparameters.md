---
description: Recupera los parámetros del algoritmo de clave pública.
ms.assetid: 1d12f72e-0144-4b7b-b468-d2f35bf253d3
title: Propiedad PublicKey. EncodedParameters
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.EncodedParameters
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 316e9737633bccea46cb644da24e4cc98fd118bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671053"
---
# <a name="publickeyencodedparameters-property"></a><span data-ttu-id="6ecc7-103">Propiedad PublicKey. EncodedParameters</span><span class="sxs-lookup"><span data-stu-id="6ecc7-103">PublicKey.EncodedParameters property</span></span>

<span data-ttu-id="6ecc7-104">\[La propiedad **EncodedParameters** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="6ecc7-104">\[The **EncodedParameters** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6ecc7-105">En su lugar, use la [**propiedad X509Certificate2. publickey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="6ecc7-105">Instead, use the [**X509Certificate2.PublicKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="6ecc7-106">La propiedad **EncodedParameters** recupera los parámetros del algoritmo de clave pública.</span><span class="sxs-lookup"><span data-stu-id="6ecc7-106">The **EncodedParameters** property retrieves the parameters of the public key algorithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ecc7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ecc7-107">Syntax</span></span>


```VB
PublicKey.EncodedParameters As EncodedData
```



## <a name="property-value"></a><span data-ttu-id="6ecc7-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="6ecc7-108">Property value</span></span>

<span data-ttu-id="6ecc7-109">Un objeto [**EncodedData**](encodeddata.md) que proporciona acceso a los parámetros del algoritmo de clave pública.</span><span class="sxs-lookup"><span data-stu-id="6ecc7-109">An [**EncodedData**](encodeddata.md) object that provides access to the parameters of the public key algorithm.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ecc7-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ecc7-110">Requirements</span></span>



| <span data-ttu-id="6ecc7-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ecc7-111">Requirement</span></span> | <span data-ttu-id="6ecc7-112">Value</span><span class="sxs-lookup"><span data-stu-id="6ecc7-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ecc7-113">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="6ecc7-113">Redistributable</span></span><br/> | <span data-ttu-id="6ecc7-114">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="6ecc7-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6ecc7-115">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6ecc7-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="6ecc7-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ecc7-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ecc7-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ecc7-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ecc7-118">**PublicKey**</span><span class="sxs-lookup"><span data-stu-id="6ecc7-118">**PublicKey**</span></span>](publickey.md)
</dt> </dl>

 

 
