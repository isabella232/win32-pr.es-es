---
description: Devuelve un valor booleano que indica si la clave privada está protegida.
ms.assetid: 6a329581-0ff8-45fa-9997-5fcf043287cb
title: PrivateKey. IsProtected, método
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsProtected
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 33ba72935b2c3f9f9cf537469e043160f9ce2d7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671304"
---
# <a name="privatekeyisprotected-method"></a><span data-ttu-id="7abc9-103">PrivateKey. IsProtected, método</span><span class="sxs-lookup"><span data-stu-id="7abc9-103">PrivateKey.IsProtected method</span></span>

<span data-ttu-id="7abc9-104">\[El método **IsProtected** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="7abc9-104">\[The **IsProtected** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7abc9-105">En su lugar, use la [**propiedad X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="7abc9-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="7abc9-106">El método **IsProtected** devuelve un valor booleano que indica si la clave privada está protegida.</span><span class="sxs-lookup"><span data-stu-id="7abc9-106">The **IsProtected** method returns a Boolean value that indicates whether the private key is protected.</span></span>

## <a name="syntax"></a><span data-ttu-id="7abc9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7abc9-107">Syntax</span></span>


```VB
PrivateKey.IsProtected()
```



## <a name="parameters"></a><span data-ttu-id="7abc9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7abc9-108">Parameters</span></span>

<span data-ttu-id="7abc9-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="7abc9-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7abc9-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7abc9-110">Return value</span></span>

<span data-ttu-id="7abc9-111">Si es true, la clave privada está protegida.</span><span class="sxs-lookup"><span data-stu-id="7abc9-111">If true, the private key is protected.</span></span>

## <a name="remarks"></a><span data-ttu-id="7abc9-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7abc9-112">Remarks</span></span>

<span data-ttu-id="7abc9-113">El valor devuelto de este método depende del [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) utilizado.</span><span class="sxs-lookup"><span data-stu-id="7abc9-113">The return value of this method is dependent on the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) used.</span></span> <span data-ttu-id="7abc9-114">Este método devolverá un valor de confianza si se usa un CSP de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7abc9-114">This method will return a trustworthy value if a Microsoft CSP is used.</span></span> <span data-ttu-id="7abc9-115">Si el CSP no es un CSP de Microsoft, el valor devuelto no puede ser de confianza para ser preciso.</span><span class="sxs-lookup"><span data-stu-id="7abc9-115">If the CSP is not a Microsoft CSP, the return value cannot be trusted to be accurate.</span></span>

## <a name="requirements"></a><span data-ttu-id="7abc9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7abc9-116">Requirements</span></span>



| <span data-ttu-id="7abc9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7abc9-117">Requirement</span></span> | <span data-ttu-id="7abc9-118">Value</span><span class="sxs-lookup"><span data-stu-id="7abc9-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7abc9-119">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="7abc9-119">Redistributable</span></span><br/> | <span data-ttu-id="7abc9-120">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="7abc9-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7abc9-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7abc9-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="7abc9-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7abc9-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7abc9-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="7abc9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7abc9-124">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="7abc9-124">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
