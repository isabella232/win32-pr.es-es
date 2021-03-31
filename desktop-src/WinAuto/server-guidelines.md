---
title: Instrucciones de servidor
description: Para que Microsoft Active Accessibility funcione según lo previsto, los servidores deben proporcionar información de accesibilidad a los clientes.
ms.assetid: 88be4bae-fdeb-467c-b5b1-19f2adc0575d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 344721428c94e2ea3d9e9ff78e194851ba9304db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418465"
---
# <a name="server-guidelines"></a><span data-ttu-id="dadf5-103">Instrucciones de servidor</span><span class="sxs-lookup"><span data-stu-id="dadf5-103">Server Guidelines</span></span>

<span data-ttu-id="dadf5-104">Para que Microsoft Active Accessibility funcione según lo previsto, los servidores deben proporcionar información de accesibilidad a los clientes.</span><span class="sxs-lookup"><span data-stu-id="dadf5-104">For Microsoft Active Accessibility to work as designed, servers must provide accessibility information to clients.</span></span>

<span data-ttu-id="dadf5-105">Para implementar [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), los desarrolladores de servidor deben seguir este proceso básico.</span><span class="sxs-lookup"><span data-stu-id="dadf5-105">To implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), server developers must follow this basic process.</span></span>

1.  <span data-ttu-id="dadf5-106">Cree objetos accesibles implementando las propiedades y los métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para los elementos de la interfaz de usuario personalizados y para el cliente de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="dadf5-106">Create accessible objects by implementing the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods for your custom user interface elements and for your application's client.</span></span> <span data-ttu-id="dadf5-107">Asegúrese de proporcionar una interfaz dual que admita **IAccessible** y [**IDispatch**](idispatch-interface.md) para que los clientes escritos en Microsoft Visual Basic y varios lenguajes de scripting puedan obtener información sobre los objetos.</span><span class="sxs-lookup"><span data-stu-id="dadf5-107">Be sure to provide a dual interface that supports both **IAccessible** and [**IDispatch**](idispatch-interface.md) so that clients written in Microsoft Visual Basic and various scripting languages can get information about the objects.</span></span>
2.  <span data-ttu-id="dadf5-108">Llame a [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) para notificar a los clientes los cambios en los elementos de la interfaz de usuario personalizados.</span><span class="sxs-lookup"><span data-stu-id="dadf5-108">Call [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) to notify clients of changes to your custom user interface elements.</span></span>
3.  <span data-ttu-id="dadf5-109">Controlar [**WM \_ GETOBJECT**](wm-getobject.md) para proporcionar acceso a los objetos accesibles.</span><span class="sxs-lookup"><span data-stu-id="dadf5-109">Handle [**WM\_GETOBJECT**](wm-getobject.md) to provide access to your accessible objects.</span></span>

<span data-ttu-id="dadf5-110">Para obtener sugerencias e instrucciones para el diseño de objetos accesibles, consulte [la guía del desarrollador de servidores de Active Accessibility](developer-s-guide-for-active-accessibility-servers.md).</span><span class="sxs-lookup"><span data-stu-id="dadf5-110">For suggestions and guidelines for designing accessible objects, see [Developer's Guide for Active Accessibility Servers](developer-s-guide-for-active-accessibility-servers.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="dadf5-111">En esta sección</span><span class="sxs-lookup"><span data-stu-id="dadf5-111">In this section</span></span>

-   [<span data-ttu-id="dadf5-112">Cómo los servidores implementan identificadores secundarios</span><span class="sxs-lookup"><span data-stu-id="dadf5-112">How Servers Implement Child IDs</span></span>](how-servers-implement-child-ids.md)

 

 




