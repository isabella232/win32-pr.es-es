---
description: Cuando una aplicación habilitada para SOAP se ha exportado desde un servidor en modo proxy, los clientes que la importan pueden tener acceso automáticamente a los métodos de los componentes que contiene, de forma remota, como servicios web ofrecidos por el servidor en modo de objeto activado en el cliente (CAO). Esto le permite implementar fácilmente la funcionalidad de una aplicación COM+ a través de una red como servicio Web XML.
ms.assetid: 7f4783f7-4f53-4f0b-bb64-ae7903097d6c
title: Importar una aplicación SOAP-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d9faca91a726caea765d4b2ca227ddba0ff3a2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539303"
---
# <a name="importing-a-soap-enabled-application"></a>Importar una aplicación SOAP-Enabled

Cuando una aplicación habilitada para SOAP se ha [exportado](exporting-a-soap-enabled-application.md) desde un servidor en modo proxy, los clientes que la importan pueden tener acceso automáticamente a los métodos de los componentes que contiene, de forma remota, como servicios web ofrecidos por el servidor en modo de objeto activado en el cliente (CaO). Esto le permite implementar fácilmente la funcionalidad de una aplicación COM+ a través de una red como servicio Web XML.

Cuando se utilizan en el cliente los componentes de una aplicación importada de esta manera, no se ejecutan en el cliente, sino que se accede a ellos de forma remota mediante el servicio Web XML proporcionado por el servidor desde el que se exportó la aplicación. Para obtener información detallada sobre el uso de los componentes de una aplicación importada de esta manera, vea [obtener acceso a los servicios Web XML en el modo de Cao](accessing-xml-web-services-in-cao-mode.md).

## <a name="component-services-administrative-tool"></a>Herramienta administrativa Servicios de componentes

Para importar una aplicación habilitada para SOAP en un cliente de, siga estos pasos:

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, en **servicios de componentes**, abra la carpeta asociada al equipo cliente en el que desea instalar la aplicación.

2.  Haga clic con el botón secundario en la carpeta **aplicaciones com+** del cliente y elija **nuevo**. Aparece el **Asistente para instalación de aplicaciones com+** .

3.  En el **Asistente para instalación de aplicaciones com+**, haga clic en **instalar aplicaciones creadas previamente**.

4.  Examine la red para buscar o especificar la ruta de acceso de red del archivo MSI en el servidor desde el que desea instalar la aplicación.

## <a name="visual-basic"></a>Visual Basic

No corresponde.

## <a name="cc"></a>C/C++

No corresponde.

## <a name="remarks"></a>Observaciones

Los componentes COM se identifican mediante un GUID, que cambia si se vuelven a compilar los componentes. Si se vuelve a compilar un componente COM configurado que se expone como un servicio Web XML, las aplicaciones cliente que lo utilicen se interrumpirán. Por lo tanto, cuando se vuelve a compilar un componente que se expone como un servicio Web XML, los clientes deben volver a importar las aplicaciones que usan el componente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción al servicio SOAP de COM+](com--soap-service-overview.md)
</dt> <dt>

[Crear servicios Web XML](creating-xml-web-services.md)
</dt> <dt>

[Exportar una aplicación SOAP-Enabled](exporting-a-soap-enabled-application.md)
</dt> </dl>

 

 



