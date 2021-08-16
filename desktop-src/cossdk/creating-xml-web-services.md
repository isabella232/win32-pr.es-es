---
description: Cualquier aplicación COM+ se puede exponer como un servicio web XML.
ms.assetid: 03c3d5a7-eb98-4916-b6ef-ef6aac86c574
title: Creación de servicios web XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12dbc5ee08d9300d52b538648ba520b16a60a9e3769242c252eaa40d518a3ea1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307342"
---
# <a name="creating-xml-web-services"></a>Creación de servicios web XML

Cualquier aplicación COM+ se puede exponer como un servicio web XML. A continuación, se puede llamar a los métodos de las interfaces predeterminadas de los componentes configurados por las aplicaciones (componentes del catálogo COM+ de servidores) de forma remota. Puede usar la herramienta administrativa Servicios de componentes para crear un directorio raíz virtual de IIS desde el que se puede llamar a los métodos de componente mediante SOAP.

> [!Note]  
> El .NET Framework debe instalarse en el equipo para exponer una aplicación COM+ como un servicio web XML.

 

**Para exponer una aplicación COM+ como un servicio web XML**

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, en Servicios de componentes **,** abra la carpeta **Aplicaciones COM+** asociada al equipo que desea administrar.

2.  Haga clic con el botón derecho en la aplicación que desea exponer como servicio web XML y elija **Propiedades.**

3.  Haga clic en **la pestaña** Activación en el cuadro de diálogo de propiedades.

4.  Active la **casilla Usa SOAP.**

5.  En el **cuadro de texto SOAP VRoot,** escriba el nombre del directorio raíz virtual de IIS desde el que se puede acceder a los métodos de componentes de forma remota. Tenga en cuenta que un VRoot de SOAP no puede ser un subdirectorio de otro directorio VRoot de SOAP.

6.  Haga clic en **Aceptar**.

    Si especifica el directorio raíz virtual de IIS como *vroot* y si el nombre de dominio completo de los servidores es *servername*, la dirección URL en la que el componente se expone como un servicio web XML es https://*nombre* de servidor / *vroot*/.

    El directorio correspondiente del sistema de archivos \\ es windows \\ system32 \\ com \\ SoapVRoots \\ *vroot* \\ ; COM+ coloca varios archivos de configuración y ASP.NET programas allí. Para un servicio web XML con mucha carga, puede ajustar los parámetros almacenados en el archivo web.config. Para obtener información sobre este archivo, consulte la documentación de IIS.

    La configuración de seguridad predeterminada para una aplicación COM+ expuesta como un servicio web XML difiere en función de la versión del .NET Framework está instalada. Si está instalada la versión 1.0, los servicios web XML no son seguros de forma predeterminada; se aceptan todas las llamadas y no se usa cifrado. Si está instalada la versión 1.1 o posterior, los servicios web XML son seguros de forma predeterminada; Los autores de la llamada deben autenticarse y se requiere cifrado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acceso a servicios web XML en modo DESA](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[Acceso a servicios web XML en modo WKO](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[Información general sobre el servicio SOAP de COM+](com--soap-service-overview.md)
</dt> <dt>

[Protección de servicios Web XML](securing-xml-web-services.md)
</dt> </dl>

 

 



