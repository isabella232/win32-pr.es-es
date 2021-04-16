---
description: Recupera una cadena que contiene el número de serie del certificado.
ms.assetid: d08be744-4ae8-49f9-8b00-48e76c296f2b
title: Propiedad Certificate. SerialNumber
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.SerialNumber
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6dbd9485891cc89e686cef118e12dd43ec400f60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690273"
---
# <a name="certificateserialnumber-property"></a><span data-ttu-id="1f2eb-103">Propiedad Certificate. SerialNumber</span><span class="sxs-lookup"><span data-stu-id="1f2eb-103">Certificate.SerialNumber property</span></span>

<span data-ttu-id="1f2eb-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1f2eb-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="1f2eb-105">En su lugar, use la [**clase X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="1f2eb-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="1f2eb-106">La propiedad **SerialNumber** recupera una cadena que contiene el número de serie del certificado.</span><span class="sxs-lookup"><span data-stu-id="1f2eb-106">The **SerialNumber** property retrieves a string that contains the certificate serial number.</span></span>

<span data-ttu-id="1f2eb-107">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1f2eb-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f2eb-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1f2eb-108">Syntax</span></span>


```VB
Certificate.SerialNumber As String
```



## <a name="property-value"></a><span data-ttu-id="1f2eb-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="1f2eb-109">Property value</span></span>

<span data-ttu-id="1f2eb-110">Cadena que contiene el número de serie del certificado.</span><span class="sxs-lookup"><span data-stu-id="1f2eb-110">A string that contains the certificate serial number.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f2eb-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f2eb-111">Requirements</span></span>



| <span data-ttu-id="1f2eb-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f2eb-112">Requirement</span></span> | <span data-ttu-id="1f2eb-113">Value</span><span class="sxs-lookup"><span data-stu-id="1f2eb-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f2eb-114">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="1f2eb-114">End of client support</span></span><br/> | <span data-ttu-id="1f2eb-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1f2eb-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1f2eb-116">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="1f2eb-116">End of server support</span></span><br/> | <span data-ttu-id="1f2eb-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f2eb-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1f2eb-118">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="1f2eb-118">Redistributable</span></span><br/>       | <span data-ttu-id="1f2eb-119">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="1f2eb-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1f2eb-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1f2eb-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="1f2eb-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f2eb-121"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
