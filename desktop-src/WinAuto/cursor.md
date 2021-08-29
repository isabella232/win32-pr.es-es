---
title: Cursor (Referencia del elemento de interfaz de usuario de MSAA)
description: Un cursor es una imagen pequeña cuya ubicación en la pantalla se controla mediante un dispositivo que apunta, como un mouse, un lápiz o un trackball. Cuando el usuario mueve el dispositivo que apunta, Windows sistema operativo mueve el cursor.
ms.assetid: ff97d474-7c96-4f89-bc34-2cf320381ce0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52140da712c5fb889a12c466a34f8587c7291664fd774ac71a3f877031ce30b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118830084"
---
# <a name="cursor-msaa-ui-element-reference"></a>Cursor (Referencia del elemento de interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen los cursores para fines de referencia de elementos de la interfaz de usuario de MSAA. Aquí no se describe cómo usar cursores en varios marcos de interfaz de usuario. Consulte la documentación de referencia de API para el marco de interfaz de usuario que está usando.

 

Un cursor es una imagen pequeña cuya ubicación en la pantalla se controla mediante un dispositivo que apunta, como un mouse, un lápiz o un trackball. Cuando el usuario mueve el dispositivo que apunta, Windows sistema operativo mueve el cursor.

## <a name="iaccessible-methods"></a>Métodos IAccessible

Un cursor admite los siguientes métodos [**IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="iaccessible-properties"></a>Propiedades IAccessible

Un cursor admite las siguientes [**propiedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount): la **propiedad ChildCount** es cero.
-   [**get \_ accName:**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)los desarrolladores pueden crear cursores personalizados o usar los cursores predefinidos identificados por su identificador de cursor. La **propiedad Name** del cursor depende de su forma y es una de las siguientes: 

    | Forma del cursor     | Nombre              |
    |------------------|-------------------|
    | Cursor personalizado    | "Desconocido"         |
    | FLECHA DE \_ IDC       | "Normal"          |
    | IDC \_ IBEAM       | "Editar"            |
    | IDC \_ WAIT        | "Esperar"            |
    | IDC \_ CROSS       | "Gráfico"         |
    | IDC \_ UPARROW     | "Up"              |
    | IDC \_ SIZENWSE    | "Tamaño de NWSE"       |
    | IDC \_ SIZENESW    | "Tamaño de NESW"       |
    | IDC \_ SIZEWE      | "Tamaño horizontal" |
    | IDC \_ SIZENS      | "Tamaño vertical"   |
    | IDC \_ SIZEALL     | "Mover"            |
    | IDC \_ NO          | "Prohibido"       |
    | IDC \_ APPSTARTING | "Inicio de la aplicación"       |
    | AYUDA DE \_ IDC        | "Ayuda"            |

    

     

-   [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole): la **propiedad Role** es ROLE SYSTEM [**\_ \_ CURSOR**](object-roles.md).
-   [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate): la **propiedad State** es una combinación de uno o varios de los valores [siguientes:](object-state-constants.md)

    [**STATE \_ SISTEMA \_ FLOTANTE DEL SISTEMA DE**](object-state-constants.md) ESTADO INVISIBLE DEL \| [ **\_ \_ SISTEMA**](object-state-constants.md)

## <a name="notes"></a>Notas

-   A diferencia de otros elementos de la interfaz de usuario, el objeto de cursor no tiene un identificador de ventana asociado. Para obtener acceso al objeto de cursor, los clientes deben establecer [*winEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) y esperar a que el objeto de cursor genere eventos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (Interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




