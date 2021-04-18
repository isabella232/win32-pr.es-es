---
description: Quita un objeto de certificado único de la colección.
ms.assetid: dff82825-1a7d-4c1a-94e2-7f9d1281ecf2
title: 'ICertificates2:: Remove (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Remove
- ICertificates2.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6a2f9336a420f1d014e178f67cae02cf85f0fd44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690820"
---
# <a name="icertificates2remove-method"></a><span data-ttu-id="df0b8-103">ICertificates2:: Remove (método)</span><span class="sxs-lookup"><span data-stu-id="df0b8-103">ICertificates2::Remove method</span></span>

<span data-ttu-id="df0b8-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="df0b8-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="df0b8-105">En su lugar, use la [**clase X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="df0b8-105">Instead, use the [**X509Certificate2Collection Class**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="df0b8-106">El método **Remove** quita un objeto de [**certificado**](certificate.md) único de la colección.</span><span class="sxs-lookup"><span data-stu-id="df0b8-106">The **Remove** method removes a single [**Certificate**](certificate.md) object from the collection.</span></span> <span data-ttu-id="df0b8-107">Este método se presentó en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="df0b8-107">This method was introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="df0b8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="df0b8-108">Syntax</span></span>


```VB
Certificates.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a><span data-ttu-id="df0b8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="df0b8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df0b8-110">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="df0b8-110">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df0b8-111">Valor de índice del objeto de [**certificado**](certificate.md) que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="df0b8-111">Index value for the [**Certificate**](certificate.md) object to be removed.</span></span> <span data-ttu-id="df0b8-112">Este parámetro puede ser uno de los siguientes tipos posibles.</span><span class="sxs-lookup"><span data-stu-id="df0b8-112">This parameter can be one of the following possible types.</span></span>



| <span data-ttu-id="df0b8-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="df0b8-113">Type</span></span>                                                                                                                                                                                                                                                              | <span data-ttu-id="df0b8-114">Significado</span><span class="sxs-lookup"><span data-stu-id="df0b8-114">Meaning</span></span>                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Long"></span><span id="long"></span><span id="LONG"></span><dl> <span data-ttu-id="df0b8-115"><dt>\* \* \* \* Largo \* \*</dt> \* \* <dt></dt></span><span class="sxs-lookup"><span data-stu-id="df0b8-115"><dt>\*\*\*\*Long\*\*\*\*</dt> <dt></dt></span></span> </dl>                                                | <span data-ttu-id="df0b8-116">Se quita el objeto de [**certificado**](certificate.md) que se encuentra en el índice especificado de la colección.</span><span class="sxs-lookup"><span data-stu-id="df0b8-116">The [**Certificate**](certificate.md) object at the specified index into the collection is removed.</span></span><br/>                                                                                                          |
| <span id="String"></span><span id="string"></span><span id="STRING"></span><dl> <span data-ttu-id="df0b8-117">\* \* \* \* <dt>Cadena \* \*</dt> \* \*<dt></dt></span><span class="sxs-lookup"><span data-stu-id="df0b8-117"><dt>\*\*\*\*String\*\*\*\*</dt> <dt></dt></span></span> </dl>                                        | <span data-ttu-id="df0b8-118">Se quita el primer objeto de [**certificado**](certificate.md) de la colección que coincide con la huella digital [*SHA-1*](../secgloss/s-gly.md) incluida en la cadena especificada.</span><span class="sxs-lookup"><span data-stu-id="df0b8-118">The first [**Certificate**](certificate.md) object in the collection that matches the [*SHA-1*](../secgloss/s-gly.md) thumbprint contained in the specified string is removed.</span></span><br/> |
| <span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span><dl> <span data-ttu-id="df0b8-119"><dt>**[**Certificado**](certificate.md)**</dt> de <dt></dt></span><span class="sxs-lookup"><span data-stu-id="df0b8-119"><dt>**[**Certificate**](certificate.md)**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="df0b8-120">Se quita el primer objeto de [**certificado**](certificate.md) de la colección que coincide con el objeto de **certificado** especificado.</span><span class="sxs-lookup"><span data-stu-id="df0b8-120">The first [**Certificate**](certificate.md) object in the collection that matches the specified **Certificate** object is removed.</span></span><br/>                                                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df0b8-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="df0b8-121">Return value</span></span>

<span data-ttu-id="df0b8-122">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="df0b8-122">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="df0b8-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df0b8-123">Requirements</span></span>



| <span data-ttu-id="df0b8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="df0b8-124">Requirement</span></span> | <span data-ttu-id="df0b8-125">Value</span><span class="sxs-lookup"><span data-stu-id="df0b8-125">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="df0b8-126">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="df0b8-126">End of client support</span></span><br/> | <span data-ttu-id="df0b8-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="df0b8-127">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="df0b8-128">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="df0b8-128">End of server support</span></span><br/> | <span data-ttu-id="df0b8-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df0b8-129">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="df0b8-130">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="df0b8-130">Redistributable</span></span><br/>       | <span data-ttu-id="df0b8-131">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="df0b8-131">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="df0b8-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="df0b8-132">DLL</span></span><br/>                   | <dl> <span data-ttu-id="df0b8-133"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df0b8-133"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
