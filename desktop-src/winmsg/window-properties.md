---
description: En esta sección se de abordan las propiedades de la ventana. Una propiedad de ventana es cualquier dato asignado a una ventana.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\windowproperties.htm
title: Propiedades de la ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a06be9fca67dedeb98afd7a56638622dabc858
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572233"
---
# <a name="window-properties"></a>Propiedades de la ventana

Una propiedad de ventana es cualquier dato asignado a una ventana. Una propiedad de ventana suele ser un identificador de los datos específicos de la ventana, pero puede ser cualquier valor. Cada propiedad de ventana se identifica mediante un nombre de cadena.

### <a name="in-this-section"></a>En esta sección



| Nombre                                                       | Descripción                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Acerca de las propiedades de la ventana](about-window-properties.md)     | Describe las propiedades de la ventana.<br/>                                                   |
| [Usar propiedades de ventana](using-window-properties.md)     | Explica cómo realizar las siguientes tareas asociadas a las propiedades de la ventana.<br/> |
| [Referencia de propiedades de ventana](window-property-reference.md) | Contiene la referencia de API.<br/>                                                    |



 

### <a name="window-property-functions"></a>Funciones de propiedad de ventana



| Nombre                                   | Descripción                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumProps**](/windows/win32/api/winuser/nf-winuser-enumpropsa)         | Enumera todas las entradas de la lista de propiedades de una ventana pasandolas, una a una, a la función de devolución de llamada especificada. [**EnumProps continúa**](/windows/win32/api/winuser/nf-winuser-enumpropsa) hasta que se enumera la última entrada o la función de devolución de llamada devuelve **FALSE.**<br/>                                                                                                        |
| [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa)     | Enumera todas las entradas de la lista de propiedades de una ventana pasandolas, una a una, a la función de devolución de llamada especificada. [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) continúa hasta que se enumera la última entrada o la función de devolución de llamada devuelve **FALSE.** <br/>                                                                                                  |
| [**GetProp**](/windows/win32/api/winuser/nf-winuser-getpropa)             | Recupera un identificador de datos de la lista de propiedades de la ventana especificada. La cadena de caracteres identifica el identificador que se va a recuperar. La cadena y el identificador deben haber sido agregados a la lista de propiedades mediante una llamada anterior a la [**función SetProp.**](/windows/win32/api/winuser/nf-winuser-setpropa) <br/>                                                                                    |
| [*PropEnumProc*](/windows/win32/api/winuser/nc-winuser-propenumproca)     | Función de devolución de llamada definida por la aplicación que se usa con [**la función EnumProps.**](/windows/win32/api/winuser/nf-winuser-enumpropsa) La función recibe entradas de propiedad de la lista de propiedades de una ventana. El **tipo PROPENUMPROC** define un puntero a esta función de devolución de llamada. [*PropEnumProc es*](/windows/win32/api/winuser/nc-winuser-propenumproca) un marcador de posición para el nombre de función definido por la aplicación. <br/>           |
| [*PropEnumProcEx*](/windows/win32/api/winuser/nc-winuser-propenumprocexa) | Función de devolución de llamada definida por la aplicación que se usa con [**la función EnumPropsEx.**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) La función recibe entradas de propiedad de la lista de propiedades de una ventana. El **tipo PROPENUMPROCEX** define un puntero a esta función de devolución de llamada. [*PropEnumProcEx es*](/windows/win32/api/winuser/nc-winuser-propenumprocexa) un marcador de posición para el nombre de la función definida por la aplicación. <br/> |
| [**RemoveProp**](/windows/win32/api/winuser/nf-winuser-removepropa)       | Quita una entrada de la lista de propiedades de la ventana especificada. La cadena de caracteres especificada identifica la entrada que se va a quitar.<br/>                                                                                                                                                                                                                    |
| [**SetProp**](/windows/win32/api/winuser/nf-winuser-setpropa)             | Agrega una nueva entrada o cambia una entrada existente en la lista de propiedades de la ventana especificada. La función agrega una nueva entrada a la lista si la cadena de caracteres especificada no existe aún en la lista. La nueva entrada contiene la cadena y el identificador. De lo contrario, la función reemplaza el identificador actual de la cadena por el identificador especificado. <br/> |



 

 

 
