---
title: Tipos de anotación dinámica
description: Hay tres tipos de anotaciones dinámicas admitidas en Microsoft Active Accessibility anotación directa, anotación asignada por valor y anotación de servidor. Cada tipo ofrece ventajas específicas, por lo que es importante comprender las diferencias.
ms.assetid: 113fea65-982e-4291-9d60-bbb57282f3f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0453d3b5d05e2713d1a57fb0f475d4ec2a481b02
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070595"
---
# <a name="types-of-dynamic-annotation"></a>Tipos de anotación dinámica

Hay tres tipos de anotaciones dinámicas admitidas en *Microsoft Active Accessibility:* anotación *directa,* anotación asignada por valor y *anotación de servidor*. Cada tipo ofrece ventajas específicas, por lo que es importante comprender las diferencias.

## <a name="direct-annotation"></a>Anotación directa

La anotación directa es la forma más sencilla de anotación dinámica. Es más aplicable para los elementos accesibles cuya propiedad anotada no depende del estado del control y no requiere la compatibilidad adicional proporcionada por la anotación asignada por valor y la anotación del servidor. La anotación directa se usa para invalidar el valor de una o varias propiedades Microsoft Active Accessibility de un elemento accesible y para invalidar o agregar una propiedad de Microsoft Automatización de la interfaz de usuario al control. Todas las anotaciones realizadas en una Microsoft Active Accessibility propiedad se reflejan en la traducción de Automatización de la interfaz de usuario, así como en el proxy Microsoft Active Accessibility a Automatización de la interfaz de usuario proxy. Para obtener más información, vea [Anotación directa.](direct-annotation.md)

## <a name="value-map-annotation"></a>Anotación de mapa de valores

Además de anotar directamente las propiedades [**IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) a menudo es necesario convertir un valor específico del control en una cadena que un usuario final pueda entender. Un ejemplo es el control deslizante de resolución de pantalla en **la Configuración** de la Propiedades de pantalla **(desde** **Panel de control**). Aunque cada posición del control deslizante corresponde a una resolución diferente (por ejemplo, 640 x 480, 1024 x 768), el control no tiene conocimiento de esta relación y no puede transmitir esta información a Microsoft Active Accessibility.

La anotación asignada a valores facilita esta tarea. Con esta forma de anotación, puede especificar cadenas para los valores de control deslizante y especificar roles, estados y descripciones para los iconos de las vistas de lista y árbol. Para obtener más información, vea [Anotación de mapa de valores](value-map-annotation.md).

## <a name="server-annotation"></a>Anotación del servidor

La anotación de servidor permite a los desarrolladores registrar un objeto de devolución de llamada para las solicitudes de cliente de servicio de la propiedad anotada de un elemento. Este objeto de devolución de llamada debe implementar [**la interfaz IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver) y registrarse con Microsoft Active Accessibility de anotación. Una vez registrado, se le pedirá que abate todas las solicitudes de cliente para el valor de propiedad de ese elemento accesible.

Una característica especialmente útil de la anotación del servidor es que un servidor se puede registrar una vez para controlar las solicitudes de un contenedor y todos sus elementos secundarios. Por ejemplo, un único servidor se puede configurar una vez para controlar las solicitudes de todos los elementos es un cuadro de lista. Para obtener más información, vea [Anotación de servidor](server-annotation.md).

 

 




