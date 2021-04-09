---
description: La propiedad Value del objeto SWbemNamedValue devuelve el valor Variant de un elemento SWbemNamedValue.
ms.assetid: f9609bd2-893a-48c3-9faa-93cd033c4109
ms.tgt_platform: multiple
title: Propiedad SWbemNamedValue. Value (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValue.Value
- ISWbemNamedValue.Value
- ISWbemNamedValue.get_Value
- ISWbemNamedValue.put_Value
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4bf63b15a27c1149341200f29e938bdba6cd7bae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155833"
---
# <a name="swbemnamedvaluevalue-property"></a><span data-ttu-id="79685-103">SWbemNamedValue. Value (propiedad)</span><span class="sxs-lookup"><span data-stu-id="79685-103">SWbemNamedValue.Value property</span></span>

<span data-ttu-id="79685-104">La propiedad **Value** del objeto [**SWbemNamedValue**](swbemnamedvalue.md) devuelve el valor Variant de un elemento **SWbemNamedValue** .</span><span class="sxs-lookup"><span data-stu-id="79685-104">The **Value** property of the [**SWbemNamedValue**](swbemnamedvalue.md) object returns the variant value of an **SWbemNamedValue** item.</span></span> <span data-ttu-id="79685-105">Esta es la propiedad predeterminada de los objetos **SWbemNamedValue** .</span><span class="sxs-lookup"><span data-stu-id="79685-105">This is the default property for **SWbemNamedValue** objects.</span></span> <span data-ttu-id="79685-106">Los cambios realizados en la propiedad Value se reflejan automáticamente en la colección [**SWbemNamedValueSet**](swbemnamedvalueset.md) a la que pertenece el objeto **SWbemNamedValue** .</span><span class="sxs-lookup"><span data-stu-id="79685-106">Changes made to the value property are reflected automatically in the [**SWbemNamedValueSet**](swbemnamedvalueset.md) collection to which the **SWbemNamedValue** object belongs.</span></span>

<span data-ttu-id="79685-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="79685-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="79685-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="79685-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="79685-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79685-109">Syntax</span></span>


```VB
SWbemNamedValue.Value As Variant
```



## <a name="property-value"></a><span data-ttu-id="79685-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="79685-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="79685-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79685-111">Requirements</span></span>



| <span data-ttu-id="79685-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="79685-112">Requirement</span></span> | <span data-ttu-id="79685-113">Value</span><span class="sxs-lookup"><span data-stu-id="79685-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="79685-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79685-114">Minimum supported client</span></span><br/> | <span data-ttu-id="79685-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="79685-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="79685-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79685-116">Minimum supported server</span></span><br/> | <span data-ttu-id="79685-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="79685-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="79685-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79685-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="79685-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="79685-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="79685-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="79685-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="79685-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="79685-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="79685-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="79685-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79685-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79685-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="79685-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="79685-124">CLSID</span></span><br/>                    | <span data-ttu-id="79685-125">CLSID \_ SWbemNamedValue</span><span class="sxs-lookup"><span data-stu-id="79685-125">CLSID\_SWbemNamedValue</span></span><br/>                                                       |
| <span data-ttu-id="79685-126">IID</span><span class="sxs-lookup"><span data-stu-id="79685-126">IID</span></span><br/>                      | <span data-ttu-id="79685-127">\_ISWBEMNAMEDVALUE IID</span><span class="sxs-lookup"><span data-stu-id="79685-127">IID\_ISWbemNamedValue</span></span><br/>                                                        |



 

 




