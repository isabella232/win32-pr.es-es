---
description: Recupera una cadena que contiene el nombre del emisor del certificado.
ms.assetid: 6cf528e3-061a-44dc-b320-0e4b48a6c6ab
title: Propiedad Certificate. IssuerName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.IssuerName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6b34b3bf198759d08fd3d0e3e4261407389a69a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670826"
---
# <a name="certificateissuername-property"></a><span data-ttu-id="bc84e-103">Propiedad Certificate. IssuerName</span><span class="sxs-lookup"><span data-stu-id="bc84e-103">Certificate.IssuerName property</span></span>

<span data-ttu-id="bc84e-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bc84e-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="bc84e-105">En su lugar, use la [**clase X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="bc84e-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="bc84e-106">La propiedad **IssuerName** recupera una cadena que contiene el nombre del emisor del certificado.</span><span class="sxs-lookup"><span data-stu-id="bc84e-106">The **IssuerName** property retrieves a string that contains the name of the certificate issuer.</span></span>

<span data-ttu-id="bc84e-107">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bc84e-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc84e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bc84e-108">Syntax</span></span>


```VB
Certificate.IssuerName As String
```



## <a name="property-value"></a><span data-ttu-id="bc84e-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="bc84e-109">Property value</span></span>

<span data-ttu-id="bc84e-110">Cadena que contiene el nombre del emisor del certificado.</span><span class="sxs-lookup"><span data-stu-id="bc84e-110">String that contains the name of the certificate issuer.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc84e-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc84e-111">Requirements</span></span>



| <span data-ttu-id="bc84e-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc84e-112">Requirement</span></span> | <span data-ttu-id="bc84e-113">Value</span><span class="sxs-lookup"><span data-stu-id="bc84e-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc84e-114">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="bc84e-114">End of client support</span></span><br/> | <span data-ttu-id="bc84e-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bc84e-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="bc84e-116">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="bc84e-116">End of server support</span></span><br/> | <span data-ttu-id="bc84e-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc84e-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="bc84e-118">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="bc84e-118">Redistributable</span></span><br/>       | <span data-ttu-id="bc84e-119">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="bc84e-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="bc84e-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bc84e-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="bc84e-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc84e-121"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
