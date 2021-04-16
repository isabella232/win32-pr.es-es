---
description: Recupera la especificación de clave.
ms.assetid: 93c909cb-b1d1-4c2b-a66c-9d3f6dd9b340
title: PrivateKey. Especificación de la propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.KeySpec
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f9d0ba55ca48d5257a038845f84374544b7615b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671303"
---
# <a name="privatekeykeyspec-property"></a><span data-ttu-id="a65cd-103">PrivateKey. Especificación de la propiedad</span><span class="sxs-lookup"><span data-stu-id="a65cd-103">PrivateKey.KeySpec property</span></span>

<span data-ttu-id="a65cd-104">\[La propiedad especificada por **especificación** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="a65cd-104">\[The **KeySpec** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a65cd-105">En su lugar, use la [**propiedad X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="a65cd-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="a65cd-106">La **propiedad especificación de clave** recupera la especificación de clave.</span><span class="sxs-lookup"><span data-stu-id="a65cd-106">The **KeySpec** property retrieves the key specification.</span></span>

## <a name="syntax"></a><span data-ttu-id="a65cd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a65cd-107">Syntax</span></span>


```VB
PrivateKey.KeySpec As CAPICOM_KEY_SPEC
```



## <a name="property-value"></a><span data-ttu-id="a65cd-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a65cd-108">Property value</span></span>

<span data-ttu-id="a65cd-109">Un valor de la enumeración de la especificación de [**\_ \_ clave CAPICOM**](capicom-key-spec.md) que indica la especificación de clave.</span><span class="sxs-lookup"><span data-stu-id="a65cd-109">A value of the [**CAPICOM\_KEY\_SPEC**](capicom-key-spec.md) enumeration that indicates the key specification.</span></span> <span data-ttu-id="a65cd-110">En la siguiente tabla se muestran los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="a65cd-110">The following table shows the possible values.</span></span>



| <span data-ttu-id="a65cd-111">Valor</span><span class="sxs-lookup"><span data-stu-id="a65cd-111">Value</span></span>                                                                                                                                                                                                        | <span data-ttu-id="a65cd-112">Significado</span><span class="sxs-lookup"><span data-stu-id="a65cd-112">Meaning</span></span>                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="CAPICOM_KEY_SPEC_KEYEXCHANGE"></span><span id="capicom_key_spec_keyexchange"></span><dl> <span data-ttu-id="a65cd-113"><dt>**\_KEYEXCHANGE de \_ especificación de clave CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a65cd-113"><dt>**CAPICOM\_KEY\_SPEC\_KEYEXCHANGE**</dt></span></span> </dl> | <span data-ttu-id="a65cd-114">La clave se puede utilizar para el cifrado y la firma.</span><span class="sxs-lookup"><span data-stu-id="a65cd-114">The key can be used for encryption and signing.</span></span><br/> |
| <span id="CAPICOM_KEY_SPEC_SIGNATURE"></span><span id="capicom_key_spec_signature"></span><dl> <span data-ttu-id="a65cd-115"><dt>**firma de la \_ especificación de clave CAPICOM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a65cd-115"><dt>**CAPICOM\_KEY\_SPEC\_SIGNATURE**</dt></span></span> </dl>       | <span data-ttu-id="a65cd-116">La clave solo se puede utilizar para firmar.</span><span class="sxs-lookup"><span data-stu-id="a65cd-116">The key can be used only for signing.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="a65cd-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a65cd-117">Requirements</span></span>



| <span data-ttu-id="a65cd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a65cd-118">Requirement</span></span> | <span data-ttu-id="a65cd-119">Value</span><span class="sxs-lookup"><span data-stu-id="a65cd-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a65cd-120">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="a65cd-120">Redistributable</span></span><br/> | <span data-ttu-id="a65cd-121">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="a65cd-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a65cd-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a65cd-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="a65cd-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a65cd-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a65cd-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="a65cd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a65cd-125">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="a65cd-125">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
