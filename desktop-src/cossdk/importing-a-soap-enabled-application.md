---
description: Cuando una aplicación habilitada para SOAP se ha exportado desde un servidor en modo proxy, los clientes que la importan pueden acceder automáticamente a los métodos de los componentes que contiene, de forma remota, como servicios web ofrecidos por el servidor en modo de objeto activado por el cliente (VMM). Esto le permite implementar fácilmente la funcionalidad de una aplicación COM+ en una red como un servicio web XML.
ms.assetid: 7f4783f7-4f53-4f0b-bb64-ae7903097d6c
title: Importación de una SOAP-Enabled aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a41a60c2b5ca69197582a684920e9e935f28631779bc632810049f1a7d03945
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858925"
---
# <a name="importing-a-soap-enabled-application"></a>Importación de una SOAP-Enabled aplicación

Cuando una aplicación habilitada [](exporting-a-soap-enabled-application.md) para SOAP se ha exportado desde un servidor en modo proxy, los clientes que la importan pueden acceder automáticamente a los métodos de los componentes que contiene, de forma remota, como servicios web ofrecidos por el servidor en modo de objeto activado por el cliente (VMM). Esto le permite implementar fácilmente la funcionalidad de una aplicación COM+ en una red como un servicio web XML.

Cuando los componentes de una aplicación importada de esta manera se usan en el cliente, no se ejecutan en el cliente, sino que se accede a ellos de forma remota mediante el servicio web XML proporcionado por el servidor desde el que se exportó la aplicación. Para obtener más información sobre el uso de los componentes de una aplicación importada de esta manera, vea Acceso a [servicios Web XML en el modo DESEDI](accessing-xml-web-services-in-cao-mode.md).

## <a name="component-services-administrative-tool"></a>Herramienta administrativa de servicios de componentes

Para importar una aplicación habilitada para SOAP en un cliente, siga estos pasos:

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, en Servicios de componentes **,** abra la carpeta asociada al equipo cliente en el que desea instalar la aplicación.

2.  Haga clic con el botón derecho en la carpeta **Aplicaciones COM+ del** cliente y, a continuación, **elija Nuevo**. Aparece **el Asistente para instalación de aplicaciones COM+.**

3.  En el Asistente **para instalación de aplicaciones COM+**, haga clic en Instalar aplicaciones pre-creadas. 

4.  Examine la red para buscar o especificar la ruta de acceso de red del archivo MSI en el servidor desde el que desea instalar la aplicación.

## <a name="visual-basic"></a>Visual Basic

No corresponde.

## <a name="cc"></a>C/C++

No corresponde.

## <a name="remarks"></a>Comentarios

Los componentes COM se identifican mediante un GUID, que cambia si se vuelve a compilar los componentes. Si se vuelve a compilar un componente COM configurado que se expone como un servicio web XML, se interrumpirán las aplicaciones cliente que lo usan. Por lo tanto, cuando se vuelve a compilar un componente que se expone como un servicio web XML, los clientes deben volver a importar las aplicaciones que usan el componente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre el servicio SOAP de COM+](com--soap-service-overview.md)
</dt> <dt>

[Creación de servicios web XML](creating-xml-web-services.md)
</dt> <dt>

[Exportación de una SOAP-Enabled aplicación](exporting-a-soap-enabled-application.md)
</dt> </dl>

 

 



