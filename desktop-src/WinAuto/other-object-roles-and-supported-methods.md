---
title: Otros roles de objeto y métodos admitidos (Referencia de elementos de la interfaz de usuario de MSAA)
description: En este tema se proporciona información sobre los roles de objeto que no se incluyen en los temas anteriores para los elementos de la interfaz de usuario.
ms.assetid: 0c3a3ccf-f02a-4aca-9380-a13774598a19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17e8573142a57e0acf08980895fdae3ea6d1841
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444006"
---
# <a name="other-object-roles-and-supported-methods-msaa-ui-element-reference"></a>Otros roles de objeto y métodos admitidos (Referencia de elementos de la interfaz de usuario de MSAA)

En este tema se proporciona información sobre los roles de objeto que no se incluyen en los temas anteriores para los elementos de la interfaz de usuario. Cada rol de objeto incluye una lista de los métodos y propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) que se admiten para el rol de objeto. Aunque otros temas documentan propiedades y métodos **IAccessible** admitidos para los elementos de la interfaz de usuario, en este tema se enumeran los métodos y propiedades que puede esperar que se admiten para un rol de objeto determinado. Muchos de los elementos de la interfaz de usuario que podrían tener uno de los roles enumerados aquí se suelen ver en los exploradores.

> [!Note]  
> Use este tema como guía. Se recomienda encarecidamente usar herramientas de Microsoft Active Accessibility para comprobar el comportamiento esperado de un rol de objeto individual.

 

En la tabla siguiente se enumeran los roles de objeto adicionales que Oleacc.dll admite.



| &nbsp; |  &nbsp; |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [**ALERTA \_ DEL SISTEMA DE \_ ROL**](/windows)                           | [**LISTA DESPLEGABLE \_ DEL \_ SISTEMA DE ROL**](/windows)       |
| [**APLICACIÓN \_ DEL SISTEMA DE \_ ROLES**](/windows)               | [**ECUACIÓN \_ DEL SISTEMA \_ DE ROL**](/windows)       |
| [**BORDE \_ DEL SISTEMA DE \_ ROL**](/windows)                         | [**GRÁFICO \_ DEL SISTEMA DE \_ ROLES**](/windows)         |
| [**ROLE \_ SYSTEM \_ BUTTONDROPDOWN**](/windows)         | [**ROLE \_ SYSTEM \_ HELPBALLOON**](/windows) |
| [**ROLE \_ SYSTEM \_ BUTTONDROPDOWNGRID**](/windows) | [**ROLE \_ SYSTEM \_ IPADDRESS**](/windows)     |
| [**ROLE \_ SYSTEM \_ BUTTONMENU**](/windows)                 | [**VÍNCULO \_ DEL SISTEMA DE \_ ROLES**](/windows)               |
| [**CELDA \_ DEL SISTEMA DE \_ ROL**](/windows)                             | [**PANEL \_ SISTEMA DE \_ ROL**](/windows)               |
| [**CARÁCTER \_ DEL SISTEMA DE \_ ROLES**](/windows)                   | [**FILA \_ DEL SISTEMA DE \_ ROL**](/windows)                 |
| [**GRÁFICO \_ DEL SISTEMA DE \_ ROLES**](/windows)                           | [**ROLE \_ SYSTEM \_ ROWHEADER**](/windows)     |
| [**RELOJ \_ DEL SISTEMA DE \_ ROL**](/windows)                           | [**SEPARADOR \_ DEL SISTEMA DE \_ ROLES**](/windows)     |
| [**COLUMNA \_ DEL SISTEMA DE \_ ROL**](/windows)                         | [**SONIDO \_ DEL SISTEMA DE \_ ROL**](/windows)             |
| [**DIAGRAMA \_ DEL SISTEMA DE \_ ROLES**](/windows)                       | [**ROLE \_ SYSTEM \_ SPLITBUTTON**](/windows) |
| [**MARCADO \_ DEL SISTEMA DE \_ ROL**](/windows)                             | [**TABLA \_ DEL SISTEMA DE \_ ROLES**](/windows)             |
| [**DOCUMENTO \_ DEL SISTEMA DE \_ ROLES**](/windows)                     | [**ESPACIO \_ EN BLANCO DEL SISTEMA DE \_ ROLES**](/windows)   |



 

## <a name="role_system_alert"></a>ALERTA \_ DEL SISTEMA DE \_ ROL

Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ ALERT**](object-roles.md).

**Propiedades y métodos admitidos**

-   get \_ accName
-   get \_ accRole
-   get \_ accState

## <a name="role_system_application"></a>APLICACIÓN \_ DEL SISTEMA DE \_ ROLES

Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ APPLICATION**](object-roles.md).

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_border"></a>BORDE \_ DEL SISTEMA DE \_ ROL

Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ BORDER**](object-roles.md).

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accRole
-   get \_ accState

## <a name="role_system_buttondropdown"></a>ROLE \_ SYSTEM \_ BUTTONDROPDOWN

Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ BUTTONDROPDOWN**](object-roles.md).

