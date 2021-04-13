---
title: Cursor (referencia de elementos de interfaz de usuario de MSAA)
description: Un cursor es una pequeña imagen cuya ubicación en la pantalla está controlada por un dispositivo señalador, como un mouse, un lápiz o un trackball. Cuando el usuario mueve el dispositivo señalador, el sistema operativo Windows mueve el cursor.
ms.assetid: ff97d474-7c96-4f89-bc34-2cf320381ce0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff351040d342adccda8cb03d56d91f9dc429074f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356816"
---
# <a name="cursor-msaa-ui-element-reference"></a><span data-ttu-id="e2d0f-104">Cursor (referencia de elementos de interfaz de usuario de MSAA)</span><span class="sxs-lookup"><span data-stu-id="e2d0f-104">Cursor (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="e2d0f-105">En este tema se describen los cursores para la referencia de elementos de la interfaz de usuario de MSAA.</span><span class="sxs-lookup"><span data-stu-id="e2d0f-105">This topic describes cursors for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="e2d0f-106">El uso de cursores en varios marcos de interfaz de usuario no se describe aquí.</span><span class="sxs-lookup"><span data-stu-id="e2d0f-106">How to use cursors in various UI frameworks is not described here.</span></span> <span data-ttu-id="e2d0f-107">Consulte la documentación de referencia de la API del marco de interfaz de usuario que está usando.</span><span class="sxs-lookup"><span data-stu-id="e2d0f-107">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="e2d0f-108">Un cursor es una pequeña imagen cuya ubicación en la pantalla está controlada por un dispositivo señalador, como un mouse, un lápiz o un trackball.</span><span class="sxs-lookup"><span data-stu-id="e2d0f-108">A cursor is a small picture whose location on the screen is controlled by a pointing device, such as a mouse, pen, or trackball.</span></span> <span data-ttu-id="e2d0f-109">Cuando el usuario mueve el dispositivo señalador, el sistema operativo Windows mueve el cursor.</span><span class="sxs-lookup"><span data-stu-id="e2d0f-109">When the user moves the pointing device, the Windows operating system moves the cursor.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="e2d0f-110">Métodos IAccessible</span><span class="sxs-lookup"><span data-stu-id="e2d0f-110">IAccessible Methods</span></span>

<span data-ttu-id="e2d0f-111">Un cursor admite los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="e2d0f-111">A cursor supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="e2d0f-112">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="e2d0f-112">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="e2d0f-113">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="e2d0f-113">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="iaccessible-properties"></a><span data-ttu-id="e2d0f-114">Propiedades de IAccessible</span><span class="sxs-lookup"><span data-stu-id="e2d0f-114">IAccessible Properties</span></span>

<span data-ttu-id="e2d0f-115">Un cursor admite las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="e2d0f-115">A cursor supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>

