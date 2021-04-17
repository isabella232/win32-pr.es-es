---
description: Establece o recupera una cadena que contiene un valor de cadena OID de EKU tal y como se define en Wincrypt. h.
ms.assetid: 2fdaeddc-5ed6-46a6-a4f7-827a605e890a
title: 'IEKU:: OID (propiedad)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKU.OID
- IEKU.get_OID
- IEKU.put_OID
- EKU.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 77a519051d2bd1cb3c948bf0e2271cced7d80a20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671237"
---
# <a name="iekuoid-property"></a><span data-ttu-id="70a5e-103">IEKU:: OID (propiedad)</span><span class="sxs-lookup"><span data-stu-id="70a5e-103">IEKU::OID property</span></span>

<span data-ttu-id="70a5e-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="70a5e-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="70a5e-105">En su lugar, use la [**clase X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="70a5e-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="70a5e-106">La propiedad **OID** establece o recupera una cadena que contiene un valor de cadena OID de EKU tal y como se define en Wincrypt. h.</span><span class="sxs-lookup"><span data-stu-id="70a5e-106">The **OID** property sets or retrieves a string that contains an EKU OID string value as defined in Wincrypt.h.</span></span>

<span data-ttu-id="70a5e-107">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="70a5e-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="70a5e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="70a5e-108">Syntax</span></span>


```VB
EKU.OID As String
```



## <a name="property-value"></a><span data-ttu-id="70a5e-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="70a5e-109">Property value</span></span>

<span data-ttu-id="70a5e-110">Cadena que contiene el valor de cadena OID del EKU tal y como se define en Wincrypt. h.</span><span class="sxs-lookup"><span data-stu-id="70a5e-110">String that contains the EKU OID string value as defined in Wincrypt.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="70a5e-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="70a5e-111">Remarks</span></span>

<span data-ttu-id="70a5e-112">Esta propiedad no utiliza el objeto [**OID**](oid.md) incluido en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="70a5e-112">This property does not use the [**OID**](oid.md) object introduced in CAPICOM 2.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="70a5e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70a5e-113">Requirements</span></span>



| <span data-ttu-id="70a5e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="70a5e-114">Requirement</span></span> | <span data-ttu-id="70a5e-115">Value</span><span class="sxs-lookup"><span data-stu-id="70a5e-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="70a5e-116">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="70a5e-116">End of client support</span></span><br/> | <span data-ttu-id="70a5e-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="70a5e-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="70a5e-118">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="70a5e-118">End of server support</span></span><br/> | <span data-ttu-id="70a5e-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="70a5e-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="70a5e-120">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="70a5e-120">Redistributable</span></span><br/>       | <span data-ttu-id="70a5e-121">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="70a5e-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="70a5e-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="70a5e-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="70a5e-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70a5e-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
