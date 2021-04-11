---
title: Valores de WTNCA (uxtheme. h)
description: Especifica las marcas que modifican los atributos de estilo visual de ventana. Use uno o una combinación bit a bit de los valores siguientes.
ms.assetid: C71D1957-6572-4242-B715-C54BDFBBD6B7
topic_type:
- apiref
api_name:
- WTNCA_NODRAWCAPTION
- WTNCA_NODRAWICON
- WTNCA_NOSYSMENU
- WTNCA_NOMIRRORHELP
- WTNCA_VALIDBITS
api_location:
- Uxtheme.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebaf543b688d0b403962da43029ac9aa85422bc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151039"
---
# <a name="wtnca-values"></a><span data-ttu-id="3ce12-104">Valores de WTNCA</span><span class="sxs-lookup"><span data-stu-id="3ce12-104">WTNCA Values</span></span>

<span data-ttu-id="3ce12-105">Especifica las marcas que modifican los atributos de estilo visual de ventana.</span><span class="sxs-lookup"><span data-stu-id="3ce12-105">Specifies flags that modify window visual style attributes.</span></span> <span data-ttu-id="3ce12-106">Use uno o una combinación bit a bit de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="3ce12-106">Use one, or a bitwise combination of the following values.</span></span>



| <span data-ttu-id="3ce12-107">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="3ce12-107">Constant/value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="3ce12-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ce12-108">Description</span></span>                                                                             |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| <span id="WTNCA_NODRAWCAPTION"></span><span id="wtnca_nodrawcaption"></span><dl> <span data-ttu-id="3ce12-109"><dt>**WTNCA \_ NODRAWCAPTION**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="3ce12-109"><dt>**WTNCA\_NODRAWCAPTION**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="3ce12-110">Impide que se dibuje el título de la ventana.</span><span class="sxs-lookup"><span data-stu-id="3ce12-110">Prevents the window caption from being drawn.</span></span><br/>                                |
| <span id="WTNCA_NODRAWICON"></span><span id="wtnca_nodrawicon"></span><dl> <span data-ttu-id="3ce12-111"><dt>**WTNCA \_ NODRAWICON**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="3ce12-111"><dt>**WTNCA\_NODRAWICON**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="3ce12-112">Impide que se dibuje el icono del sistema.</span><span class="sxs-lookup"><span data-stu-id="3ce12-112">Prevents the system icon from being drawn.</span></span><br/>                                   |
| <span id="WTNCA_NOSYSMENU"></span><span id="wtnca_nosysmenu"></span><dl> <span data-ttu-id="3ce12-113"><dt>**WTNCA \_ NOSYSMENU**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="3ce12-113"><dt>**WTNCA\_NOSYSMENU**</dt> <dt>0x00000004</dt></span></span> </dl>             | <span data-ttu-id="3ce12-114">Impide que aparezca el menú de iconos del sistema.</span><span class="sxs-lookup"><span data-stu-id="3ce12-114">Prevents the system icon menu from appearing.</span></span><br/>                                |
| <span id="WTNCA_NOMIRRORHELP"></span><span id="wtnca_nomirrorhelp"></span><dl> <span data-ttu-id="3ce12-115"><dt>**WTNCA \_ NOMIRRORHELP**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="3ce12-115"><dt>**WTNCA\_NOMIRRORHELP**</dt> <dt>0x00000008</dt></span></span> </dl>    | <span data-ttu-id="3ce12-116">Impide la creación de reflejo del signo de interrogación, incluso en el diseño de derecha a izquierda (RTL).</span><span class="sxs-lookup"><span data-stu-id="3ce12-116">Prevents mirroring of the question mark, even in right-to-left (RTL) layout.</span></span><br/> |
| <span id="WTNCA_VALIDBITS"></span><span id="wtnca_validbits"></span><dl> <span data-ttu-id="3ce12-117"><dt>**WTNCA \_ VALIDBITS**</dt></span><span class="sxs-lookup"><span data-stu-id="3ce12-117"><dt>**WTNCA\_VALIDBITS**</dt></span></span> </dl>                                                                             | <span data-ttu-id="3ce12-118">Máscara que contiene todos los bits válidos.</span><span class="sxs-lookup"><span data-stu-id="3ce12-118">A mask that contains all the valid bits.</span></span><br/>                                     |



## <a name="requirements"></a><span data-ttu-id="3ce12-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ce12-119">Requirements</span></span>



| <span data-ttu-id="3ce12-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ce12-120">Requirement</span></span> | <span data-ttu-id="3ce12-121">Value</span><span class="sxs-lookup"><span data-stu-id="3ce12-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3ce12-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ce12-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3ce12-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3ce12-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3ce12-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ce12-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3ce12-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3ce12-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3ce12-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3ce12-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ce12-127"><dt>Uxtheme. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ce12-127"><dt>Uxtheme.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ce12-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ce12-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="3ce12-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="3ce12-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3ce12-130">**Opciones de WTA \_**</span><span class="sxs-lookup"><span data-stu-id="3ce12-130">**WTA\_OPTIONS**</span></span>](/windows/desktop/api/Uxtheme/ns-uxtheme-wta_options)
</dt> <dt>

[<span data-ttu-id="3ce12-131">**SetWindowThemeNonClientAttributes**</span><span class="sxs-lookup"><span data-stu-id="3ce12-131">**SetWindowThemeNonClientAttributes**</span></span>](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowthemenonclientattributes)
</dt> </dl>

 

 