-   <span data-ttu-id="e2d0f-116">[**obtener \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount): la propiedad **ChildCount** es cero.</span><span class="sxs-lookup"><span data-stu-id="e2d0f-116">[**get\_accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)—The **ChildCount** property is zero.</span></span>
-   <span data-ttu-id="e2d0f-117">[**obtener \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname): los desarrolladores pueden crear cursores personalizados o usar los cursores predefinidos que se identifican por su ID. de cursor.</span><span class="sxs-lookup"><span data-stu-id="e2d0f-117">[**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)—Developers can create custom cursors or use the predefined cursors that are identified by their cursor ID.</span></span> <span data-ttu-id="e2d0f-118">La propiedad **Name** del cursor depende de su forma y es una de las siguientes:</span><span class="sxs-lookup"><span data-stu-id="e2d0f-118">The **Name** property of the cursor depends on its shape and is one of the following:</span></span> 

    | <span data-ttu-id="e2d0f-119">Forma del cursor</span><span class="sxs-lookup"><span data-stu-id="e2d0f-119">Cursor shape</span></span>     | <span data-ttu-id="e2d0f-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="e2d0f-120">Name</span></span>              |
    |------------------|-------------------|
    | <span data-ttu-id="e2d0f-121">Cursor personalizado</span><span class="sxs-lookup"><span data-stu-id="e2d0f-121">Custom cursor</span></span>    | <span data-ttu-id="e2d0f-122">Unknown</span><span class="sxs-lookup"><span data-stu-id="e2d0f-122">"Unknown"</span></span>         |
    | <span data-ttu-id="e2d0f-123">flecha de IDC \_</span><span class="sxs-lookup"><span data-stu-id="e2d0f-123">IDC\_ARROW</span></span>       | <span data-ttu-id="e2d0f-124">"Normal"</span><span class="sxs-lookup"><span data-stu-id="e2d0f-124">"Normal"</span></span>          |
    | <span data-ttu-id="e2d0f-125">IDC \_ en i</span><span class="sxs-lookup"><span data-stu-id="e2d0f-125">IDC\_IBEAM</span></span>       | <span data-ttu-id="e2d0f-126">Editar</span><span class="sxs-lookup"><span data-stu-id="e2d0f-126">"Edit"</span></span>            |
    | <span data-ttu-id="e2d0f-127">espera de IDC \_</span><span class="sxs-lookup"><span data-stu-id="e2d0f-127">IDC\_WAIT</span></span>        | <span data-ttu-id="e2d0f-128">Currir</span><span class="sxs-lookup"><span data-stu-id="e2d0f-128">"Wait"</span></span>            |
    | <span data-ttu-id="e2d0f-129">Cruz de IDC \_</span><span class="sxs-lookup"><span data-stu-id="e2d0f-129">IDC\_CROSS</span></span>       | <span data-ttu-id="e2d0f-130">Imagen</span><span class="sxs-lookup"><span data-stu-id="e2d0f-130">"Graphic"</span></span>         |
    | <span data-ttu-id="e2d0f-131">\_flecha arriba de IDC</span><span class="sxs-lookup"><span data-stu-id="e2d0f-131">IDC\_UPARROW</span></span>     | <span data-ttu-id="e2d0f-132">Los</span><span class="sxs-lookup"><span data-stu-id="e2d0f-132">"Up"</span></span>              |
    | <span data-ttu-id="e2d0f-133">IDC \_ SIZENWSE</span><span class="sxs-lookup"><span data-stu-id="e2d0f-133">IDC\_SIZENWSE</span></span>    | <span data-ttu-id="e2d0f-134">"Nose size"</span><span class="sxs-lookup"><span data-stu-id="e2d0f-134">"NWSE size"</span></span>       |
    | <span data-ttu-id="e2d0f-135">IDC \_ SIZENESW</span><span class="sxs-lookup"><span data-stu-id="e2d0f-135">IDC\_SIZENESW</span></span>    | <span data-ttu-id="e2d0f-136">"Tamaño de Neso"</span><span class="sxs-lookup"><span data-stu-id="e2d0f-136">"NESW size"</span></span>       |
    | <span data-ttu-id="e2d0f-137">IDC \_ SIZEWE</span><span class="sxs-lookup"><span data-stu-id="e2d0f-137">IDC\_SIZEWE</span></span>      | <span data-ttu-id="e2d0f-138">"Tamaño horizontal"</span><span class="sxs-lookup"><span data-stu-id="e2d0f-138">"Horizontal size"</span></span> |
    | <span data-ttu-id="e2d0f-139">tamaños de IDC \_</span><span class="sxs-lookup"><span data-stu-id="e2d0f-139">IDC\_SIZENS</span></span>      | <span data-ttu-id="e2d0f-140">"Tamaño vertical"</span><span class="sxs-lookup"><span data-stu-id="e2d0f-140">"Vertical size"</span></span>   |
    | <span data-ttu-id="e2d0f-141">IDC \_ SIZEALL</span><span class="sxs-lookup"><span data-stu-id="e2d0f-141">IDC\_SIZEALL</span></span>     | <span data-ttu-id="e2d0f-142">Sube</span><span class="sxs-lookup"><span data-stu-id="e2d0f-142">"Move"</span></span>            |
    | <span data-ttu-id="e2d0f-143">IDC \_ no</span><span class="sxs-lookup"><span data-stu-id="e2d0f-143">IDC\_NO</span></span>          | <span data-ttu-id="e2d0f-144">Permiso</span><span class="sxs-lookup"><span data-stu-id="e2d0f-144">"Forbidden"</span></span>       |
    | <span data-ttu-id="e2d0f-145">IDC \_ APPSTARTING</span><span class="sxs-lookup"><span data-stu-id="e2d0f-145">IDC\_APPSTARTING</span></span> | <span data-ttu-id="e2d0f-146">"Inicio de la aplicación"</span><span class="sxs-lookup"><span data-stu-id="e2d0f-146">"App start"</span></span>       |
    | <span data-ttu-id="e2d0f-147">ayuda de IDC \_</span><span class="sxs-lookup"><span data-stu-id="e2d0f-147">IDC\_HELP</span></span>        | <span data-ttu-id="e2d0f-148">Ayudan</span><span class="sxs-lookup"><span data-stu-id="e2d0f-148">"Help"</span></span>            |

    

     

-   <span data-ttu-id="e2d0f-149">[**obtener \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole): la propiedad de **rol** es [**cursor de \_ sistema \_ de rol**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="e2d0f-149">[**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)—The **Role** property is [**ROLE\_SYSTEM\_CURSOR**](object-roles.md).</span></span>
-   <span data-ttu-id="e2d0f-150">[**obtener \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate): la propiedad **State** es una combinación de uno o varios de los [valores](object-state-constants.md)siguientes:</span><span class="sxs-lookup"><span data-stu-id="e2d0f-150">[**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)—The **State** property is a combination of one or more of the following [values](object-state-constants.md):</span></span>

    <span data-ttu-id="e2d0f-151">[**Estado \_ de sistema \_**](object-state-constants.md) de estado invisible del sistema \| [ **\_ \_ flotante**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="e2d0f-151">[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FLOATING**](object-state-constants.md)</span></span>

## <a name="notes"></a><span data-ttu-id="e2d0f-152">Notas</span><span class="sxs-lookup"><span data-stu-id="e2d0f-152">Notes</span></span>

-   <span data-ttu-id="e2d0f-153">A diferencia de otros elementos de la interfaz de usuario, el objeto Cursor no tiene un identificador de ventana asociado.</span><span class="sxs-lookup"><span data-stu-id="e2d0f-153">Unlike other UI elements, the cursor object does not have an associated window handle.</span></span> <span data-ttu-id="e2d0f-154">Para obtener acceso al objeto cursor, los clientes deben establecer [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) y esperar a que el objeto Cursor genere eventos.</span><span class="sxs-lookup"><span data-stu-id="e2d0f-154">To obtain access to the cursor object, clients must set a [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) and wait for the cursor object to generate events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2d0f-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e2d0f-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2d0f-156">IAccessible (interfaz)</span><span class="sxs-lookup"><span data-stu-id="e2d0f-156">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




