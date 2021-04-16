---
description: Representa una propiedad de uso de clave extendida (EKU) de un certificado.
ms.assetid: 08eb7c77-0224-4ab5-99e7-edf18eb23c60
title: Objeto EKU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKU
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ff397ae747ecd09dd1292e5c15eb4291692d9651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671451"
---
# <a name="eku-object"></a><span data-ttu-id="69edc-103">Objeto EKU</span><span class="sxs-lookup"><span data-stu-id="69edc-103">EKU object</span></span>

<span data-ttu-id="69edc-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="69edc-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="69edc-105">En su lugar, use la [**clase X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="69edc-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="69edc-106">El objeto **EKU** representa una única propiedad de uso de clave extendida (EKU) de un certificado.</span><span class="sxs-lookup"><span data-stu-id="69edc-106">The **EKU** object represents a single extended key usage (EKU) property of a certificate.</span></span>

## <a name="members"></a><span data-ttu-id="69edc-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="69edc-107">Members</span></span>

<span data-ttu-id="69edc-108">El objeto **EKU** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="69edc-108">The **EKU** object has these types of members:</span></span>

-   [<span data-ttu-id="69edc-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="69edc-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="69edc-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="69edc-110">Properties</span></span>

<span data-ttu-id="69edc-111">El objeto **EKU** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="69edc-111">The **EKU** object has these properties.</span></span>



| <span data-ttu-id="69edc-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="69edc-112">Property</span></span>                            | <span data-ttu-id="69edc-113">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="69edc-113">Access type</span></span>           | <span data-ttu-id="69edc-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="69edc-114">Description</span></span>                                                                                                                                                                                                   |
|:------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="69edc-115">**Name**</span><span class="sxs-lookup"><span data-stu-id="69edc-115">**Name**</span></span>](eku-name.md)<br/> | <span data-ttu-id="69edc-116">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="69edc-116">Read/write</span></span><br/> | <span data-ttu-id="69edc-117">Establece o recupera un valor de enumeración que especifica el nombre de CAPICOM del EKU.</span><span class="sxs-lookup"><span data-stu-id="69edc-117">Sets or retrieves an enumeration value that specifies the CAPICOM name of the EKU.</span></span> <span data-ttu-id="69edc-118">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="69edc-118">This is the default property.</span></span><br/>                                                                                   |
| [<span data-ttu-id="69edc-119">**OID**</span><span class="sxs-lookup"><span data-stu-id="69edc-119">**OID**</span></span>](eku-oid.md)<br/>   | <span data-ttu-id="69edc-120">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="69edc-120">Read/write</span></span><br/> | <span data-ttu-id="69edc-121">Establece o recupera una cadena que contiene un valor de cadena de [*identificador de objeto*](../secgloss/o-gly.md) (OID) de EKU tal y como se define en Wincrypt. h.</span><span class="sxs-lookup"><span data-stu-id="69edc-121">Sets or retrieves a string that contains an EKU [*object identifier*](../secgloss/o-gly.md) (OID) string value as defined in Wincrypt.h.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="69edc-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69edc-122">Remarks</span></span>

<span data-ttu-id="69edc-123">El objeto **EKU** se usa en la colección y la propiedad siguientes:</span><span class="sxs-lookup"><span data-stu-id="69edc-123">The **EKU** object is used by the following collection and property:</span></span>

-   <span data-ttu-id="69edc-124">[**EKU**](ekus.md) (colección)</span><span class="sxs-lookup"><span data-stu-id="69edc-124">[**EKUs**](ekus.md) collection</span></span>
-   <span data-ttu-id="69edc-125">Propiedad [**CertificateStatus. EKU**](certificatestatus-eku.md)</span><span class="sxs-lookup"><span data-stu-id="69edc-125">[**CertificateStatus.EKU**](certificatestatus-eku.md) property</span></span>

<span data-ttu-id="69edc-126">No se puede crear el objeto **EKU** .</span><span class="sxs-lookup"><span data-stu-id="69edc-126">The **EKU** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="69edc-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69edc-127">Requirements</span></span>



| <span data-ttu-id="69edc-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="69edc-128">Requirement</span></span> | <span data-ttu-id="69edc-129">Value</span><span class="sxs-lookup"><span data-stu-id="69edc-129">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="69edc-130">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="69edc-130">End of client support</span></span><br/> | <span data-ttu-id="69edc-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="69edc-131">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="69edc-132">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="69edc-132">End of server support</span></span><br/> | <span data-ttu-id="69edc-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69edc-133">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="69edc-134">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="69edc-134">Redistributable</span></span><br/>       | <span data-ttu-id="69edc-135">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="69edc-135">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="69edc-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="69edc-136">DLL</span></span><br/>                   | <dl> <span data-ttu-id="69edc-137"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69edc-137"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
