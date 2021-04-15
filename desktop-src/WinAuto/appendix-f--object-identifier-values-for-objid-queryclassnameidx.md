---
title: Apéndice F valores de identificador de objeto para OBJID_QUERYCLASSNAMEIDX
description: Cuando OLEACC envía un mensaje de WM \_ GETOBJECT con el parámetro lParam establecido en OBJIDQUERYCLASSNAMEIDX, muchos controles comunes o de usuario estándar (COMCTL) devuelven uno de los valores siguientes.
ms.assetid: 2a54973c-7dfa-49af-8fd0-925fafa256ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faffd8382820aef2cd341ce54b23c9e9e7c9a59b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695706"
---
# <a name="appendix-f-object-identifier-values-for-objid_queryclassnameidx"></a><span data-ttu-id="f426e-103">Apéndice F: valores de identificador de objeto para OBJID \_ QUERYCLASSNAMEIDX</span><span class="sxs-lookup"><span data-stu-id="f426e-103">Appendix F: Object Identifier Values for OBJID\_QUERYCLASSNAMEIDX</span></span>

<span data-ttu-id="f426e-104">Cuando OLEACC envía un mensaje de [**WM \_ GETOBJECT**](wm-getobject.md) con el parámetro *lParam* establecido en OBJIDQUERYCLASSNAMEIDX, muchos controles comunes o de usuario estándar (COMCTL) devuelven uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="f426e-104">When OLEACC sends a [**WM\_GETOBJECT**](wm-getobject.md) message with the *lParam* parameter set to OBJIDQUERYCLASSNAMEIDX, many standard USER or common controls (COMCTL) return one of the following values.</span></span>



| <span data-ttu-id="f426e-105">Control de usuario o común</span><span class="sxs-lookup"><span data-stu-id="f426e-105">USER or common control</span></span> | <span data-ttu-id="f426e-106">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f426e-106">Return value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="f426e-107">Listbox</span><span class="sxs-lookup"><span data-stu-id="f426e-107">Listbox</span></span>                | <span data-ttu-id="f426e-108">65536 + 0</span><span class="sxs-lookup"><span data-stu-id="f426e-108">65536+0</span></span>      |
| <span data-ttu-id="f426e-109">Botón</span><span class="sxs-lookup"><span data-stu-id="f426e-109">Button</span></span>                 | <span data-ttu-id="f426e-110">65536 + 2</span><span class="sxs-lookup"><span data-stu-id="f426e-110">65536+2</span></span>      |
| <span data-ttu-id="f426e-111">estática</span><span class="sxs-lookup"><span data-stu-id="f426e-111">Static</span></span>                 | <span data-ttu-id="f426e-112">65536 + 3</span><span class="sxs-lookup"><span data-stu-id="f426e-112">65536+3</span></span>      |
| <span data-ttu-id="f426e-113">Editar</span><span class="sxs-lookup"><span data-stu-id="f426e-113">Edit</span></span>                   | <span data-ttu-id="f426e-114">65536 + 4</span><span class="sxs-lookup"><span data-stu-id="f426e-114">65536+4</span></span>      |
| <span data-ttu-id="f426e-115">ComboBox</span><span class="sxs-lookup"><span data-stu-id="f426e-115">Combobox</span></span>               | <span data-ttu-id="f426e-116">65536 + 5</span><span class="sxs-lookup"><span data-stu-id="f426e-116">65536+5</span></span>      |
| <span data-ttu-id="f426e-117">Barra de desplazamiento</span><span class="sxs-lookup"><span data-stu-id="f426e-117">Scrollbar</span></span>              | <span data-ttu-id="f426e-118">65536 + 10</span><span class="sxs-lookup"><span data-stu-id="f426e-118">65536+10</span></span>     |
| <span data-ttu-id="f426e-119">Status</span><span class="sxs-lookup"><span data-stu-id="f426e-119">Status</span></span>                 | <span data-ttu-id="f426e-120">65536 + 11</span><span class="sxs-lookup"><span data-stu-id="f426e-120">65536+11</span></span>     |
| <span data-ttu-id="f426e-121">Barra de herramientas</span><span class="sxs-lookup"><span data-stu-id="f426e-121">Toolbar</span></span>                | <span data-ttu-id="f426e-122">65536 + 12</span><span class="sxs-lookup"><span data-stu-id="f426e-122">65536+12</span></span>     |
| <span data-ttu-id="f426e-123">Progreso</span><span class="sxs-lookup"><span data-stu-id="f426e-123">Progress</span></span>               | <span data-ttu-id="f426e-124">65536 + 13</span><span class="sxs-lookup"><span data-stu-id="f426e-124">65536+13</span></span>     |
| <span data-ttu-id="f426e-125">Dicha</span><span class="sxs-lookup"><span data-stu-id="f426e-125">Animate</span></span>                | <span data-ttu-id="f426e-126">65536 + 14</span><span class="sxs-lookup"><span data-stu-id="f426e-126">65536+14</span></span>     |
| <span data-ttu-id="f426e-127">Pestaña</span><span class="sxs-lookup"><span data-stu-id="f426e-127">Tab</span></span>                    | <span data-ttu-id="f426e-128">65536 + 15</span><span class="sxs-lookup"><span data-stu-id="f426e-128">65536+15</span></span>     |
| <span data-ttu-id="f426e-129">Tecla de acceso rápido</span><span class="sxs-lookup"><span data-stu-id="f426e-129">Hotkey</span></span>                 | <span data-ttu-id="f426e-130">65536 + 16</span><span class="sxs-lookup"><span data-stu-id="f426e-130">65536+16</span></span>     |
| <span data-ttu-id="f426e-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f426e-131">Header</span></span>                 | <span data-ttu-id="f426e-132">65536 + 17</span><span class="sxs-lookup"><span data-stu-id="f426e-132">65536+17</span></span>     |
| <span data-ttu-id="f426e-133">TrackBar</span><span class="sxs-lookup"><span data-stu-id="f426e-133">Trackbar</span></span>               | <span data-ttu-id="f426e-134">65536 + 18</span><span class="sxs-lookup"><span data-stu-id="f426e-134">65536+18</span></span>     |
| <span data-ttu-id="f426e-135">ListView</span><span class="sxs-lookup"><span data-stu-id="f426e-135">Listview</span></span>               | <span data-ttu-id="f426e-136">65536 + 19</span><span class="sxs-lookup"><span data-stu-id="f426e-136">65536+19</span></span>     |
| <span data-ttu-id="f426e-137">Cuadro numérico</span><span class="sxs-lookup"><span data-stu-id="f426e-137">Updown</span></span>                 | <span data-ttu-id="f426e-138">65536 + 22</span><span class="sxs-lookup"><span data-stu-id="f426e-138">65536+22</span></span>     |
| <span data-ttu-id="f426e-139">Información sobre herramientas</span><span class="sxs-lookup"><span data-stu-id="f426e-139">ToolTips</span></span>               | <span data-ttu-id="f426e-140">65536 + 24</span><span class="sxs-lookup"><span data-stu-id="f426e-140">65536+24</span></span>     |
| <span data-ttu-id="f426e-141">Vista</span><span class="sxs-lookup"><span data-stu-id="f426e-141">Treeview</span></span>               | <span data-ttu-id="f426e-142">65536 + 25</span><span class="sxs-lookup"><span data-stu-id="f426e-142">65536+25</span></span>     |
| <span data-ttu-id="f426e-143">RichEdit</span><span class="sxs-lookup"><span data-stu-id="f426e-143">RichEdit</span></span>               | <span data-ttu-id="f426e-144">65536 + 28</span><span class="sxs-lookup"><span data-stu-id="f426e-144">65536+28</span></span>     |



 

