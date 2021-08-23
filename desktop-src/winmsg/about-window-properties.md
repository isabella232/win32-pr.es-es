---
description: Esta información general describe las propiedades de la ventana.
ms.assetid: 67ca264e-af8e-41bf-b9d1-d3db8cf1cdc3
title: Acerca de las propiedades de ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c88657cba4cf12ed7ecedb07aeb545f8e4bf64109d34297637d734743d32dd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028503"
---
# <a name="about-window-properties"></a>Acerca de las propiedades de ventana

Una *propiedad de ventana* es cualquier dato asignado a una ventana. Una propiedad de ventana suele ser un identificador de los datos específicos de la ventana, pero puede ser cualquier valor. Cada propiedad de ventana se identifica mediante un nombre de cadena. Hay varias funciones que permiten a las aplicaciones usar propiedades de ventana. En esta introducción se de abordan los temas siguientes:

-   [Ventajas de usar propiedades de ventana](#advantages-of-using-window-properties)
-   [Asignar propiedades de ventana](#assigning-window-properties)
-   [Enumerar propiedades de ventana](#enumerating-window-properties)

## <a name="advantages-of-using-window-properties"></a>Ventajas de usar propiedades de ventana

Las propiedades de ventana se usan normalmente para asociar datos a una ventana con subclases o a una ventana en una aplicación de interfaz de varios documentos (MDI). En cualquier caso, no es conveniente usar los bytes adicionales especificados en la función [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o la estructura de clase por los dos motivos siguientes:

-   Es posible que una aplicación no sepa cuántos bytes adicionales hay disponibles o cómo se usa el espacio. Mediante el uso de propiedades de ventana, la aplicación puede asociar datos a una ventana sin tener acceso a los bytes adicionales.
-   Una aplicación debe tener acceso a los bytes adicionales mediante desplazamientos. Sin embargo, se accede a las propiedades de ventana mediante sus identificadores de cadena, no mediante desplazamientos.

Para obtener más información sobre las subclases, vea [Subclases de procedimiento de ventana](about-window-procedures.md). Para obtener más información sobre las ventanas MDI, vea [Multiple Document Interface](multiple-document-interface.md).

## <a name="assigning-window-properties"></a>Asignar propiedades de ventana

La [**función SetProp**](/windows/win32/api/winuser/nf-winuser-setpropa) asigna una propiedad de ventana y su identificador de cadena a una ventana. La [**función GetProp**](/windows/win32/api/winuser/nf-winuser-getpropa) recupera la propiedad de ventana identificada por la cadena especificada. La [**función RemoveProp**](/windows/win32/api/winuser/nf-winuser-removepropa) destruye la asociación entre una ventana y una propiedad de ventana, pero no destruye los propios datos. Para destruir los propios datos, use la función adecuada para liberar el identificador devuelto por **RemoveProp**.

## <a name="enumerating-window-properties"></a>Enumerar propiedades de ventana

Las [**funciones EnumProps**](/windows/win32/api/winuser/nf-winuser-enumpropsa) y [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) enumeran todas las propiedades de una ventana mediante una función de devolución de llamada definida por la aplicación. Para obtener más información sobre la función de devolución de llamada, [*vea PropEnumProc*](/windows/win32/api/winuser/nc-winuser-propenumproca).

[**EnumPropsEx incluye**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) un parámetro adicional para los datos definidos por la aplicación que usa la función de devolución de llamada. Para obtener más información sobre la función de devolución de llamada, [*vea PropEnumProcEx*](/windows/win32/api/winuser/nc-winuser-propenumprocexa).

 

 
