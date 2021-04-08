---
title: Otros roles de objeto y métodos admitidos (referencia de elementos de interfaz de usuario de MSAA)
description: En este tema se proporciona información sobre los roles de objeto que no se incluyen en los temas anteriores de los elementos de la interfaz de usuario.
ms.assetid: 0c3a3ccf-f02a-4aca-9380-a13774598a19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3d7fbdbb6dfbf83729f3e1c1d4caa3027f8d51
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792921"
---
# <a name="other-object-roles-and-supported-methods-msaa-ui-element-reference"></a>Otros roles de objeto y métodos admitidos (referencia de elementos de interfaz de usuario de MSAA)

En este tema se proporciona información sobre los roles de objeto que no se incluyen en los temas anteriores de los elementos de la interfaz de usuario. Cada rol de objeto incluye una lista de los métodos y propiedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) que se admiten para el rol de objeto. Mientras que otros temas documentan los métodos y propiedades de **IAccessible** compatibles con los elementos de la interfaz de usuario, en este tema se enumeran los métodos y las propiedades que puede esperar que se admitan para un rol de objeto determinado. Muchos de los elementos de la interfaz de usuario que pueden tener uno de los roles enumerados aquí se suelen ver en los exploradores.

> [!Note]  
> Use este tema como guía. Le recomendamos encarecidamente que use herramientas de Active Accessibility de Microsoft para comprobar el comportamiento esperado de un rol de objeto individual.

 

En la tabla siguiente se enumeran los roles de objeto adicionales que admite Oleacc.dll.



|                                                                         |                                                           |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [**\_alerta del sistema de roles \_**](/windows)                           | [**desplegable sistema de roles \_ \_**](/windows)       |
| [**\_aplicación de sistema de roles \_**](/windows)               | [**\_ecuación del sistema de roles \_**](/windows)       |
| [**\_borde del sistema de roles \_**](/windows)                         | [**\_gráfico del sistema de roles \_**](/windows)         |
| [**\_BUTTONDROPDOWN del sistema de roles \_**](/windows)         | [**\_HELPBALLOON del sistema de roles \_**](/windows) |
| [**\_BUTTONDROPDOWNGRID del sistema de roles \_**](/windows) | [**\_IPAddress del sistema de roles \_**](/windows)     |
| [**\_BUTTONMENU del sistema de roles \_**](/windows)                 | [**\_vínculo del sistema de roles \_**](/windows)               |
| [**\_celda del sistema de roles \_**](/windows)                             | [**\_panel del sistema de roles \_**](/windows)               |
| [**\_carácter de sistema de rol \_**](/windows)                   | [**\_fila del sistema de roles \_**](/windows)                 |
| [**\_gráfico del sistema de roles \_**](/windows)                           | [**\_ROWHEADER del sistema de roles \_**](/windows)     |
| [**\_reloj del sistema de roles \_**](/windows)                           | [**separador de sistema de roles \_ \_**](/windows)     |
| [**\_columna del sistema de roles \_**](/windows)                         | [**\_sonido del sistema de roles \_**](/windows)             |
| [**\_Diagrama del sistema de roles \_**](/windows)                       | [**sistema de roles \_ \_ SPLITBUTTON**](/windows) |
| [**\_marcado del sistema de roles \_**](/windows)                             | [**\_tabla del sistema de roles \_**](/windows)             |
| [**\_documento de sistema de roles \_**](/windows)                     | [**\_espacio en blanco del sistema de roles \_**](/windows)   |



 

## <a name="role_system_alert"></a>\_alerta del sistema de roles \_

Para obtener más información sobre este rol, [**consulte \_ \_ alerta del sistema de roles**](object-roles.md).

**Propiedades y métodos admitidos**

-   obtener \_ accName
-   obtener \_ accRole
-   obtener \_ accState

## <a name="role_system_application"></a>\_aplicación de sistema de roles \_

Para obtener más información sobre este rol, [**vea \_ \_ aplicación de sistema de roles**](object-roles.md).

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   accNavigate
-   obtener \_ accChild
-   obtener \_ accChildCount
-   obtener \_ accFocus
-   obtener \_ accHelp
-   obtener \_ accHelpTopic
-   obtener \_ accKeyboardShortcut
-   obtener \_ accName
-   obtener \_ accParent
-   obtener \_ accRole
-   obtener \_ accState

