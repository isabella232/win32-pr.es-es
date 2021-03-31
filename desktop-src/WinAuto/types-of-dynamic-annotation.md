---
title: Tipos de anotación dinámica
description: Hay tres tipos de anotación dinámica admitidos en Microsoft Active Accessibility anotación directa, anotación asignada por valores y anotación de servidor. Cada tipo ofrece ventajas específicas, por lo que es importante comprender las diferencias.
ms.assetid: 113fea65-982e-4291-9d60-bbb57282f3f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0453d3b5d05e2713d1a57fb0f475d4ec2a481b02
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903480"
---
# <a name="types-of-dynamic-annotation"></a>Tipos de anotación dinámica

En Microsoft Active Accessibility se admiten tres tipos de anotación dinámica: *anotación directa*, *anotación asignada por valor* y *anotación de servidor*. Cada tipo ofrece ventajas específicas, por lo que es importante comprender las diferencias.

## <a name="direct-annotation"></a>Anotación directa

La anotación directa es la forma más sencilla de una anotación dinámica. Es más aplicable a los elementos accesibles cuya propiedad anotada no depende del estado del control y no requiere la compatibilidad adicional proporcionada por la anotación asignada por valores y la anotación del servidor. La anotación directa se usa para invalidar el valor de una o varias propiedades de Microsoft Active Accessibility de un elemento accesible, y para invalidar o agregar una propiedad de automatización de la interfaz de usuario de Microsoft al control. Todas las anotaciones realizadas en una propiedad de Microsoft Active Accessibility se reflejan en la traducción de automatización de la interfaz de usuario, así como en el proxy de automatización de Active Accessibility a la interfaz de usuario de Microsoft. Para obtener más información, vea [anotación directa](direct-annotation.md).

## <a name="value-map-annotation"></a>Anotación de asignación de valores

Además de anotar directamente las propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , suele ser necesario convertir un valor específico del control en una cadena que un usuario final pueda entender. Un ejemplo es el control deslizante de resolución de pantalla en la pestaña **configuración** de la ventana **propiedades de pantalla** (en el **Panel de control**). Aunque cada posición del control deslizante corresponde a una resolución diferente (por ejemplo, 640 x 480, 1024 x 768), el control no tiene conocimiento de esta relación y no puede transmitir esta información a Microsoft Active Accessibility.

La anotación con valores asignados facilita esta tarea. Con esta forma de anotación, puede especificar cadenas para los valores del control deslizante y especificar roles, Estados y descripciones para los iconos de las vistas de lista y de árbol. Para obtener más información, vea [anotación de asignación de valores](value-map-annotation.md).

## <a name="server-annotation"></a>Anotación de servidor

La anotación del servidor permite a los desarrolladores registrar un objeto de devolución de llamada en las solicitudes de cliente de servicio para la propiedad anotada de un elemento. Este objeto de devolución de llamada debe implementar la interfaz [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver) y registrarse en Microsoft Active Accessibility Annotation Services. Una vez registrado, se le pedirá que ponga servicio a todas las solicitudes de cliente para el valor de propiedad de ese elemento accesible.

Una característica especialmente útil de la anotación de servidor es que un servidor se puede registrar una vez para controlar las solicitudes de un contenedor y todos sus elementos secundarios. Por lo tanto, por ejemplo, un solo servidor puede configurarse una vez para controlar las solicitudes de todos los elementos es un cuadro de lista. Para obtener más información, vea [anotación del servidor](server-annotation.md).

 

 




