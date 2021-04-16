---
description: Establece o recupera el objeto de certificado que representa el certificado de un firmante de los datos.
ms.assetid: 92ac209e-59b5-4a75-922d-d61629ca41b1
title: Propiedad Signer. Certificate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Certificate
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 96652f85e6058682dedd3370965ea7ff2408b3b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689974"
---
# <a name="signercertificate-property"></a><span data-ttu-id="a8f36-103">Propiedad Signer. Certificate</span><span class="sxs-lookup"><span data-stu-id="a8f36-103">Signer.Certificate property</span></span>

<span data-ttu-id="a8f36-104">\[La propiedad de **certificado** está disponible para su uso en los sistemas operativos especificados en la sección requisitos.</span><span class="sxs-lookup"><span data-stu-id="a8f36-104">\[The **Certificate** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a8f36-105">En su lugar, use la [**clase CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="a8f36-105">Instead, use the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="a8f36-106">La propiedad de **certificado** establece o recupera el objeto de [**certificado**](certificate.md) que representa el certificado de un firmante de los datos.</span><span class="sxs-lookup"><span data-stu-id="a8f36-106">The **Certificate** property sets or retrieves the [**Certificate**](certificate.md) object that represents the certificate of a signer of the data.</span></span> <span data-ttu-id="a8f36-107">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a8f36-107">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8f36-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a8f36-108">Syntax</span></span>


```VB
Signer.Certificate As Certificate
```



## <a name="property-value"></a><span data-ttu-id="a8f36-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a8f36-109">Property value</span></span>

<span data-ttu-id="a8f36-110">Objeto de [**certificado**](certificate.md) que representa el certificado de un firmante de los datos.</span><span class="sxs-lookup"><span data-stu-id="a8f36-110">The [**Certificate**](certificate.md) object that represents the certificate of a signer of the data.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8f36-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8f36-111">Remarks</span></span>

<span data-ttu-id="a8f36-112">Cuando el valor de esta propiedad se restablece, directa o indirectamente, se restablece el [*Estado*](../secgloss/s-gly.md) completo del objeto.</span><span class="sxs-lookup"><span data-stu-id="a8f36-112">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8f36-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8f36-113">Requirements</span></span>



| <span data-ttu-id="a8f36-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8f36-114">Requirement</span></span> | <span data-ttu-id="a8f36-115">Value</span><span class="sxs-lookup"><span data-stu-id="a8f36-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8f36-116">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="a8f36-116">Redistributable</span></span><br/> | <span data-ttu-id="a8f36-117">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="a8f36-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a8f36-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a8f36-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="a8f36-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8f36-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8f36-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8f36-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8f36-121">**Firmante**</span><span class="sxs-lookup"><span data-stu-id="a8f36-121">**Signer**</span></span>](signer.md)
</dt> </dl>

 

 
