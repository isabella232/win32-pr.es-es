---
description: Establece o recupera el algoritmo utilizado para la firma, la envoltura y el cifrado de las operaciones. Esta es la propiedad predeterminada.
ms.assetid: e1144a9c-a352-4f73-a91c-ea66f3d61608
title: Propiedad Algorithm.Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 35ff147d8db7fb409787fa938a951dfc0a2320e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670394"
---
# <a name="algorithmname-property"></a><span data-ttu-id="d4468-104">Propiedad Algorithm.Name</span><span class="sxs-lookup"><span data-stu-id="d4468-104">Algorithm.Name property</span></span>

<span data-ttu-id="d4468-105">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d4468-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="d4468-106">En su lugar, use la [**clase AlgorithmIdentifier**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="d4468-106">Instead, use the [**AlgorithmIdentifier Class**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="d4468-107">La propiedad **Name** establece o recupera el algoritmo utilizado para la firma, la envoltura y las operaciones de cifrado.</span><span class="sxs-lookup"><span data-stu-id="d4468-107">The **Name** property sets or retrieves the algorithm used for signing, enveloping, and encrypting operations.</span></span> <span data-ttu-id="d4468-108">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d4468-108">This is the default property.</span></span>

<span data-ttu-id="d4468-109">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d4468-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4468-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d4468-110">Syntax</span></span>


```VB
Algorithm.Name As CAPICOM_ENCRYPTION_ALGORITHM
```



## <a name="property-value"></a><span data-ttu-id="d4468-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d4468-111">Property value</span></span>

<span data-ttu-id="d4468-112">Valor de la enumeración del [**\_ \_ algoritmo de cifrado CAPICOM**](capicom-encryption-algorithm.md) que especifica el algoritmo que se va a utilizar.</span><span class="sxs-lookup"><span data-stu-id="d4468-112">A value of the [**CAPICOM\_ENCRYPTION\_ALGORITHM**](capicom-encryption-algorithm.md) enumeration that specifies which algorithm to use.</span></span> <span data-ttu-id="d4468-113">En la siguiente tabla se muestran los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="d4468-113">The following table shows the possible values.</span></span>



| <span data-ttu-id="d4468-114">Valor</span><span class="sxs-lookup"><span data-stu-id="d4468-114">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="d4468-115">Significado</span><span class="sxs-lookup"><span data-stu-id="d4468-115">Meaning</span></span>                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_RC2"></span><span id="capicom_encryption_algorithm_rc2"></span><dl> <span data-ttu-id="d4468-116"><dt>**\_Algoritmo de cifrado de CAPICOM \_ \_ RC2**</dt></span><span class="sxs-lookup"><span data-stu-id="d4468-116"><dt>**CAPICOM\_ENCRYPTION\_ALGORITHM\_RC2**</dt></span></span> </dl>    | <span data-ttu-id="d4468-117">Use el cifrado RC2.</span><span class="sxs-lookup"><span data-stu-id="d4468-117">Use RC2 encryption.</span></span><br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_RC4"></span><span id="capicom_encryption_algorithm_rc4"></span><dl> <span data-ttu-id="d4468-118"><dt>**\_Algoritmo de cifrado de CAPICOM \_ \_ RC4**</dt></span><span class="sxs-lookup"><span data-stu-id="d4468-118"><dt>**CAPICOM\_ENCRYPTION\_ALGORITHM\_RC4**</dt></span></span> </dl>    | <span data-ttu-id="d4468-119">Usar el cifrado RC4.</span><span class="sxs-lookup"><span data-stu-id="d4468-119">Use RC4 encryption.</span></span><br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_DES"></span><span id="capicom_encryption_algorithm_des"></span><dl> <span data-ttu-id="d4468-120"><dt>**\_ \_ algoritmo des de cifrado de CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d4468-120"><dt>**CAPICOM\_ENCRYPTION\_ALGORITHM\_DES**</dt></span></span> </dl>    | <span data-ttu-id="d4468-121">Use el cifrado DES.</span><span class="sxs-lookup"><span data-stu-id="d4468-121">Use DES encryption.</span></span><br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_3DES"></span><span id="capicom_encryption_algorithm_3des"></span><dl> <span data-ttu-id="d4468-122"><dt>**\_Algoritmo de cifrado \_ \_ 3DES de CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="d4468-122"><dt>**CAPICOM\_ENCRYPTION\_ALGORITHM\_3DES**</dt></span></span> </dl> | <span data-ttu-id="d4468-123">Use el cifrado Triple DES.</span><span class="sxs-lookup"><span data-stu-id="d4468-123">Use triple DES encryption.</span></span><br/> |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_AES"></span><span id="capicom_encryption_algorithm_aes"></span><dl> <span data-ttu-id="d4468-124"><dt>**\_algoritmo de cifrado de CAPICOM \_ \_ AES**</dt></span><span class="sxs-lookup"><span data-stu-id="d4468-124"><dt>**CAPICOM\_ENCRYPTION\_ALGORITHM\_AES**</dt></span></span> </dl>    | <span data-ttu-id="d4468-125">Use el algoritmo AES.</span><span class="sxs-lookup"><span data-stu-id="d4468-125">Use the AES algorithm.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="d4468-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d4468-126">Remarks</span></span>

<span data-ttu-id="d4468-127">Cuando el valor de esta propiedad se restablece, directa o indirectamente, se restablece el estado completo del objeto.</span><span class="sxs-lookup"><span data-stu-id="d4468-127">When the value of this property is reset, directly or indirectly, the whole state of the object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4468-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4468-128">Requirements</span></span>



| <span data-ttu-id="d4468-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4468-129">Requirement</span></span> | <span data-ttu-id="d4468-130">Value</span><span class="sxs-lookup"><span data-stu-id="d4468-130">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4468-131">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="d4468-131">End of client support</span></span><br/> | <span data-ttu-id="d4468-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d4468-132">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d4468-133">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="d4468-133">End of server support</span></span><br/> | <span data-ttu-id="d4468-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d4468-134">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d4468-135">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="d4468-135">Redistributable</span></span><br/>       | <span data-ttu-id="d4468-136">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="d4468-136">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d4468-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d4468-137">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d4468-138"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4468-138"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
