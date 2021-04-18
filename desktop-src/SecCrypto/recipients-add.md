---
description: Agrega un objeto de certificado a una colección de destinatarios.
ms.assetid: 2a1b9e0f-ccbf-4042-871b-397de6b6fc35
title: Recipients. Add (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 255d17485e3423d50cd86b092c2120605f0f1106
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670654"
---
# <a name="recipientsadd-method"></a><span data-ttu-id="b7faf-103">Recipients. Add (método)</span><span class="sxs-lookup"><span data-stu-id="b7faf-103">Recipients.Add method</span></span>

<span data-ttu-id="b7faf-104">\[El método **Add** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="b7faf-104">\[The **Add** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b7faf-105">En su lugar, use la [**clase CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="b7faf-105">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="b7faf-106">El método **Add** agrega un objeto de [**certificado**](certificate.md) a una colección de [**destinatarios**](recipients.md) .</span><span class="sxs-lookup"><span data-stu-id="b7faf-106">The **Add** method adds a [**Certificate**](certificate.md) object to a [**Recipients**](recipients.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7faf-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b7faf-107">Syntax</span></span>


```VB
Recipients.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a><span data-ttu-id="b7faf-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b7faf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7faf-109">*Certificado* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b7faf-109">*Certificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7faf-110">Expresión que se resuelve en el objeto de [**certificado**](certificate.md) que se va a agregar a la colección.</span><span class="sxs-lookup"><span data-stu-id="b7faf-110">Expression that resolves to the [**Certificate**](certificate.md) object to be added to the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7faf-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b7faf-111">Return value</span></span>

<span data-ttu-id="b7faf-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b7faf-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7faf-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7faf-113">Requirements</span></span>



| <span data-ttu-id="b7faf-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7faf-114">Requirement</span></span> | <span data-ttu-id="b7faf-115">Value</span><span class="sxs-lookup"><span data-stu-id="b7faf-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7faf-116">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="b7faf-116">Redistributable</span></span><br/> | <span data-ttu-id="b7faf-117">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="b7faf-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b7faf-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b7faf-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="b7faf-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7faf-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7faf-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="b7faf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7faf-121">**Objetos de criptografía**</span><span class="sxs-lookup"><span data-stu-id="b7faf-121">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="b7faf-122">**Recipients**</span><span class="sxs-lookup"><span data-stu-id="b7faf-122">**Recipients**</span></span>](recipients.md)
</dt> </dl>

 

 
