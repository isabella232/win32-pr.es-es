---
title: Categorías de componentes y cómo funcionan
description: Categorías de componentes y cómo funcionan
ms.assetid: efbf4a25-3c73-4d09-a172-6676c6d6501b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddfd5580e12ce3d4a44ca251142e29f6eea8f9f5823cf18999f876a4ef732d09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737022"
---
# <a name="component-categories-and-how-they-work"></a>Categorías de componentes y cómo funcionan

Las categorías de componentes identifican las áreas de funcionalidad que un componente de software admite y requiere, y se usa una entrada del Registro para cada categoría o área de funcionalidad identificada. Cada categoría de componente se identifica mediante un identificador único global (GUID), cuando se instala un control, se registra como un control en el registro del sistema mediante el identificador de categoría de componente para el control, vea [Registro](self-registration-for-controls.md)automático para controles . Dentro del registro automático de controles, también registrará las categorías de componentes que implementa y las categorías de componentes que requiere que admita un contenedor para hospedar correctamente el control.

Cuando un contenedor de controles ofrece controles al usuario para insertar, solo permite al usuario seleccionar y crear instancias de esos controles que podrán funcionar correctamente en ese entorno. Por ejemplo, si el contenedor de controles no admite el enlace de datos, el contenedor no permitirá al usuario seleccionar y crear instancias de esos controles que tienen una entrada en el Registro que significa que requieren la categoría de componente de enlace de datos. Hay disponible un cuadro de diálogo común para la inserción de controles y las API para controlar las entradas del Registro.

Las categorías de componentes no son acumulativas ni excluyentes, un control puede requerir cualquier combinación de categorías de componentes para funcionar. Se puede esperar que un control que no tenga entradas necesarias para las categorías de componentes pueda funcionar en cualquier contenedor de controles y no requiera ninguna funcionalidad específica de un contenedor de controles para funcionar.

Las siguientes categorías de componentes se identifican aquí, siempre que sea necesario que haya especificaciones más detalladas de las categorías disponibles.

-   [**Contención del control ISimpleFrameSite.**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)
-   Enlace de datos simple a través [**de la interfaz IPropertyNotifySink.**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink)
-   Enlace de datos avanzado (compatible con las interfaces de enlace de datos adicionales de VB4.0).
-   Visual Basic interfaces privadas: [**IVBFormat**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbformat), [**IVBGetControl**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbgetcontrol)
-   Controles con conexión a Internet.
-   Controles sin ventanas.

No se trata de una lista definitiva de categorías; Es probable que se definan más categorías en el futuro a medida que se identifiquen nuevos requisitos. Microsoft dispone de una lista actualizada de categorías de componentes. esta lista refleja las categorías de componentes identificadas por Microsoft y otras que sobre qué proveedores han informado a Microsoft.

Es importante recordar que los controles deben intentar trabajar en tantos entornos como sea posible. Si es posible, el control debe degradar su funcionalidad cuando se coloca en un contenedor que no admite determinadas interfaces. El propósito de las categorías de componentes es evitar una situación en la que el control se coloca en un entorno que no es adecuado y el control no puede lograr la tarea deseada. Por lo general, un control debe degradarse correctamente cuando las interfaces no están presentes, un control puede optar por aconsejar al usuario con un cuadro de mensaje que alguna funcionalidad no está disponible o documentar claramente la funcionalidad necesaria de un contenedor de control para un rendimiento óptimo.

Tenga en cuenta que los controles y contenedores anteriores no usan categorías de componentes y, en su lugar, se basan en la palabra clave de control que está presente en el control en el Registro. Para que los controles de contenedores anteriores puedan desear registrar la palabra clave de control en el Registro, los desarrolladores de controles deben comprobar que el control se puede hospedar correctamente en dichos contenedores antes de hacerlo. Los contenedores que usan categorías de componentes pueden usarlos correctamente para hospedar controles más antiguos a medida que el archivo DLL de categoría de componentes controla la asignación; existe una categoría independiente para los controles anteriores CATID ControlV1 para que un contenedor pueda excluirlos opcionalmente si es \_ necesario.

Como las categorías de componentes se identifican mediante GUID, es posible que los contenedores que ofrecen una funcionalidad específica tengan sus propios identificadores de categoría, generados mediante una herramienta de generación de GUID. Sin embargo, esto puede perjudicar la ventaja de interoperabilidad de los controles y contenedores, por lo que es preferible usar siempre que sea posible las categorías de componentes existentes. Se recomienda a los proveedores que consulten juntos al definir nuevas categorías de componentes para asegurarse de que cumplen los requisitos comunes de Marketplace y siguen el alma de interoperabilidad de ActiveX controles.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Categorías del componente](component-categories.md)
</dt> </dl>

 

 