**Propiedades y métodos admitidos**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accDefaultAction
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_buttondropdowngrid"></a>ROLE \_ SYSTEM \_ BUTTONDROPDOWNGRID

Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ BUTTONDROPDOWNGRID**](object-roles.md).

**Propiedades y métodos admitidos**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accDefaultAction
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_buttonmenu"></a>ROLE \_ SYSTEM \_ BUTTONMENU

Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ BUTTONMENU**](object-roles.md).

**Propiedades y métodos admitidos**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accDefaultAction
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_cell"></a>CELDA \_ DEL SISTEMA DE \_ ROL

Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ CELL**](object-roles.md).

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_character"></a>CARÁCTER \_ DEL SISTEMA DE \_ ROLES

Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ CHARACTER**](object-roles.md).

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accDescription
-   get \_ accFocus
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_chart"></a>GRÁFICO \_ DEL SISTEMA DE \_ ROLES

Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ CHART**](object-roles.md).

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_clock"></a>RELOJ \_ DEL SISTEMA DE \_ ROL

Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ CLOCK**](object-roles.md).

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_column"></a>COLUMNA \_ DEL SISTEMA DE \_ ROL

Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ COLUMN**](object-roles.md).

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accFocus
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_diagram"></a>DIAGRAMA \_ DEL SISTEMA DE \_ ROLES

Para obtener más información sobre este rol, vea [**DIAGRAMA DEL SISTEMA DE \_ \_ ROLES**](object-roles.md).

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_dial"></a>MARCADO \_ DEL SISTEMA DE \_ ROL

Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ DIAL**](object-roles.md).

**Propiedades y métodos admitidos**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accDefaultAction
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_document"></a>DOCUMENTO \_ DEL SISTEMA DE \_ ROLES

Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ DOCUMENT**](object-roles.md).

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accFocus
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_droplist"></a>LISTA DESPLEGABLE \_ DEL \_ SISTEMA DE ROL

Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ DROPLIST**](object-roles.md).

**Propiedades y métodos admitidos**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accDefaultAction
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_equation"></a>ECUACIÓN \_ DEL SISTEMA \_ DE ROL

Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ EQUATION**](object-roles.md).

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accFocus
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_graphic"></a>GRÁFICO \_ DEL SISTEMA DE \_ ROLES

Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ GRAPHIC**](object-roles.md).

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_helpballoon"></a>ROLE \_ SYSTEM \_ HELPBALLOON

Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ HELPBALLOON**](object-roles.md).

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accDefaultAction
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_ipaddress"></a>ROLE \_ SYSTEM \_ IPADDRESS

Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ IPADDRESS**](object-roles.md).

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_link"></a>VÍNCULO \_ DEL SISTEMA DE \_ ROLES

Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ LINK**](object-roles.md).

**Propiedades y métodos admitidos**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accDefaultAction
-   get \_ accDescription
-   get \_ accFocus
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_pane"></a>PANEL \_ SISTEMA DE \_ ROL

Para obtener más información sobre este rol, vea [**PANEL DEL SISTEMA DE \_ \_ ROLES**](object-roles.md).

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_row"></a>FILA \_ DEL SISTEMA DE \_ ROL

Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ ROW**](object-roles.md).

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accDescription
-   get \_ accFocus
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_rowheader"></a>ROLE \_ SYSTEM \_ ROWHEADER

Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ ROWHEADER**](object-roles.md).

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accDefaultAction
-   get \_ accDescription
-   get \_ accFocus
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState
-   get \_ accValue

## <a name="role_system_separator"></a>SEPARADOR \_ DEL SISTEMA DE \_ ROLES

Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ SEPARATOR**](object-roles.md).

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_sound"></a>SONIDO \_ DEL SISTEMA DE \_ ROL

Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ SOUND**](object-roles.md).

**Propiedades y métodos admitidos**

-   get \_ accDescription
-   get \_ accName
-   get \_ accRole
-   get \_ accState

## <a name="role_system_splitbutton"></a>ROLE \_ SYSTEM \_ SPLITBUTTON

Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ SPLITBUTTON**](object-roles.md).

**Propiedades y métodos admitidos**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   get \_ accDefaultAction
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_table"></a>TABLA \_ DEL SISTEMA DE \_ ROLES

Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ TABLE**](object-roles.md).

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   get \_ accChild
-   get \_ accChildCount
-   get \_ accDescription
-   get \_ accFocus
-   get \_ accHelp
-   get \_ accHelpTopic
-   get \_ accKeyboardShortcut
-   get \_ accName
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

## <a name="role_system_whitespace"></a>ESPACIO \_ EN BLANCO DEL SISTEMA DE \_ ROLES

Para obtener más información sobre este rol, vea [**ROLE \_ SYSTEM \_ WHITESPACE**](object-roles.md).

**Propiedades y métodos admitidos**

-   accLocation
-   accSelect
-   get \_ accParent
-   get \_ accRole
-   get \_ accState

 

 