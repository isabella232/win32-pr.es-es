---
title: Cursor (Referencia del elemento de interfaz de usuario de MSAA)
description: Un cursor es una imagen pequeña cuya ubicación en la pantalla se controla mediante un dispositivo que apunta, como un mouse, un lápiz o un trackball. Cuando el usuario mueve el dispositivo que apunta, el Windows operativo mueve el cursor.
ms.assetid: ff97d474-7c96-4f89-bc34-2cf320381ce0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff351040d342adccda8cb03d56d91f9dc429074f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174918"
---
# <a name="cursor-msaa-ui-element-reference"></a>Cursor (Referencia del elemento de interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen los cursores para fines de referencia de elementos de la interfaz de usuario de MSAA. Aquí no se describe cómo usar cursores en varios marcos de interfaz de usuario. Consulte la documentación de referencia de API para el marco de interfaz de usuario que está usando.

 

Un cursor es una imagen pequeña cuya ubicación en la pantalla se controla mediante un dispositivo que apunta, como un mouse, un lápiz o un trackball. Cuando el usuario mueve el dispositivo que apunta, el Windows operativo mueve el cursor.

## <a name="iaccessible-methods"></a>Métodos IAccessible

Un cursor admite los siguientes métodos [**IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="iaccessible-properties"></a>Propiedades IAccessible

Un cursor admite las siguientes [**propiedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount): la **propiedad ChildCount** es cero.
-   [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname): los desarrolladores pueden crear cursores personalizados o usar los cursores predefinidos que se identifican por su identificador de cursor. La **propiedad Name** del cursor depende de su forma y es una de las siguientes: 

    | Forma del cursor     | Nombre              |
    |------------------|-------------------|
    | Cursor personalizado    | "Desconocido"         |
    | FLECHA DE \_ IDC       | "Normal"          |
    | IDC \_ IBEAM       | "Editar"            |
    | IDC \_ WAIT        | "Esperar"            |
    | IDC \_ CROSS       | "Gráfico"         |
    | IDC \_ UPARROW     | "Up"              |
    | TAMAÑO DE \_ IDCNWSE    | "Tamaño de NWSE"       |
    | TAMAÑO DE \_ IDCNESW    | "Tamaño de NESW"       |
    | TAMAÑO DE \_ IDCWE      | "Tamaño horizontal" |
    | TAMAÑO DE \_ IDC      | "Tamaño vertical"   |
    | TAMAÑO DE \_ IDCALL     | "Mover"            |
    | IDC \_ NO          | "Prohibido"       |
    | IDC \_ APPSTARTING | "Inicio de la aplicación"       |
    | AYUDA DE \_ IDC        | "Ayuda"            |

    

     

-   [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole): la **propiedad Role** es ROLE SYSTEM [**\_ \_ CURSOR**](object-roles.md).
-   [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate): la **propiedad State** es una combinación de uno o varios de los valores [siguientes:](object-state-constants.md)

    [**STATE \_ FLOTANTE \_ DEL SISTEMA DE**](object-state-constants.md) ESTADO INVISIBLE \| [ **DEL \_ \_ SISTEMA**](object-state-constants.md)

## <a name="notes"></a>Notas

-   A diferencia de otros elementos de la interfaz de usuario, el objeto de cursor no tiene un identificador de ventana asociado. Para obtener acceso al objeto de cursor, los clientes deben establecer [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) y esperar a que el objeto de cursor genere eventos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaz IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




