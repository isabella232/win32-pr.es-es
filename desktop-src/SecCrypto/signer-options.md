---
description: Establece o recupera la opción de certificado del firmante.
ms.assetid: 2362b9d4-d4d8-46fb-8791-7e856827fb31
title: Propiedad Signer. Options
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Options
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c22cf7b9d9ebe7e98e534d62b0a2771391c6cacb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671234"
---
# <a name="signeroptions-property"></a><span data-ttu-id="f9dbd-103">Propiedad Signer. Options</span><span class="sxs-lookup"><span data-stu-id="f9dbd-103">Signer.Options property</span></span>

<span data-ttu-id="f9dbd-104">\[La propiedad **Opciones** está disponible para su uso en los sistemas operativos especificados en la sección requisitos.</span><span class="sxs-lookup"><span data-stu-id="f9dbd-104">\[The **Options** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f9dbd-105">En su lugar, use la [**clase CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="f9dbd-105">Instead, use the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="f9dbd-106">La propiedad **Options** establece o recupera la opción de certificado del firmante.</span><span class="sxs-lookup"><span data-stu-id="f9dbd-106">The **Options** property sets or retrieves the signer's certificate option.</span></span>

<span data-ttu-id="f9dbd-107">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="f9dbd-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9dbd-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f9dbd-108">Syntax</span></span>


```VB
Signer.Options As CAPICOM_CERTIFICATE_INCLUDE_OPTION
```



## <a name="property-value"></a><span data-ttu-id="f9dbd-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f9dbd-109">Property value</span></span>

<span data-ttu-id="f9dbd-110">Un valor de la enumeración de la [**\_ \_ \_ opción incluir certificado de CAPICOM**](capicom-certificate-include-option.md) que especifica la opción de certificado del firmante.</span><span class="sxs-lookup"><span data-stu-id="f9dbd-110">A value of the [**CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION**](capicom-certificate-include-option.md) enumeration that specifies the signer's certificate option.</span></span> <span data-ttu-id="f9dbd-111">El valor predeterminado es el \_ certificado de CAPICOM \_ incluir \_ cadena \_ excepto \_ raíz.</span><span class="sxs-lookup"><span data-stu-id="f9dbd-111">The default value is CAPICOM\_CERTIFICATE\_INCLUDE\_CHAIN\_EXCEPT\_ROOT.</span></span> <span data-ttu-id="f9dbd-112">En la siguiente tabla se muestran los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="f9dbd-112">The following table shows the possible values.</span></span>



| <span data-ttu-id="f9dbd-113">Valor</span><span class="sxs-lookup"><span data-stu-id="f9dbd-113">Value</span></span>                                                                                                                                                                                                                                                             | <span data-ttu-id="f9dbd-114">Significado</span><span class="sxs-lookup"><span data-stu-id="f9dbd-114">Meaning</span></span>                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_INCLUDE_CHAIN_EXCEPT_ROOT"></span><span id="capicom_certificate_include_chain_except_root"></span><dl> <span data-ttu-id="f9dbd-115"><dt>**el \_ certificado de CAPICOM \_ incluye una \_ cadena excepto la \_ \_ raíz**</dt></span><span class="sxs-lookup"><span data-stu-id="f9dbd-115"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_CHAIN\_EXCEPT\_ROOT**</dt></span></span> </dl> | <span data-ttu-id="f9dbd-116">Guarda todos los certificados de la cadena con la excepción de la entidad raíz.</span><span class="sxs-lookup"><span data-stu-id="f9dbd-116">Saves all certificates in the chain with the exception of the root entity.</span></span><br/> |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_WHOLE_CHAIN"></span><span id="capicom_certificate_include_whole_chain"></span><dl> <span data-ttu-id="f9dbd-117"><dt>**el \_ certificado de CAPICOM \_ incluye una \_ \_ cadena entera**</dt></span><span class="sxs-lookup"><span data-stu-id="f9dbd-117"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_WHOLE\_CHAIN**</dt></span></span> </dl>                    | <span data-ttu-id="f9dbd-118">Guarda la cadena de certificados completa.</span><span class="sxs-lookup"><span data-stu-id="f9dbd-118">Saves the complete certificate chain.</span></span><br/>                                      |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_END_ENTITY_ONLY"></span><span id="capicom_certificate_include_end_entity_only"></span><dl> <span data-ttu-id="f9dbd-119"><dt>**el \_ certificado de CAPICOM \_ incluye \_ \_ solo la entidad final \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f9dbd-119"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_END\_ENTITY\_ONLY**</dt></span></span> </dl>       | <span data-ttu-id="f9dbd-120">Guarda solo el certificado de entidad final.</span><span class="sxs-lookup"><span data-stu-id="f9dbd-120">Saves only the end entity certificate.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="f9dbd-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9dbd-121">Requirements</span></span>



| <span data-ttu-id="f9dbd-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9dbd-122">Requirement</span></span> | <span data-ttu-id="f9dbd-123">Value</span><span class="sxs-lookup"><span data-stu-id="f9dbd-123">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9dbd-124">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="f9dbd-124">Redistributable</span></span><br/> | <span data-ttu-id="f9dbd-125">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="f9dbd-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f9dbd-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f9dbd-126">DLL</span></span><br/>             | <dl> <span data-ttu-id="f9dbd-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9dbd-127"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9dbd-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9dbd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9dbd-129">**Firmante**</span><span class="sxs-lookup"><span data-stu-id="f9dbd-129">**Signer**</span></span>](signer.md)
</dt> </dl>

 

 
