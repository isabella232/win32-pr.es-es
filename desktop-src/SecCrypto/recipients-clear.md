---
description: Quita todos los objetos de certificado de una colección de destinatarios.
ms.assetid: 456fcfbc-4388-40f4-ab58-04508ee2141b
title: Recipients. Clear (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Clear
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7d9bd711bbc97997045989f2eb4ffdbc51ae3559
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690189"
---
# <a name="recipientsclear-method"></a><span data-ttu-id="493bd-103">Recipients. Clear (método)</span><span class="sxs-lookup"><span data-stu-id="493bd-103">Recipients.Clear method</span></span>

<span data-ttu-id="493bd-104">\[El método **Clear** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="493bd-104">\[The **Clear** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="493bd-105">En su lugar, use la [**clase CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="493bd-105">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="493bd-106">El método **Clear** quita todos los objetos de [**certificado**](certificate.md) de una colección de [**destinatarios**](recipients.md) .</span><span class="sxs-lookup"><span data-stu-id="493bd-106">The **Clear** method removes all [**Certificate**](certificate.md) objects from a [**Recipients**](recipients.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="493bd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="493bd-107">Syntax</span></span>


```VB
Recipients.Clear()
```



## <a name="parameters"></a><span data-ttu-id="493bd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="493bd-108">Parameters</span></span>

<span data-ttu-id="493bd-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="493bd-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="493bd-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="493bd-110">Return value</span></span>

<span data-ttu-id="493bd-111">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="493bd-111">This method does not return a value.</span></span> <span data-ttu-id="493bd-112">Una aplicación que utiliza este método debe contener código para controlar una excepción generada por este método.</span><span class="sxs-lookup"><span data-stu-id="493bd-112">An application that uses this method must contain code to handle an exception raised by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="493bd-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="493bd-113">Requirements</span></span>



| <span data-ttu-id="493bd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="493bd-114">Requirement</span></span> | <span data-ttu-id="493bd-115">Value</span><span class="sxs-lookup"><span data-stu-id="493bd-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="493bd-116">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="493bd-116">Redistributable</span></span><br/> | <span data-ttu-id="493bd-117">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="493bd-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="493bd-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="493bd-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="493bd-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="493bd-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="493bd-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="493bd-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="493bd-121">**Objetos de criptografía**</span><span class="sxs-lookup"><span data-stu-id="493bd-121">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="493bd-122">**Recipients**</span><span class="sxs-lookup"><span data-stu-id="493bd-122">**Recipients**</span></span>](recipients.md)
</dt> </dl>

 

 
