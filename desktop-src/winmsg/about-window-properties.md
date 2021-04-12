---
description: En esta información general se describen las propiedades de la ventana.
ms.assetid: 67ca264e-af8e-41bf-b9d1-d3db8cf1cdc3
title: Acerca de las propiedades de la ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea646c594186b05bb74e70e6829f13a83cd0ec1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104276887"
---
# <a name="about-window-properties"></a>Acerca de las propiedades de la ventana

Una *propiedad de ventana* es cualquier dato asignado a una ventana. Una propiedad de ventana suele ser un identificador de los datos específicos de la ventana, pero puede ser cualquier valor. Cada propiedad de ventana se identifica mediante un nombre de cadena. Hay varias funciones que permiten a las aplicaciones usar las propiedades de la ventana. En esta información general se describen los temas siguientes:

-   [Ventajas del uso de las propiedades de ventana](#advantages-of-using-window-properties)
-   [Asignar propiedades de ventana](#assigning-window-properties)
-   [Enumerar propiedades de ventana](#enumerating-window-properties)

## <a name="advantages-of-using-window-properties"></a>Ventajas del uso de las propiedades de ventana

Las propiedades de la ventana se utilizan normalmente para asociar datos con una ventana de subclase o una ventana en una aplicación de interfaz de múltiples documentos (MDI). En cualquier caso, no es conveniente usar los bytes adicionales especificados en la función [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o en la estructura de clases por los dos motivos siguientes:

-   Es posible que una aplicación no sepa cuántos bytes adicionales están disponibles o cómo se utiliza el espacio. Mediante el uso de las propiedades de la ventana, la aplicación puede asociar datos a una ventana sin tener acceso a los bytes adicionales.
-   Una aplicación debe tener acceso a los bytes adicionales mediante desplazamientos. Sin embargo, los identificadores de cadena tienen acceso a las propiedades de la ventana, no los desplazamientos.

Para obtener más información sobre las subclases, vea [subclases de procedimientos de ventana](about-window-procedures.md). Para obtener más información acerca de las ventanas MDI, vea [interfaz de varios documentos](multiple-document-interface.md).

## <a name="assigning-window-properties"></a>Asignar propiedades de ventana

La función [**SetProp**](/windows/win32/api/winuser/nf-winuser-setpropa) asigna una propiedad de ventana y su identificador de cadena a una ventana. La función [**GetProp**](/windows/win32/api/winuser/nf-winuser-getpropa) recupera la propiedad de la ventana identificada por la cadena especificada. La función [**RemoveProp**](/windows/win32/api/winuser/nf-winuser-removepropa) destruye la asociación entre una ventana y una propiedad de ventana, pero no destruye los datos en sí. Para destruir los propios datos, utilice la función adecuada para liberar el identificador devuelto por **RemoveProp**.

## <a name="enumerating-window-properties"></a>Enumerar propiedades de ventana

Las funciones [**EnumProps**](/windows/win32/api/winuser/nf-winuser-enumpropsa) y [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) enumeran todas las propiedades de una ventana mediante una función de devolución de llamada definida por la aplicación. Para obtener más información sobre la función de devolución de llamada, vea [*PropEnumProc*](/windows/win32/api/winuser/nc-winuser-propenumproca).

[**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) incluye un parámetro adicional para los datos definidos por la aplicación que usa la función de devolución de llamada. Para obtener más información sobre la función de devolución de llamada, vea [*PropEnumProcEx*](/windows/win32/api/winuser/nc-winuser-propenumprocexa).

 

 
