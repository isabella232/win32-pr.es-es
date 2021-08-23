---
title: Instrucciones del servidor
description: Para Microsoft Active Accessibility funcione según lo diseñado, los servidores deben proporcionar información de accesibilidad a los clientes.
ms.assetid: 88be4bae-fdeb-467c-b5b1-19f2adc0575d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b92d70a33dc8d397ff84fc3b9901dba044741d3044f6a7b7f6d1226aa5b683
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614555"
---
# <a name="server-guidelines"></a>Instrucciones del servidor

Para Microsoft Active Accessibility funcione según lo diseñado, los servidores deben proporcionar información de accesibilidad a los clientes.

Para implementar [**IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)los desarrolladores de servidores deben seguir este proceso básico.

1.  Cree objetos accesibles mediante la implementación de las propiedades y métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para los elementos de la interfaz de usuario personalizada y para el cliente de la aplicación. Asegúrese de proporcionar una interfaz dual que admita **IAccessible** e [**IDispatch**](idispatch-interface.md) para que los clientes escritos en Microsoft Visual Basic y varios lenguajes de scripting puedan obtener información sobre los objetos.
2.  Llame [**a NotifyWinEvent para**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) notificar a los clientes los cambios en los elementos de la interfaz de usuario personalizada.
3.  Controle [**WM \_ GETOBJECT**](wm-getobject.md) para proporcionar acceso a los objetos accesibles.

Para obtener sugerencias e instrucciones para diseñar objetos accesibles, vea [Developer's Guide for Active Accessibility Servers](developer-s-guide-for-active-accessibility-servers.md).

## <a name="in-this-section"></a>En esta sección

-   [Cómo implementan los servidores los IDs secundarios](how-servers-implement-child-ids.md)

 

 




