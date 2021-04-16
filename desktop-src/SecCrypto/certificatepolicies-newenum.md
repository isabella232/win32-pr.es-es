---
description: La \_ propiedad NewEnum de CertificatePolicies recupera una interfaz IEnumVARIANT en un objeto que se puede usar para enumerar la colección.
ms.assetid: 631a11c8-4442-493e-9406-bc63f79db548
title: Propiedad CertificatePolicies._NewEnum
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2d5e90d4b906661119936ca1e893e3b6e17c9bf5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690589"
---
# <a name="certificatepolicies_newenum-property"></a><span data-ttu-id="e8446-103">CertificatePolicies. \_ Propiedad NewEnum</span><span class="sxs-lookup"><span data-stu-id="e8446-103">CertificatePolicies.\_NewEnum property</span></span>

<span data-ttu-id="e8446-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e8446-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="e8446-105">En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para que las directivas de certificado recuperen las directivas de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="e8446-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to retrieve the certificate policies.\]</span></span>

<span data-ttu-id="e8446-106">La propiedad **\_ NewEnum** recupera una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección.</span><span class="sxs-lookup"><span data-stu-id="e8446-106">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="e8446-107">Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="e8446-107">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="e8446-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8446-108">Syntax</span></span>


```VB
CertificatePolicies._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="e8446-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e8446-109">Property value</span></span>

<span data-ttu-id="e8446-110">Una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección.</span><span class="sxs-lookup"><span data-stu-id="e8446-110">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8446-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e8446-111">Remarks</span></span>

<span data-ttu-id="e8446-112">Esta propiedad se utiliza internamente de forma automática cuando se usa la `For Each In` construcción en Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="e8446-112">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="e8446-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8446-113">Requirements</span></span>



| <span data-ttu-id="e8446-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8446-114">Requirement</span></span> | <span data-ttu-id="e8446-115">Value</span><span class="sxs-lookup"><span data-stu-id="e8446-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8446-116">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="e8446-116">End of client support</span></span><br/> | <span data-ttu-id="e8446-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e8446-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e8446-118">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="e8446-118">End of server support</span></span><br/> | <span data-ttu-id="e8446-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8446-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e8446-120">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="e8446-120">Redistributable</span></span><br/>       | <span data-ttu-id="e8446-121">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="e8446-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e8446-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e8446-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="e8446-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8446-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