<span data-ttu-id="f426e-145">Solo los controles comunes de usuario y de Windows (COMCTL) devolverán uno de los valores de la tabla.</span><span class="sxs-lookup"><span data-stu-id="f426e-145">Only USER and Windows common controls (COMCTL) will return one of the values from the table.</span></span> <span data-ttu-id="f426e-146">Si una ventana devuelve 0 en respuesta a este mensaje, la ventana puede ser una de las siguientes:</span><span class="sxs-lookup"><span data-stu-id="f426e-146">If a window returns 0 in response to this message, the window may be one of the following:</span></span>

-   <span data-ttu-id="f426e-147">Un control personalizado</span><span class="sxs-lookup"><span data-stu-id="f426e-147">A custom control</span></span>
-   <span data-ttu-id="f426e-148">Control distinto de uno de los controles de la tabla anterior.</span><span class="sxs-lookup"><span data-stu-id="f426e-148">A control other than one of the controls in the previous table</span></span>
-   <span data-ttu-id="f426e-149">Una versión anterior de un control del sistema que no reconoce el mensaje de [**WM \_ GETOBJECT**](wm-getobject.md)</span><span class="sxs-lookup"><span data-stu-id="f426e-149">An old version of a system control that does not recognize the [**WM\_GETOBJECT**](wm-getobject.md) message</span></span>

<span data-ttu-id="f426e-150">Si una ventana devuelve 0, es posible que los clientes tengan que usar [**RealGetWindowClass**](/windows/win32/api/winuser/nf-winuser-realgetwindowclassw) o [**getClassName**](/windows/win32/api/winuser/nf-winuser-getclassname).</span><span class="sxs-lookup"><span data-stu-id="f426e-150">If a window returns 0, clients may need to use [**RealGetWindowClass**](/windows/win32/api/winuser/nf-winuser-realgetwindowclassw) or [**GetClassName**](/windows/win32/api/winuser/nf-winuser-getclassname).</span></span> <span data-ttu-id="f426e-151">Puede utilizar estas funciones para determinar el tipo de control basado en el nombre de clase.</span><span class="sxs-lookup"><span data-stu-id="f426e-151">You can use these functions to determine the type of control based on class name.</span></span>

<span data-ttu-id="f426e-152">En general, los clientes pueden usar la información proporcionada por OLEACC.</span><span class="sxs-lookup"><span data-stu-id="f426e-152">In general, clients can use the information provided by OLEACC.</span></span>

 

 