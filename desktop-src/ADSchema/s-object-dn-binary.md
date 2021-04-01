---
title: Sintaxis de Object (DN-Binary)
description: Cadena de octetos que contiene un valor binario y un nombre distintivo (DN).
ms.assetid: 1d7efc17-a99a-41bf-9812-9e8a2b2b6644
ms.tgt_platform: multiple
keywords:
- Esquema de AD de sintaxis de objeto (DN-binario)
topic_type:
- apiref
api_name:
- Object(DN-Binary)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e96f640ad729f203362df906bcc6afe6b82e7e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151293"
---
# <a name="objectdn-binary-syntax"></a><span data-ttu-id="05b5a-104">Sintaxis de Object (DN-Binary)</span><span class="sxs-lookup"><span data-stu-id="05b5a-104">Object(DN-Binary) syntax</span></span>

<span data-ttu-id="05b5a-105">Cadena de octetos que contiene un valor binario y un nombre distintivo (DN).</span><span class="sxs-lookup"><span data-stu-id="05b5a-105">An octet string that contains a binary value and a distinguished name (DN).</span></span>



| <span data-ttu-id="05b5a-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="05b5a-106">Entry</span></span> | <span data-ttu-id="05b5a-107">Value</span><span class="sxs-lookup"><span data-stu-id="05b5a-107">Value</span></span> |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="05b5a-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="05b5a-108">Name</span></span>         | <span data-ttu-id="05b5a-109">Object(DN-Binary)</span><span class="sxs-lookup"><span data-stu-id="05b5a-109">Object(DN-Binary)</span></span>                                                                  |
| <span data-ttu-id="05b5a-110">IDENTIFICADOR de sintaxis</span><span class="sxs-lookup"><span data-stu-id="05b5a-110">Syntax ID</span></span>    | <span data-ttu-id="05b5a-111">2.5.5.7</span><span class="sxs-lookup"><span data-stu-id="05b5a-111">2.5.5.7</span></span>                                                                            |
| <span data-ttu-id="05b5a-112">IDENTIFICADOR DE OM</span><span class="sxs-lookup"><span data-stu-id="05b5a-112">OM ID</span></span>        | <span data-ttu-id="05b5a-113">127</span><span class="sxs-lookup"><span data-stu-id="05b5a-113">127</span></span>                                                                                |
| <span data-ttu-id="05b5a-114">Tipo MAPI</span><span class="sxs-lookup"><span data-stu-id="05b5a-114">MAPI Type</span></span>    | <span data-ttu-id="05b5a-115">TSTRING</span><span class="sxs-lookup"><span data-stu-id="05b5a-115">TSTRING</span></span>                                                                            |
| <span data-ttu-id="05b5a-116">Tipo ADS</span><span class="sxs-lookup"><span data-stu-id="05b5a-116">ADS Type</span></span>     | <span data-ttu-id="05b5a-117">\_DN ADSTYPE \_ con \_ binario</span><span class="sxs-lookup"><span data-stu-id="05b5a-117">ADSTYPE\_DN\_WITH\_BINARY</span></span>                                                          |
| <span data-ttu-id="05b5a-118">Tipo Variant</span><span class="sxs-lookup"><span data-stu-id="05b5a-118">Variant Type</span></span> | <span data-ttu-id="05b5a-119">distribución de VT \_</span><span class="sxs-lookup"><span data-stu-id="05b5a-119">VT\_DISPATCH</span></span>                                                                       |
| <span data-ttu-id="05b5a-120">Tipo de SDS</span><span class="sxs-lookup"><span data-stu-id="05b5a-120">SDS Type</span></span>     | <span data-ttu-id="05b5a-121">Objeto COM que se puede convertir en un [**IADsDNWithBinary**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary).</span><span class="sxs-lookup"><span data-stu-id="05b5a-121">A COM object that can be cast to an [**IADsDNWithBinary**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary).</span></span> |



## <a name="remarks"></a><span data-ttu-id="05b5a-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="05b5a-122">Remarks</span></span>

<span data-ttu-id="05b5a-123">Un valor con esta sintaxis tiene el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="05b5a-123">A value with this syntax has the following format:</span></span>

``` syntax
B:<char count>:<binary value>:<object DN>
```

<span data-ttu-id="05b5a-124">donde " &lt; número &gt; de caracteres" es el número de dígitos hexadecimales en " &lt; valor binario" &gt; , " &lt; valor binario &gt; " es la representación hexadecimal del valor binario y " &lt; DN del objeto &gt; " es un nombre distintivo.</span><span class="sxs-lookup"><span data-stu-id="05b5a-124">where "&lt;char count&gt;" is the number of hexadecimal digits in "&lt;binary value&gt;", "&lt;binary value&gt;" is the hexadecimal representation of the binary value, and "&lt;object DN&gt;" is a distinguished name.</span></span> <span data-ttu-id="05b5a-125">Active Directory actualiza automáticamente el DN si el objeto al que hace referencia se mueve o se cambia de nombre.</span><span class="sxs-lookup"><span data-stu-id="05b5a-125">Active Directory automatically updates the DN if the object that it refers to is moved or renamed.</span></span> <span data-ttu-id="05b5a-126">Para obtener más información y un ejemplo de código que use esta sintaxis, vea [Habilitar el enlace de renombre seguro con la propiedad otherWellKnownObjects](/windows/desktop/AD/enabling-rename-safe-binding-with-the-otherwellknownobjects-property).</span><span class="sxs-lookup"><span data-stu-id="05b5a-126">For more information and a code example that uses this syntax, see [Enabling Rename-safe Binding with the otherWellKnownObjects Property](/windows/desktop/AD/enabling-rename-safe-binding-with-the-otherwellknownobjects-property).</span></span>

## <a name="see-also"></a><span data-ttu-id="05b5a-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="05b5a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05b5a-128">**IADsDNWithBinary**</span><span class="sxs-lookup"><span data-stu-id="05b5a-128">**IADsDNWithBinary**</span></span>](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary)
</dt> </dl>

 

 