## <a name="role_system_border"></a>\_borde del sistema de roles \_

Para obtener más información sobre este rol, [**vea \_ \_ borde del sistema de roles**](object-roles.md).

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   accNavigate
-   obtener \_ accRole
-   obtener \_ accState

## <a name="role_system_buttondropdown"></a>\_BUTTONDROPDOWN del sistema de roles \_

Para obtener más información sobre este rol, [**consulte \_ \_ BUTTONDROPDOWN de sistema de roles**](object-roles.md).

**Propiedades y métodos admitidos**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   obtener \_ accChild
-   obtener \_ accChildCount
-   obtener \_ accDefaultAction
-   obtener \_ accFocus
-   obtener \_ accHelp
-   obtener \_ accHelpTopic
-   obtener \_ accKeyboardShortcut
-   obtener \_ accName
-   obtener \_ accParent
-   obtener \_ accRole
-   obtener \_ accState

## <a name="role_system_buttondropdowngrid"></a>\_BUTTONDROPDOWNGRID del sistema de roles \_

Para obtener más información sobre este rol, [**consulte \_ \_ BUTTONDROPDOWNGRID de sistema de roles**](object-roles.md).

**Propiedades y métodos admitidos**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   obtener \_ accChild
-   obtener \_ accChildCount
-   obtener \_ accDefaultAction
-   obtener \_ accFocus
-   obtener \_ accHelp
-   obtener \_ accHelpTopic
-   obtener \_ accKeyboardShortcut
-   obtener \_ accName
-   obtener \_ accParent
-   obtener \_ accRole
-   obtener \_ accState

## <a name="role_system_buttonmenu"></a>\_BUTTONMENU del sistema de roles \_

Para obtener más información sobre este rol, vea el caso de la función [**\_ \_ BUTTONMENU del sistema de roles**](object-roles.md).

**Propiedades y métodos admitidos**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   obtener \_ accDefaultAction
-   obtener \_ accFocus
-   obtener \_ accHelp
-   obtener \_ accHelpTopic
-   obtener \_ accKeyboardShortcut
-   obtener \_ accName
-   obtener \_ accParent
-   obtener \_ accRole
-   obtener \_ accState

## <a name="role_system_cell"></a>\_celda del sistema de roles \_

Para obtener más información sobre este rol, [**consulte \_ \_ celda del sistema de roles**](object-roles.md).

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   obtener \_ accChild
-   obtener \_ accChildCount
-   obtener \_ accFocus
-   obtener \_ accHelp
-   obtener \_ accHelpTopic
-   obtener \_ accKeyboardShortcut
-   obtener \_ accName
-   obtener \_ accParent
-   obtener \_ accRole
-   obtener \_ accState
-   obtener \_ accValue

## <a name="role_system_character"></a>\_carácter de sistema de rol \_

Para obtener más información sobre este rol, [**vea \_ \_ carácter de sistema de rol**](object-roles.md).

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   accNavigate
-   obtener \_ accDescription
-   obtener \_ accFocus
-   obtener \_ accKeyboardShortcut
-   obtener \_ accName
-   obtener \_ accParent
-   obtener \_ accRole
-   obtener \_ accState
-   obtener \_ accValue

## <a name="role_system_chart"></a>\_gráfico del sistema de roles \_

Para más información sobre este rol, consulte [**el \_ \_ gráfico del sistema de roles**](object-roles.md).

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   accNavigate
-   obtener \_ accChild
-   obtener \_ accChildCount
-   obtener \_ accFocus
-   obtener \_ accHelp
-   obtener \_ accHelpTopic
-   obtener \_ accKeyboardShortcut
-   obtener \_ accName
-   obtener \_ accParent
-   obtener \_ accRole
-   obtener \_ accState

## <a name="role_system_clock"></a>\_reloj del sistema de roles \_

Para obtener más información sobre este rol, consulte el [**\_ \_ reloj del sistema de roles**](object-roles.md).

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   accNavigate
-   obtener \_ accFocus
-   obtener \_ accHelp
-   obtener \_ accHelpTopic
-   obtener \_ accKeyboardShortcut
-   obtener \_ accName
-   obtener \_ accParent
-   obtener \_ accRole
-   obtener \_ accState
-   obtener \_ accValue

## <a name="role_system_column"></a>\_columna del sistema de roles \_

