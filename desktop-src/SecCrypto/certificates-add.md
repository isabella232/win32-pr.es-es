---
description: Agrega un objeto de certificado a la colección.
ms.assetid: 0973018d-1e83-41b4-a250-7dd5be2fb664
title: 'ICertificates2:: Add (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Add
- ICertificates2.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d56120c6f584e828c3aadca037d75263d5350f48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671281"
---
# <a name="icertificates2add-method"></a><span data-ttu-id="fc962-103">ICertificates2:: Add (método)</span><span class="sxs-lookup"><span data-stu-id="fc962-103">ICertificates2::Add method</span></span>

<span data-ttu-id="fc962-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fc962-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="fc962-105">En su lugar, use la [**clase X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="fc962-105">Instead, use the [**X509Certificate2Collection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="fc962-106">El método **Add** agrega un objeto de [**certificado**](certificate.md) a la colección.</span><span class="sxs-lookup"><span data-stu-id="fc962-106">The **Add** method adds a [**Certificate**](certificate.md) object to the collection.</span></span> <span data-ttu-id="fc962-107">Este método se presenta en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="fc962-107">This method is introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc962-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fc962-108">Syntax</span></span>


```VB
Certificates.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a><span data-ttu-id="fc962-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fc962-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc962-110">*Certificado* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="fc962-110">*Certificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc962-111">Objeto de [**certificado**](certificate.md) que se va a agregar a la colección.</span><span class="sxs-lookup"><span data-stu-id="fc962-111">The [**Certificate**](certificate.md) object to be added to the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc962-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fc962-112">Return value</span></span>

<span data-ttu-id="fc962-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fc962-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc962-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc962-114">Requirements</span></span>



| <span data-ttu-id="fc962-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc962-115">Requirement</span></span> | <span data-ttu-id="fc962-116">Value</span><span class="sxs-lookup"><span data-stu-id="fc962-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc962-117">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="fc962-117">End of client support</span></span><br/> | <span data-ttu-id="fc962-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fc962-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="fc962-119">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="fc962-119">End of server support</span></span><br/> | <span data-ttu-id="fc962-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fc962-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="fc962-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="fc962-121">Redistributable</span></span><br/>       | <span data-ttu-id="fc962-122">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="fc962-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="fc962-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fc962-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="fc962-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc962-124"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
