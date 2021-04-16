---
description: Establece o recupera la clave privada asociada al certificado.
ms.assetid: 976d81b4-5cbe-4824-9087-9a908b0e60e5
title: Propiedad Certificate. PrivateKey
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.PrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: eed2297a4546250cfe9e360029f11b2e4e6e67d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671847"
---
# <a name="certificateprivatekey-property"></a><span data-ttu-id="b2a09-103">Propiedad Certificate. PrivateKey</span><span class="sxs-lookup"><span data-stu-id="b2a09-103">Certificate.PrivateKey property</span></span>

<span data-ttu-id="b2a09-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b2a09-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="b2a09-105">En su lugar, use la [**clase X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="b2a09-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="b2a09-106">La propiedad **PrivateKey** establece o recupera la clave privada asociada al certificado.</span><span class="sxs-lookup"><span data-stu-id="b2a09-106">The **PrivateKey** property sets or retrieves the private key associated with the certificate.</span></span> <span data-ttu-id="b2a09-107">Esta propiedad se incorporó en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="b2a09-107">This property was introduced in CAPICOM 2.0.</span></span>

<span data-ttu-id="b2a09-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b2a09-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2a09-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b2a09-109">Syntax</span></span>


```VB
Certificate.PrivateKey As PrivateKey
```



## <a name="property-value"></a><span data-ttu-id="b2a09-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b2a09-110">Property value</span></span>

<span data-ttu-id="b2a09-111">Objeto [**PrivateKey**](privatekey.md) que representa la clave privada asociada al certificado.</span><span class="sxs-lookup"><span data-stu-id="b2a09-111">A [**PrivateKey**](privatekey.md) object that represents the private key that is associated with the certificate.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2a09-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b2a09-112">Remarks</span></span>

<span data-ttu-id="b2a09-113">Al establecer la propiedad **PrivateKey** en Nothing, se quita la asociación entre la clave privada y el certificado, pero no se elimina la clave privada.</span><span class="sxs-lookup"><span data-stu-id="b2a09-113">Setting the **PrivateKey** property to Nothing removes the association between the private key and the certificate, but it does not delete the private key.</span></span> <span data-ttu-id="b2a09-114">Para eliminar la clave privada, llame al método [**privatekey. Delete**](privatekey-delete.md) y, a continuación, establezca esta propiedad en Nothing.</span><span class="sxs-lookup"><span data-stu-id="b2a09-114">To delete the private key, call the [**PrivateKey.Delete**](privatekey-delete.md) method, and then set this property to Nothing.</span></span>

<span data-ttu-id="b2a09-115">Esta propiedad produce CAPICOM \_ E \_ no \_ se permite cuando se establece desde una aplicación basada en Web.</span><span class="sxs-lookup"><span data-stu-id="b2a09-115">This property raises CAPICOM\_E\_NOT\_ALLOWED when it is set from a web-based application.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2a09-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2a09-116">Requirements</span></span>



| <span data-ttu-id="b2a09-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2a09-117">Requirement</span></span> | <span data-ttu-id="b2a09-118">Value</span><span class="sxs-lookup"><span data-stu-id="b2a09-118">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2a09-119">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="b2a09-119">End of client support</span></span><br/> | <span data-ttu-id="b2a09-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b2a09-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b2a09-121">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="b2a09-121">End of server support</span></span><br/> | <span data-ttu-id="b2a09-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b2a09-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b2a09-123">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="b2a09-123">Redistributable</span></span><br/>       | <span data-ttu-id="b2a09-124">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="b2a09-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b2a09-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b2a09-125">DLL</span></span><br/>                   | <dl> <span data-ttu-id="b2a09-126"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2a09-126"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2a09-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2a09-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2a09-128">**Certificado**</span><span class="sxs-lookup"><span data-stu-id="b2a09-128">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
