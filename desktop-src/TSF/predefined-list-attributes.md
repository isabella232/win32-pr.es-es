---
title: Atributos de lista predefinidos (TsAttrid. h)
description: Los valores siguientes identifican los atributos de lista obtenidos con el método ITfContext GetAppProperty. Se incluyen el formato de datos y el contenido de cada tipo de propiedad.
ms.assetid: 9a9e1912-51c0-40e0-9e3a-b84ea7077dbe
keywords:
- Atributos de lista predefinidos marco de trabajo de servicios de texto
topic_type:
- apiref
api_name:
- Predefined List Attributes
api_location:
- TsAttrid.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81ade2403e124b934c6872f39c01fc7fc1ea6f6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150854"
---
# <a name="predefined-list-attributes"></a><span data-ttu-id="bc099-105">Atributos de lista predefinidos</span><span class="sxs-lookup"><span data-stu-id="bc099-105">Predefined List Attributes</span></span>

<span data-ttu-id="bc099-106">Los valores siguientes identifican los atributos de lista obtenidos con el método [ITfContext:: GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) .</span><span class="sxs-lookup"><span data-stu-id="bc099-106">The following values identify list attributes obtained with the [ITfContext::GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) method.</span></span> <span data-ttu-id="bc099-107">Se incluyen el formato de datos y el contenido de cada tipo de propiedad.</span><span class="sxs-lookup"><span data-stu-id="bc099-107">The data format and contents of each property type are included.</span></span>

## <a name="properties"></a><span data-ttu-id="bc099-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bc099-108">Properties</span></span>



| <span data-ttu-id="bc099-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bc099-109">Property</span></span>                          | <span data-ttu-id="bc099-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="bc099-110">Description</span></span>                                                                                     |
|-----------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc099-111">Lista de TSATTRID \_</span><span class="sxs-lookup"><span data-stu-id="bc099-111">TSATTRID\_List</span></span>                    | <span data-ttu-id="bc099-112">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="bc099-112">Not used.</span></span>                                                                                       |
| <span data-ttu-id="bc099-113">TSATTRID \_ lista \_ LevelIndel</span><span class="sxs-lookup"><span data-stu-id="bc099-113">TSATTRID\_List\_LevelIndel</span></span>        | <span data-ttu-id="bc099-114">Contiene el nivel de índice de la lista.</span><span class="sxs-lookup"><span data-stu-id="bc099-114">Contains the index level of the list.</span></span> <span data-ttu-id="bc099-115">1 es el nivel más externo, 2 es el nivel siguiente, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="bc099-115">1 is the outermost level, 2 is the next level, and so on.</span></span> |
| <span data-ttu-id="bc099-116">\_Tipo de lista TSATTRID \_</span><span class="sxs-lookup"><span data-stu-id="bc099-116">TSATTRID\_List\_Type</span></span>              | <span data-ttu-id="bc099-117">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="bc099-117">Not used.</span></span>                                                                                       |
| <span data-ttu-id="bc099-118">\_Tipo de lista TSATTRID \_ \_ Árabe</span><span class="sxs-lookup"><span data-stu-id="bc099-118">TSATTRID\_List\_Type\_Arabic</span></span>      | <span data-ttu-id="bc099-119">Contiene un valor distinto de cero si la lista es una lista de números arábigos o cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="bc099-119">Contains a nonzero value if the list is an arabic numeral list or zero otherwise.</span></span>               |
| <span data-ttu-id="bc099-120">\_Viñeta de \_ tipo de lista de TSATTRID \_</span><span class="sxs-lookup"><span data-stu-id="bc099-120">TSATTRID\_List\_Type\_Bullet</span></span>      | <span data-ttu-id="bc099-121">Contiene un valor distinto de cero si la lista es una lista con viñetas o cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="bc099-121">Contains a nonzero value if the list is a bulleted list or zero otherwise.</span></span>                      |
| <span data-ttu-id="bc099-122">\_Tipo de lista TSATTRID \_ \_ LowerLetter</span><span class="sxs-lookup"><span data-stu-id="bc099-122">TSATTRID\_List\_Type\_LowerLetter</span></span> | <span data-ttu-id="bc099-123">Contiene un valor distinto de cero si la lista es una lista con letras minúsculas o cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="bc099-123">Contains a nonzero value if the list is a lowercase lettered list or zero otherwise.</span></span>            |
| <span data-ttu-id="bc099-124">\_Tipo de lista TSATTRID \_ \_ LowerRoman</span><span class="sxs-lookup"><span data-stu-id="bc099-124">TSATTRID\_List\_Type\_LowerRoman</span></span>  | <span data-ttu-id="bc099-125">Contiene un valor distinto de cero si la lista es una lista de números romanos en minúsculas o cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="bc099-125">Contains a nonzero value if the list is a lowercase roman numeral list or zero otherwise.</span></span>       |
| <span data-ttu-id="bc099-126">\_Tipo de lista TSATTRID \_ \_ UpperLetter</span><span class="sxs-lookup"><span data-stu-id="bc099-126">TSATTRID\_List\_Type\_UpperLetter</span></span> | <span data-ttu-id="bc099-127">Contiene un valor distinto de cero si la lista es una lista con letras mayúsculas o cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="bc099-127">Contains a nonzero value if the list is an upper-case lettered list or zero otherwise.</span></span>          |
| <span data-ttu-id="bc099-128">Tipo de lista TSATTRID de \_ \_ \_ perro</span><span class="sxs-lookup"><span data-stu-id="bc099-128">TSATTRID\_List\_Type\_UpperRoman</span></span>  | <span data-ttu-id="bc099-129">Contiene un valor distinto de cero si la lista es una lista de números romanos en mayúsculas o cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="bc099-129">Contains a nonzero value if the list is an uppercase roman numeral list or zero otherwise.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="bc099-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc099-130">Requirements</span></span>



| <span data-ttu-id="bc099-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc099-131">Requirement</span></span> | <span data-ttu-id="bc099-132">Value</span><span class="sxs-lookup"><span data-stu-id="bc099-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bc099-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc099-133">Minimum supported client</span></span><br/> | <span data-ttu-id="bc099-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bc099-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="bc099-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc099-135">Minimum supported server</span></span><br/> | <span data-ttu-id="bc099-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bc099-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bc099-137">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="bc099-137">Redistributable</span></span><br/>          | <span data-ttu-id="bc099-138">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bc099-138">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="bc099-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc099-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc099-140"><dt>TsAttrid. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc099-140"><dt>TsAttrid.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc099-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc099-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc099-142">ITfContext::GetAppProperty</span><span class="sxs-lookup"><span data-stu-id="bc099-142">ITfContext::GetAppProperty</span></span>](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty)
</dt> </dl>

 

