---
description: Quita un objeto de certificado de una colección de destinatarios.
ms.assetid: bb75f6d0-4bab-40dd-9d0c-f0431da9c5f3
title: Recipients. Remove (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 06d276e2d8e75e8822cee3503a7e8342a94a6b0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690188"
---
# <a name="recipientsremove-method"></a><span data-ttu-id="35fa4-103">Recipients. Remove (método)</span><span class="sxs-lookup"><span data-stu-id="35fa4-103">Recipients.Remove method</span></span>

<span data-ttu-id="35fa4-104">\[El método **Remove** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="35fa4-104">\[The **Remove** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="35fa4-105">En su lugar, use la [**clase CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="35fa4-105">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="35fa4-106">El método **Remove** quita un objeto de [**certificado**](certificate.md) de una colección de [**destinatarios**](recipients.md) .</span><span class="sxs-lookup"><span data-stu-id="35fa4-106">The **Remove** method removes a [**Certificate**](certificate.md) object from a [**Recipients**](recipients.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="35fa4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35fa4-107">Syntax</span></span>


```VB
Recipients.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a><span data-ttu-id="35fa4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="35fa4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35fa4-109">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="35fa4-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35fa4-110">Índice del objeto de [**certificado**](certificate.md) que se va a quitar de la colección.</span><span class="sxs-lookup"><span data-stu-id="35fa4-110">Index of the [**Certificate**](certificate.md) object to be removed from the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35fa4-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="35fa4-111">Return value</span></span>

<span data-ttu-id="35fa4-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="35fa4-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="35fa4-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35fa4-113">Requirements</span></span>



| <span data-ttu-id="35fa4-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="35fa4-114">Requirement</span></span> | <span data-ttu-id="35fa4-115">Value</span><span class="sxs-lookup"><span data-stu-id="35fa4-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35fa4-116">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="35fa4-116">Redistributable</span></span><br/> | <span data-ttu-id="35fa4-117">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="35fa4-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="35fa4-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="35fa4-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="35fa4-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35fa4-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35fa4-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="35fa4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35fa4-121">**Objetos de criptografía**</span><span class="sxs-lookup"><span data-stu-id="35fa4-121">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="35fa4-122">**Recipients**</span><span class="sxs-lookup"><span data-stu-id="35fa4-122">**Recipients**</span></span>](recipients.md)
</dt> </dl>

 

 
