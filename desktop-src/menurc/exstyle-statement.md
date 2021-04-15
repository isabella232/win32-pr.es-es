---
title: ExStyle (instrucción)
description: Define los estilos extendidos de ventana para un cuadro de diálogo. En una definición de recursos, la instrucción de ExStyle se coloca con las instrucciones opcionales antes del principio del cuerpo de la definición de recursos.
ms.assetid: 5dc74bab-e385-457c-80c4-5e04eed589b5
keywords:
- Menús de instrucciones de exestilo y otros recursos
topic_type:
- apiref
api_name:
- EXSTYLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 277727757daeaafe5ad11cfd2e4f5fb6ee726458
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487619"
---
# <a name="exstyle-statement"></a><span data-ttu-id="b7cb4-105">ExStyle (instrucción)</span><span class="sxs-lookup"><span data-stu-id="b7cb4-105">EXSTYLE statement</span></span>

<span data-ttu-id="b7cb4-106">Define los estilos extendidos de ventana para un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b7cb4-106">Defines extended window styles for a dialog box.</span></span> <span data-ttu-id="b7cb4-107">En una definición de recursos, la instrucción de **ExStyle** se coloca con las instrucciones opcionales antes del principio del cuerpo de la definición de recursos.</span><span class="sxs-lookup"><span data-stu-id="b7cb4-107">In a resource definition, the **EXSTYLE** statement is placed with the optional statements before the beginning of the body of the resource definition.</span></span>

``` syntax
EXSTYLE extended-style
```

<dl> <dt>

<span data-ttu-id="b7cb4-108"><span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*estilo extendido*</span><span class="sxs-lookup"><span data-stu-id="b7cb4-108"><span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*extended-style*</span></span>
</dt> <dd>

<span data-ttu-id="b7cb4-109">Estilo de ventana extendido para el cuadro de diálogo o el control.</span><span class="sxs-lookup"><span data-stu-id="b7cb4-109">Extended window style for the dialog box or control.</span></span> <span data-ttu-id="b7cb4-110">Para obtener una lista de estilos de ventana extendidos, vea [**estilos extendidos de ventana**](/windows/desktop/winmsg/extended-window-styles).</span><span class="sxs-lookup"><span data-stu-id="b7cb4-110">For a list of extended window styles, see [**Extended Window Styles**](/windows/desktop/winmsg/extended-window-styles).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b7cb4-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b7cb4-111">Remarks</span></span>

<span data-ttu-id="b7cb4-112">En el caso de los controles, los estilos extendidos se especifican después de la opción *Style* en la instrucción control Resource-Definition.</span><span class="sxs-lookup"><span data-stu-id="b7cb4-112">For controls, extended styles are specified after the *style* option in the control resource-definition statement.</span></span> <span data-ttu-id="b7cb4-113">Para obtener más información, vea la instrucción de definición de recursos para el control individual.</span><span class="sxs-lookup"><span data-stu-id="b7cb4-113">For more information, see the resource-definition statement for the individual control.</span></span>

## <a name="see-also"></a><span data-ttu-id="b7cb4-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="b7cb4-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7cb4-115">**ACELERADORES**</span><span class="sxs-lookup"><span data-stu-id="b7cb4-115">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="b7cb4-116">**CONTROL**</span><span class="sxs-lookup"><span data-stu-id="b7cb4-116">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="b7cb4-117">**DIÁLOGO**</span><span class="sxs-lookup"><span data-stu-id="b7cb4-117">**DIALOG**</span></span>](dialog-resource.md)
</dt> <dt>

[<span data-ttu-id="b7cb4-118">**MENU**</span><span class="sxs-lookup"><span data-stu-id="b7cb4-118">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="b7cb4-119">**EMERGENTE**</span><span class="sxs-lookup"><span data-stu-id="b7cb4-119">**POPUP**</span></span>](popup-resource.md)
</dt> <dt>

[<span data-ttu-id="b7cb4-120">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="b7cb4-120">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="b7cb4-121">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="b7cb4-121">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="b7cb4-122">Recurso definido por el usuario</span><span class="sxs-lookup"><span data-stu-id="b7cb4-122">User-Defined Resource</span></span>](user-defined-resource.md)
</dt> </dl>

 

 