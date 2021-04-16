---
description: Recupera un calificador basado en un índice especificado.
ms.assetid: 4d54358d-99de-4a1c-b843-41006f47a279
title: Propiedad Qualifiers. Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 798b1f212aabd5b1ab34a1eefb626be4572b9c1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671406"
---
# <a name="qualifiersitem-property"></a><span data-ttu-id="f01bf-103">Propiedad Qualifiers. Item</span><span class="sxs-lookup"><span data-stu-id="f01bf-103">Qualifiers.Item property</span></span>

<span data-ttu-id="f01bf-104">\[La propiedad **Item** está disponible para su uso en los sistemas operativos especificados en la sección requirements.</span><span class="sxs-lookup"><span data-stu-id="f01bf-104">\[The **Item** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f01bf-105">En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para las directivas de certificado para procesar calificadores que formen parte de la información de directivas en la extensión de directivas de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="f01bf-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="f01bf-106">La propiedad **Item** recupera un calificador basado en un índice especificado.</span><span class="sxs-lookup"><span data-stu-id="f01bf-106">The **Item** property retrieves a qualifier based on a specified index.</span></span> <span data-ttu-id="f01bf-107">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f01bf-107">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="f01bf-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f01bf-108">Syntax</span></span>


```VB
Qualifiers.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="f01bf-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f01bf-109">Property value</span></span>

<span data-ttu-id="f01bf-110">Objeto [**calificador**](qualifier.md) que representa el calificador indizado de la colección.</span><span class="sxs-lookup"><span data-stu-id="f01bf-110">A [**Qualifier**](qualifier.md) object that represents the indexed qualifier of the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="f01bf-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f01bf-111">Requirements</span></span>



| <span data-ttu-id="f01bf-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="f01bf-112">Requirement</span></span> | <span data-ttu-id="f01bf-113">Value</span><span class="sxs-lookup"><span data-stu-id="f01bf-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f01bf-114">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="f01bf-114">Redistributable</span></span><br/> | <span data-ttu-id="f01bf-115">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="f01bf-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f01bf-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f01bf-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="f01bf-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f01bf-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f01bf-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="f01bf-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f01bf-119">**Calificadores**</span><span class="sxs-lookup"><span data-stu-id="f01bf-119">**Qualifiers**</span></span>](qualifiers.md)
</dt> </dl>

 

 
