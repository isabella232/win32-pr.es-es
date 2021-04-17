---
description: Devuelve una colección de las extensiones asociadas al certificado.
ms.assetid: 07793061-6f94-4467-bb01-aa65db657658
title: 'ICertificate2:: Extensions (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Extensions
- ICertificate2.Extensions
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: cc96dee9c33bb3f76e1fb17acb2000f9740d1b5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671125"
---
# <a name="icertificate2extensions-method"></a><span data-ttu-id="8117c-103">ICertificate2:: Extensions (método)</span><span class="sxs-lookup"><span data-stu-id="8117c-103">ICertificate2::Extensions method</span></span>

<span data-ttu-id="8117c-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8117c-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="8117c-105">En su lugar, use la [**clase X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="8117c-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="8117c-106">El método **extensions** devuelve una colección de las extensiones asociadas al certificado.</span><span class="sxs-lookup"><span data-stu-id="8117c-106">The **Extensions** method returns a collection of the extensions associated with the certificate.</span></span> <span data-ttu-id="8117c-107">Este método se presenta en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="8117c-107">This method is introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="8117c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8117c-108">Syntax</span></span>


```VB
Certificate.Extensions()
```



## <a name="parameters"></a><span data-ttu-id="8117c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8117c-109">Parameters</span></span>

<span data-ttu-id="8117c-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="8117c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8117c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8117c-111">Return value</span></span>

<span data-ttu-id="8117c-112">Objeto de [**extensiones**](extensions.md) que representa todas las extensiones asociadas al certificado.</span><span class="sxs-lookup"><span data-stu-id="8117c-112">An [**Extensions**](extensions.md) object that represents all of the extensions associated with the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="8117c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8117c-113">Requirements</span></span>



| <span data-ttu-id="8117c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8117c-114">Requirement</span></span> | <span data-ttu-id="8117c-115">Value</span><span class="sxs-lookup"><span data-stu-id="8117c-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8117c-116">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="8117c-116">End of client support</span></span><br/> | <span data-ttu-id="8117c-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8117c-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="8117c-118">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="8117c-118">End of server support</span></span><br/> | <span data-ttu-id="8117c-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8117c-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8117c-120">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="8117c-120">Redistributable</span></span><br/>       | <span data-ttu-id="8117c-121">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="8117c-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8117c-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8117c-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="8117c-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8117c-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
