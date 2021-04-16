---
description: Recupera un objeto OID que identifica el objeto de plantilla.
ms.assetid: bdd9d401-e9c4-4307-9817-7dcb55c539f8
title: Template. OID (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4a8599ac999c7d6a3e3403d94ff2c6daf0eba48b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649976"
---
# <a name="templateoid-property"></a><span data-ttu-id="040ef-103">Template. OID (propiedad)</span><span class="sxs-lookup"><span data-stu-id="040ef-103">Template.OID property</span></span>

<span data-ttu-id="040ef-104">\[La propiedad **OID** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="040ef-104">\[The **OID** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="040ef-105">En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID de la plantilla de certificado para recuperar la plantilla de extensión de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="040ef-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="040ef-106">La propiedad **OID** recupera un objeto [**OID**](oid.md) que identifica el objeto de [**plantilla**](template.md) .</span><span class="sxs-lookup"><span data-stu-id="040ef-106">The **OID** property retrieves an [**OID**](oid.md) object that identifies the [**Template**](template.md) object.</span></span>

<span data-ttu-id="040ef-107">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="040ef-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="040ef-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="040ef-108">Syntax</span></span>


```VB
Template.OID As OID
```



## <a name="property-value"></a><span data-ttu-id="040ef-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="040ef-109">Property value</span></span>

<span data-ttu-id="040ef-110">Objeto [**OID**](oid.md) que identifica el objeto de [**plantilla**](template.md) .</span><span class="sxs-lookup"><span data-stu-id="040ef-110">An [**OID**](oid.md) object that identifies the [**Template**](template.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="040ef-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="040ef-111">Requirements</span></span>



| <span data-ttu-id="040ef-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="040ef-112">Requirement</span></span> | <span data-ttu-id="040ef-113">Value</span><span class="sxs-lookup"><span data-stu-id="040ef-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="040ef-114">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="040ef-114">Redistributable</span></span><br/> | <span data-ttu-id="040ef-115">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="040ef-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="040ef-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="040ef-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="040ef-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="040ef-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="040ef-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="040ef-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="040ef-119">**Plantilla**</span><span class="sxs-lookup"><span data-stu-id="040ef-119">**Template**</span></span>](template.md)
</dt> </dl>

 

 