Para obtener más información sobre este rol, consulte la [**\_ \_ columna sistema de rol**](object-roles.md).

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   obtener \_ accChild
-   obtener \_ accChildCount
-   obtener \_ accFocus
-   obtener \_ accName
-   obtener \_ accParent
-   obtener \_ accRole
-   obtener \_ accState
-   obtener \_ accValue

## <a name="role_system_diagram"></a>\_Diagrama del sistema de roles \_

Para obtener más información sobre este rol, [**vea \_ \_ Diagrama de sistema de roles**](object-roles.md).

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   accNavigate
-   obtener \_ accChild
-   obtener \_ accChildCount
-   obtener \_ accFocus
-   obtener \_ accHelp
-   obtener \_ accHelpTopic
-   obtener \_ accKeyboardShortcut
-   obtener \_ accName
-   obtener \_ accParent
-   obtener \_ accRole
-   obtener \_ accState

## <a name="role_system_dial"></a>\_marcado del sistema de roles \_

Para obtener más información sobre este rol, [**consulte \_ \_ marcado del sistema de roles**](object-roles.md).

**Propiedades y métodos admitidos**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   obtener \_ accDefaultAction
-   obtener \_ accFocus
-   obtener \_ accHelp
-   obtener \_ accHelpTopic
-   obtener \_ accKeyboardShortcut
-   obtener \_ accName
-   obtener \_ accParent
-   obtener \_ accRole
-   obtener \_ accState
-   obtener \_ accValue

## <a name="role_system_document"></a>\_documento de sistema de roles \_

Para obtener más información sobre este rol, consulte el [**\_ \_ documento**](object-roles.md)sobre el sistema de roles.

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   obtener \_ accChild
-   obtener \_ accChildCount
-   obtener \_ accFocus
-   obtener \_ accName
-   obtener \_ accParent
-   obtener \_ accRole
-   obtener \_ accState

## <a name="role_system_droplist"></a>desplegable sistema de roles \_ \_

Para obtener más información sobre este rol, vea el apartado de la [**\_ \_ desplegable del sistema de roles**](object-roles.md).

**Propiedades y métodos admitidos**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   obtener \_ accChild
-   obtener \_ accChildCount
-   obtener \_ accDefaultAction
-   obtener \_ accFocus
-   obtener \_ accHelp
-   obtener \_ accHelpTopic
-   obtener \_ accKeyboardShortcut
-   obtener \_ accName
-   obtener \_ accParent
-   obtener \_ accRole
-   obtener \_ accState

## <a name="role_system_equation"></a>\_ecuación del sistema de roles \_

Para obtener más información sobre este rol, [**vea \_ \_ ecuación del sistema de roles**](object-roles.md).

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   accNavigate
-   obtener \_ accFocus
-   obtener \_ accName
-   obtener \_ accParent
-   obtener \_ accRole
-   obtener \_ accState
-   obtener \_ accValue

## <a name="role_system_graphic"></a>\_gráfico del sistema de roles \_

Para obtener más información sobre este rol, consulte el [**\_ \_ gráfico del sistema de roles**](object-roles.md).

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   accNavigate
-   obtener \_ accFocus
-   obtener \_ accHelp
-   obtener \_ accHelpTopic
-   obtener \_ accKeyboardShortcut
-   obtener \_ accName
-   obtener \_ accParent
-   obtener \_ accRole
-   obtener \_ accState

## <a name="role_system_helpballoon"></a>\_HELPBALLOON del sistema de roles \_

Para obtener más información sobre este rol, [**consulte \_ \_ HELPBALLOON de sistema de roles**](object-roles.md).

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   accNavigate
-   obtener \_ accChild
-   obtener \_ accChildCount
-   obtener \_ accDefaultAction
-   obtener \_ accName
-   obtener \_ accParent
-   obtener \_ accRole
-   obtener \_ accState
-   obtener \_ accValue

## <a name="role_system_ipaddress"></a>\_IPAddress del sistema de roles \_

Para obtener más información sobre este rol, [**consulte \_ \_ IPAddress del sistema de roles**](object-roles.md).

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   accNavigate
-   obtener \_ accChild
-   obtener \_ accChildCount
-   obtener \_ accFocus
-   obtener \_ accHelp
-   obtener \_ accHelpTopic
-   obtener \_ accKeyboardShortcut
-   obtener \_ accName
-   obtener \_ accParent
-   obtener \_ accRole
-   obtener \_ accState
-   obtener \_ accValue

