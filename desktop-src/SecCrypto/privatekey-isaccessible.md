---
description: Devuelve un valor booleano que indica si se puede tener acceso a la clave privada.
ms.assetid: ee5e89af-745e-4a4d-9943-fecbaee5d3e3
title: PrivateKey. IsAccessible, método
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsAccessible
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9997fad702ab1eddbf4c60fa2304df8185ef4c63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690661"
---
# <a name="privatekeyisaccessible-method"></a><span data-ttu-id="10aa1-103">PrivateKey. IsAccessible, método</span><span class="sxs-lookup"><span data-stu-id="10aa1-103">PrivateKey.IsAccessible method</span></span>

<span data-ttu-id="10aa1-104">\[El método **IsAccessible** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="10aa1-104">\[The **IsAccessible** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="10aa1-105">En su lugar, use la [**propiedad X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="10aa1-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="10aa1-106">El método **IsAccessible** devuelve un valor booleano que indica si se puede tener acceso a la clave privada.</span><span class="sxs-lookup"><span data-stu-id="10aa1-106">The **IsAccessible** method returns a Boolean value that indicates whether the private key is accessible.</span></span>

## <a name="syntax"></a><span data-ttu-id="10aa1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="10aa1-107">Syntax</span></span>


```VB
PrivateKey.IsAccessible()
```



## <a name="parameters"></a><span data-ttu-id="10aa1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="10aa1-108">Parameters</span></span>

<span data-ttu-id="10aa1-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="10aa1-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="10aa1-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="10aa1-110">Return value</span></span>

<span data-ttu-id="10aa1-111">Si es true, se puede tener acceso a la clave privada.</span><span class="sxs-lookup"><span data-stu-id="10aa1-111">If true, the private key is accessible.</span></span>

## <a name="remarks"></a><span data-ttu-id="10aa1-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="10aa1-112">Remarks</span></span>

<span data-ttu-id="10aa1-113">El valor devuelto de este método depende del [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) utilizado.</span><span class="sxs-lookup"><span data-stu-id="10aa1-113">The return value of this method is dependent on the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) used.</span></span> <span data-ttu-id="10aa1-114">Este método devolverá un valor de confianza si se usa un CSP de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="10aa1-114">This method will return a trustworthy value if a Microsoft CSP is used.</span></span> <span data-ttu-id="10aa1-115">Si el CSP no es un CSP de Microsoft, el valor devuelto no puede ser de confianza para ser preciso.</span><span class="sxs-lookup"><span data-stu-id="10aa1-115">If the CSP is not a Microsoft CSP, the return value cannot be trusted to be accurate.</span></span>

## <a name="requirements"></a><span data-ttu-id="10aa1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10aa1-116">Requirements</span></span>



| <span data-ttu-id="10aa1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="10aa1-117">Requirement</span></span> | <span data-ttu-id="10aa1-118">Value</span><span class="sxs-lookup"><span data-stu-id="10aa1-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="10aa1-119">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="10aa1-119">Redistributable</span></span><br/> | <span data-ttu-id="10aa1-120">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="10aa1-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="10aa1-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="10aa1-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="10aa1-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10aa1-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10aa1-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="10aa1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10aa1-124">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="10aa1-124">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
