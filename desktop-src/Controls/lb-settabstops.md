---
title: Mensaje de LB_SETTABSTOPS (Winuser. h)
description: Establece las posiciones de tabulación en un cuadro de lista.
ms.assetid: b96b974e-b1e6-4361-98bb-4dc21c752690
keywords:
- LB_SETTABSTOPS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_SETTABSTOPS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f21927aaf82624242e8d42ef4a7459f1e36cdf74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905510"
---
# <a name="lb_settabstops-message"></a><span data-ttu-id="11413-104">\_Mensaje lb SETTABSTOPS</span><span class="sxs-lookup"><span data-stu-id="11413-104">LB\_SETTABSTOPS message</span></span>

<span data-ttu-id="11413-105">Establece las posiciones de tabulación en un cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="11413-105">Sets the tab-stop positions in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="11413-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="11413-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11413-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="11413-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="11413-108">Especifica el número de tabulaciones.</span><span class="sxs-lookup"><span data-stu-id="11413-108">Specifies the number of tab stops.</span></span>

</dd> <dt>

<span data-ttu-id="11413-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="11413-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="11413-110">Puntero al primer miembro de una matriz de enteros que contiene las tabulaciones.</span><span class="sxs-lookup"><span data-stu-id="11413-110">Pointer to the first member of an array of integers containing the tab stops.</span></span> <span data-ttu-id="11413-111">Los enteros representan el número de cuartos del ancho promedio de caracteres de la fuente seleccionada en el cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="11413-111">The integers represent the number of quarters of the average character width for the font that is selected into the list box.</span></span> <span data-ttu-id="11413-112">Por ejemplo, una tabulación de 4 se coloca en unidades de 1,0 caracteres y una posición de tabulación de 6 se coloca en las unidades de caracteres de promedio de 1,5.</span><span class="sxs-lookup"><span data-stu-id="11413-112">For example, a tab stop of 4 is placed at 1.0 character units, and a tab stop of 6 is placed at 1.5 average character units.</span></span> <span data-ttu-id="11413-113">Sin embargo, si el cuadro de lista forma parte de un cuadro de diálogo, los enteros se encuentran en unidades de plantilla de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="11413-113">However, if the list box is part of a dialog box, the integers are in dialog template units.</span></span> <span data-ttu-id="11413-114">Las tabulaciones se deben ordenar en orden ascendente; no se permiten pestañas hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="11413-114">The tab stops must be sorted in ascending order; backward tabs are not allowed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11413-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="11413-115">Return value</span></span>

<span data-ttu-id="11413-116">Si se establecen todas las pestañas especificadas, el valor devuelto es **true**; de lo contrario, es **false**.</span><span class="sxs-lookup"><span data-stu-id="11413-116">If all the specified tabs are set, the return value is **TRUE**; otherwise, it is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="11413-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="11413-117">Remarks</span></span>

<span data-ttu-id="11413-118">Para responder al mensaje de **lb \_ SETTABSTOPS** , el cuadro de lista se debe haber creado con el estilo [**lbs \_ USETABSTOPS**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="11413-118">To respond to the **LB\_SETTABSTOPS** message, the list box must have been created with the [**LBS\_USETABSTOPS**](list-box-styles.md) style.</span></span>

<span data-ttu-id="11413-119">Si *wParam* es 0 y *lParam* es **null**, la tabulación predeterminada es dos unidades de plantilla de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="11413-119">If *wParam* is 0 and *lParam* is **NULL**, the default tab stop is two dialog template units.</span></span> <span data-ttu-id="11413-120">Si *wParam* es 1, el cuadro de lista tendrá posiciones de tabulación separadas por la distancia especificada por *lParam*.</span><span class="sxs-lookup"><span data-stu-id="11413-120">If *wParam* is 1, the list box will have tab stops separated by the distance specified by *lParam*.</span></span>

<span data-ttu-id="11413-121">Si *lParam* apunta a más de un valor, se establecerá una detención de tabulación para cada valor de *lParam*, hasta el número especificado por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="11413-121">If *lParam* points to more than a single value, a tab stop will be set for each value in *lParam*, up to the number specified by *wParam*.</span></span>

<span data-ttu-id="11413-122">Los valores especificados por *lParam* están en unidades de plantilla de cuadro de diálogo, que son las unidades independientes del dispositivo que se usan en las plantillas de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="11413-122">The values specified by *lParam* are in dialog template units, which are the device-independent units used in dialog box templates.</span></span> <span data-ttu-id="11413-123">Para convertir las medidas de las unidades de plantilla de cuadro de diálogo en unidades de pantalla (píxeles), use la función [**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) .</span><span class="sxs-lookup"><span data-stu-id="11413-123">To convert measurements from dialog template units to screen units (pixels), use the [**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) function.</span></span>

<span data-ttu-id="11413-124">Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el búfer señalado por *lParam* debe residir en la memoria de escritura, aunque el mensaje no modifique la matriz.</span><span class="sxs-lookup"><span data-stu-id="11413-124">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The buffer pointed to by *lParam* must reside in writable memory, even though the message does not modify the array.</span></span>

## <a name="requirements"></a><span data-ttu-id="11413-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11413-125">Requirements</span></span>



| <span data-ttu-id="11413-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="11413-126">Requirement</span></span> | <span data-ttu-id="11413-127">Value</span><span class="sxs-lookup"><span data-stu-id="11413-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11413-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11413-128">Minimum supported client</span></span><br/> | <span data-ttu-id="11413-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="11413-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="11413-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11413-130">Minimum supported server</span></span><br/> | <span data-ttu-id="11413-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="11413-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="11413-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="11413-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="11413-133"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="11413-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11413-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="11413-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11413-135">**MapDialogRect**</span><span class="sxs-lookup"><span data-stu-id="11413-135">**MapDialogRect**</span></span>](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)
</dt> </dl>

 

