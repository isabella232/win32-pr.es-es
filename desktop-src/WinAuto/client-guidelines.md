---
title: Directrices de cliente
description: Los desarrolladores de cliente deben usar la siguiente funcionalidad para obtener información acerca de los elementos de la interfaz de usuario
ms.assetid: 0e102e60-4d11-490e-88d5-dfadba620781
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ced411c24ed0b7aa3ab97cbe1ce2511d4e6b05
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/29/2020
ms.locfileid: "103994895"
---
# <a name="client-guidelines"></a><span data-ttu-id="b2fff-103">Directrices de cliente</span><span class="sxs-lookup"><span data-stu-id="b2fff-103">Client Guidelines</span></span>

<span data-ttu-id="b2fff-104">Los desarrolladores de cliente deben usar la siguiente funcionalidad para obtener información acerca de los elementos de la interfaz de usuario:</span><span class="sxs-lookup"><span data-stu-id="b2fff-104">Client developers should use the following functionality to get information about the user interface elements:</span></span>

-   <span data-ttu-id="b2fff-105">Para obtener una interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para objetos, llame a [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)o [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).</span><span class="sxs-lookup"><span data-stu-id="b2fff-105">To get an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface to objects, call [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), or [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).</span></span>
-   <span data-ttu-id="b2fff-106">Para examinar y manipular objetos accesibles, use las propiedades y los métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="b2fff-106">To examine and manipulate accessible objects, use the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods.</span></span>
-   <span data-ttu-id="b2fff-107">Para recibir [WinEvents](winevents-overview.md), llame a [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) para registrar una función de devolución de llamada WinEvent para los eventos que son relevantes para la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="b2fff-107">To receive [WinEvents](winevents-overview.md), call [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) to register a WinEvent callback function for those events that are relevant to the client application.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b2fff-108">En esta sección</span><span class="sxs-lookup"><span data-stu-id="b2fff-108">In this section</span></span>

-   [<span data-ttu-id="b2fff-109">Cómo los clientes obtienen los identificadores secundarios</span><span class="sxs-lookup"><span data-stu-id="b2fff-109">How Clients Obtain Child IDs</span></span>](how-clients-obtain-child-ids.md)

 

 




