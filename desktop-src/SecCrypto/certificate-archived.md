---
description: Establece o recupera un valor booleano que indica si el certificado se ha archivado.
ms.assetid: a6526b0e-e76b-4f03-a6ba-9e380e362364
title: Certificate. Archived (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Archived
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e1d8cdea3e43bbe10ee87f8f4aa605740a15e6ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650197"
---
# <a name="certificatearchived-property"></a><span data-ttu-id="d2ab7-103">Certificate. Archived (propiedad)</span><span class="sxs-lookup"><span data-stu-id="d2ab7-103">Certificate.Archived property</span></span>

<span data-ttu-id="d2ab7-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d2ab7-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="d2ab7-105">En su lugar, use la [**clase X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="d2ab7-105">Instead, use the [**X509Certificate2 Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="d2ab7-106">La propiedad **archivada** establece o recupera un valor booleano que indica si el certificado se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="d2ab7-106">The **Archived** property sets or retrieves a Boolean value that indicates whether the certificate is archived.</span></span>

<span data-ttu-id="d2ab7-107">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d2ab7-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2ab7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d2ab7-108">Syntax</span></span>


```VB
Certificate.Archived As Boolean
```



## <a name="property-value"></a><span data-ttu-id="d2ab7-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d2ab7-109">Property value</span></span>

<span data-ttu-id="d2ab7-110">Valor booleano que indica si el certificado se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="d2ab7-110">A Boolean value that indicates whether the certificate is archived.</span></span> <span data-ttu-id="d2ab7-111">Si es **true**, el certificado se archiva.</span><span class="sxs-lookup"><span data-stu-id="d2ab7-111">If **true**, the certificate is archived.</span></span> <span data-ttu-id="d2ab7-112">Tenga en cuenta que el cambio del valor de **false** a **true** archiva el certificado.</span><span class="sxs-lookup"><span data-stu-id="d2ab7-112">Note that changing the value from **false** to **true** archives the certificate.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2ab7-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d2ab7-113">Remarks</span></span>

<span data-ttu-id="d2ab7-114">Esta propiedad produce CAPICOM \_ E \_ no \_ se permite cuando se genera un script desde una aplicación basada en Web.</span><span class="sxs-lookup"><span data-stu-id="d2ab7-114">This property raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

> [!Note]  
> <span data-ttu-id="d2ab7-115">Un certificado archivado no es visible en la interfaz de usuario de administración de certificados.</span><span class="sxs-lookup"><span data-stu-id="d2ab7-115">An archived certificate is not visible in the certificate management user interface.</span></span> <span data-ttu-id="d2ab7-116">Además, los certificados archivados no se incluirán en el método [**Store. Open**](store-open.md) a menos que \_ \_ se especifique CAPICOM Store Open \_ include \_ .</span><span class="sxs-lookup"><span data-stu-id="d2ab7-116">Also, archived certificates will not be included in the [**Store.Open**](store-open.md) method unless CAPICOM\_STORE\_OPEN\_INCLUDE\_ARCHIVED is specified.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d2ab7-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2ab7-117">Requirements</span></span>



| <span data-ttu-id="d2ab7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2ab7-118">Requirement</span></span> | <span data-ttu-id="d2ab7-119">Value</span><span class="sxs-lookup"><span data-stu-id="d2ab7-119">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2ab7-120">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="d2ab7-120">End of client support</span></span><br/> | <span data-ttu-id="d2ab7-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d2ab7-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d2ab7-122">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="d2ab7-122">End of server support</span></span><br/> | <span data-ttu-id="d2ab7-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2ab7-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d2ab7-124">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="d2ab7-124">Redistributable</span></span><br/>       | <span data-ttu-id="d2ab7-125">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="d2ab7-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d2ab7-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d2ab7-126">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d2ab7-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2ab7-127"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
