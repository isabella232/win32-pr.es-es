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
# <a name="cursor-msaa-ui-element-reference"></a>Cursor (referencia de elementos de interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen los cursores para la referencia de elementos de la interfaz de usuario de MSAA. El uso de cursores en varios marcos de interfaz de usuario no se describe aquí. Consulte la documentación de referencia de la API del marco de interfaz de usuario que está usando.

 

Un cursor es una pequeña imagen cuya ubicación en la pantalla está controlada por un dispositivo señalador, como un mouse, un lápiz o un trackball. Cuando el usuario mueve el dispositivo señalador, el sistema operativo Windows mueve el cursor.

## <a name="iaccessible-methods"></a>Métodos IAccessible

Un cursor admite los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="iaccessible-properties"></a>Propiedades de IAccessible

Un cursor admite las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**obtener \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount): la propiedad **ChildCount** es cero.
-   [**obtener \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname): los desarrolladores pueden crear cursores personalizados o usar los cursores predefinidos que se identifican por su ID. de cursor. La propiedad **Name** del cursor depende de su forma y es una de las siguientes: 

    | Forma del cursor     | Nombre              |
    |------------------|-------------------|
    | Cursor personalizado    | Unknown         |
    | flecha de IDC \_       | "Normal"          |
    | IDC \_ en i       | Editar            |
    | espera de IDC \_        | Currir            |
    | Cruz de IDC \_       | Imagen         |
    | \_flecha arriba de IDC     | Los              |
    | IDC \_ SIZENWSE    | "Nose size"       |
    | IDC \_ SIZENESW    | "Tamaño de Neso"       |
    | IDC \_ SIZEWE      | "Tamaño horizontal" |
    | tamaños de IDC \_      | "Tamaño vertical"   |
    | IDC \_ SIZEALL     | Sube            |
    | IDC \_ no          | Permiso       |
    | IDC \_ APPSTARTING | "Inicio de la aplicación"       |
    | ayuda de IDC \_        | Ayudan            |

    

     

-   [**obtener \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole): la propiedad de **rol** es [**cursor de \_ sistema \_ de rol**](object-roles.md).
-   [**obtener \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate): la propiedad **State** es una combinación de uno o varios de los [valores](object-state-constants.md)siguientes:

    [**Estado \_ de sistema \_**](object-state-constants.md) de estado invisible del sistema \| [ **\_ \_ flotante**](object-state-constants.md)

## <a name="notes"></a>Notas

-   A diferencia de otros elementos de la interfaz de usuario, el objeto Cursor no tiene un identificador de ventana asociado. Para obtener acceso al objeto cursor, los clientes deben establecer [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) y esperar a que el objeto Cursor genere eventos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




