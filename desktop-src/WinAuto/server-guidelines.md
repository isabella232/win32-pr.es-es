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
# <a name="server-guidelines"></a>Instrucciones de servidor

Para que Microsoft Active Accessibility funcione según lo previsto, los servidores deben proporcionar información de accesibilidad a los clientes.

Para implementar [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), los desarrolladores de servidor deben seguir este proceso básico.

1.  Cree objetos accesibles implementando las propiedades y los métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para los elementos de la interfaz de usuario personalizados y para el cliente de la aplicación. Asegúrese de proporcionar una interfaz dual que admita **IAccessible** y [**IDispatch**](idispatch-interface.md) para que los clientes escritos en Microsoft Visual Basic y varios lenguajes de scripting puedan obtener información sobre los objetos.
2.  Llame a [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) para notificar a los clientes los cambios en los elementos de la interfaz de usuario personalizados.
3.  Controlar [**WM \_ GETOBJECT**](wm-getobject.md) para proporcionar acceso a los objetos accesibles.

Para obtener sugerencias e instrucciones para el diseño de objetos accesibles, consulte [la guía del desarrollador de servidores de Active Accessibility](developer-s-guide-for-active-accessibility-servers.md).

## <a name="in-this-section"></a>En esta sección

-   [Cómo los servidores implementan identificadores secundarios](how-servers-implement-child-ids.md)

 

 




