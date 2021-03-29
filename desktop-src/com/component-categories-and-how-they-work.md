---
title: Categorías de componentes y cómo funcionan
description: Categorías de componentes y cómo funcionan
ms.assetid: efbf4a25-3c73-4d09-a172-6676c6d6501b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf8065584ae2dc83e470428b7345eb2d9321d32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993922"
---
# <a name="component-categories-and-how-they-work"></a>Categorías de componentes y cómo funcionan

Las categorías de componentes identifican las áreas de funcionalidad que un componente de software admite y requiere, se usa una entrada del registro para cada categoría o el área de funcionalidad identificada. Cada categoría de componente se identifica mediante un identificador único global (GUID), cuando se instala un control, se registra a sí mismo como un control en el registro del sistema mediante el identificador de categoría de componente para el control. consulte [autoregistro para controles](self-registration-for-controls.md). Dentro de los controles de registro propio, también se registran las categorías de componentes que implementa y las categorías de componentes que requiere un contenedor para hospedar correctamente el control.

Cuando un contenedor de control está ofreciendo controles al usuario que se va a insertar, solo permite al usuario seleccionar y crear instancias de esos controles que podrán funcionar de forma adecuada en ese entorno. Por ejemplo, si el contenedor de controles no admite el enlace de enlaces, el contenedor no permitirá al usuario seleccionar y crear instancias de los controles que tengan una entrada en el registro, lo que significa que requieren la categoría del componente de enlace de los enlaces. Hay disponible un cuadro de diálogo común para la inserción de controles y las API para controlar las entradas del registro.

Las categorías de componentes no son acumulativas ni exclusivas, un control puede requerir que una combinación de categorías de componentes funcione. Se puede esperar que un control que no tenga entradas necesarias para las categorías de componentes sea capaz de funcionar en cualquier contenedor de controles y no requiera una funcionalidad específica de un contenedor de control para que funcione.

Las siguientes categorías de componentes se identifican aquí, donde es posible que estén disponibles especificaciones más detalladas de las categorías.

-   Contención de control [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) .
-   Enlace de los enlaces a través de la interfaz [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) .
-   Enlace de DataBindings avanzado (compatible con las interfaces de enlace de enlaces adicionales de VB 4.0).
-   Interfaces privadas de Visual Basic: [**IVBFormat**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbformat), [**IVBGetControl**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbgetcontrol)
-   Controles compatibles con Internet.
-   Controles sin ventana.

Esta no es una lista definitiva de categorías; es probable que se definan más categorías en el futuro a medida que se identifiquen nuevos requisitos. La lista actualizada de categorías de componentes está disponible en Microsoft; en esta lista se muestran las categorías de componentes que Microsoft ha identificado y las demás personas en las que los proveedores han informado a Microsoft.

Es importante recordar que los controles deben intentar trabajar en tantos entornos como sea posible. Si es posible, el control debe degradar su funcionalidad cuando se coloca en un contenedor que no admite determinadas interfaces. El propósito de las categorías de componentes es evitar una situación en la que el control se coloca en un entorno que no es adecuado y el control no puede lograr la tarea deseada. Normalmente, un control debe degradarse correctamente cuando no haya interfaces presentes, un control puede elegir informar al usuario con un cuadro de mensaje que indica que alguna funcionalidad no está disponible o documenta claramente la funcionalidad requerida por un contenedor de control para obtener un rendimiento óptimo.

Tenga en cuenta que los controles y contenedores antiguos no hacen uso de categorías de componentes y, en su lugar, dependen de que la palabra clave control esté presente en el control del registro. Para que los controles de contenedores más antiguos lo reconozcan, es posible que deseen registrar la palabra clave de control en el registro, los desarrolladores de controles deben comprobar que el control se puede hospedar correctamente en dichos contenedores antes de hacerlo. Los contenedores que usan categorías de componentes pueden utilizarlos correctamente para hospedar controles anteriores, ya que la categoría de componentes DLL controla la asignación, existe una categoría independiente para los controles anteriores CATId \_ ControlV1, de modo que un contenedor puede excluirlos opcionalmente si es necesario.

Dado que las categorías de componentes se identifican mediante GUID, es posible que los contenedores que ofrecen una funcionalidad específica concreta tengan sus propios identificadores de categoría, que se generan mediante una herramienta de generación de GUID. Sin embargo, esto puede afectar a la ventaja de la interoperabilidad de los controles y contenedores, por lo que es preferible que siempre que se use cualquier categoría de componentes existente. Se recomienda a los proveedores que se comuniquen al definir nuevas categorías de componentes para asegurarse de que cumplen los requisitos comunes de Marketplace y que siguen el espíritu de interoperabilidad de los controles ActiveX.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Categorías del componente](component-categories.md)
</dt> </dl>

 

 