## <a name="role_system_link"></a>\_vínculo del sistema de roles \_

Para obtener más información sobre este rol, [**consulte \_ \_ vínculo del sistema de roles**](object-roles.md).

**Propiedades y métodos admitidos**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   obtener \_ accChild
-   obtener \_ accChildCount
-   obtener \_ accDefaultAction
-   obtener \_ accDescription
-   obtener \_ accFocus
-   obtener \_ accKeyboardShortcut
-   obtener \_ accName
-   obtener \_ accParent
-   obtener \_ accRole
-   obtener \_ accState
-   obtener \_ accValue

## <a name="role_system_pane"></a>\_panel del sistema de roles \_

Para obtener más información sobre este rol, [**consulte \_ \_ panel del sistema de roles**](object-roles.md).

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   accNavigate
-   obtener \_ accChild
-   obtener \_ accChildCount
-   obtener \_ accFocus
-   obtener \_ accHelp
-   obtener \_ accHelpTopic
-   obtener \_ accKeyboardShortcut
-   obtener \_ accName
-   obtener \_ accParent
-   obtener \_ accRole
-   obtener \_ accState

## <a name="role_system_row"></a>\_fila del sistema de roles \_

Para obtener más información sobre este rol, vea rol de la [**\_ \_ fila de sistema**](object-roles.md).

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   obtener \_ accChild
-   obtener \_ accChildCount
-   obtener \_ accDescription
-   obtener \_ accFocus
-   obtener \_ accName
-   obtener \_ accParent
-   obtener \_ accRole
-   obtener \_ accState
-   obtener \_ accValue

## <a name="role_system_rowheader"></a>\_ROWHEADER del sistema de roles \_

Para obtener más información sobre este rol, [**consulte \_ \_ ROWHEADER de sistema de roles**](object-roles.md).

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   obtener \_ accChild
-   obtener \_ accChildCount
-   obtener \_ accDefaultAction
-   obtener \_ accDescription
-   obtener \_ accFocus
-   obtener \_ accName
-   obtener \_ accParent
-   obtener \_ accRole
-   obtener \_ accState
-   obtener \_ accValue

## <a name="role_system_separator"></a>separador de sistema de roles \_ \_

Para obtener más información sobre este rol, [**consulte \_ \_ separador de sistema de roles**](object-roles.md).

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   obtener \_ accChild
-   obtener \_ accChildCount
-   obtener \_ accParent
-   obtener \_ accRole
-   obtener \_ accState

## <a name="role_system_sound"></a>\_sonido del sistema de roles \_

Para obtener más información sobre este rol, [**vea \_ \_ sonido del sistema de funciones**](object-roles.md).

**Propiedades y métodos admitidos**

-   obtener \_ accDescription
-   obtener \_ accName
-   obtener \_ accRole
-   obtener \_ accState

## <a name="role_system_splitbutton"></a>sistema de roles \_ \_ SPLITBUTTON

Para obtener más información sobre este rol, vea [**rol \_ System \_ SPLITBUTTON**](object-roles.md).

**Propiedades y métodos admitidos**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   obtener \_ accDefaultAction
-   obtener \_ accHelp
-   obtener \_ accHelpTopic
-   obtener \_ accKeyboardShortcut
-   obtener \_ accName
-   obtener \_ accParent
-   obtener \_ accRole
-   obtener \_ accState

## <a name="role_system_table"></a>\_tabla del sistema de roles \_

Para obtener más información sobre este rol, [**consulte \_ \_ tabla del sistema de roles**](object-roles.md).

**Propiedades y métodos admitidos**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   obtener \_ accChild
-   obtener \_ accChildCount
-   obtener \_ accDescription
-   obtener \_ accFocus
-   obtener \_ accHelp
-   obtener \_ accHelpTopic
-   obtener \_ accKeyboardShortcut
-   obtener \_ accName
-   obtener \_ accParent
-   obtener \_ accRole
-   obtener \_ accState

## <a name="role_system_whitespace"></a>\_espacio en blanco del sistema de roles \_

Para obtener más información sobre este rol, [**vea \_ \_ espacio en blanco del sistema de roles**](object-roles.md).

**Propiedades y métodos admitidos**

-   accLocation
-   accSelect
-   obtener \_ accParent
-   obtener \_ accRole
-   obtener \_ accState

 

 