---
description: Cualquier aplicación COM+ se puede exponer como un servicio Web XML.
ms.assetid: 03c3d5a7-eb98-4916-b6ef-ef6aac86c574
title: Crear servicios Web XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10652531e64fec38f2ac221184cb589a27b343d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705303"
---
# <a name="creating-xml-web-services"></a>Crear servicios Web XML

Cualquier aplicación COM+ se puede exponer como un servicio Web XML. A continuación, se puede llamar a los métodos de las interfaces predeterminadas de los componentes configurados de las aplicaciones (componentes en el catálogo COM+ de servidores) de forma remota. Puede usar la herramienta administrativa Servicios de componentes para crear un directorio raíz virtual de IIS desde el que se puede llamar a los métodos de componente mediante SOAP.

> [!Note]  
> El .NET Framework debe estar instalado en el equipo para poder exponer una aplicación COM+ como un servicio Web XML.

 

**Para exponer una aplicación COM+ como un servicio Web XML**

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, en **servicios de componentes**, abra la carpeta **aplicaciones com+** asociada con el equipo que desea administrar.

2.  Haga clic con el botón secundario en la aplicación que desea exponer como un servicio Web XML y elija **propiedades**.

3.  Haga clic en la pestaña **activación** en el cuadro de diálogo Propiedades.

4.  Active la casilla **usar SOAP** .

5.  En el cuadro de texto **vroot de SOAP** , escriba el nombre del directorio raíz virtual de IIS desde el que se puede tener acceso a los métodos de los componentes de forma remota. Tenga en cuenta que una VRoot de SOAP no puede ser un subdirectorio de otro directorio VRoot de SOAP.

6.  Haga clic en **OK**.

    Si especifica el directorio raíz virtual de IIS como *vroot* y si el nombre de dominio completo de los servidores es *ServerName*, la dirección URL donde se expone el componente como un servicio Web XML es https://*ServerName* / *vroot*/.

    El directorio correspondiente en el sistema de archivos es \\ Windows \\ system32 \\ com \\ SoapVRoots \\ *vroot* \\ ; COM+ coloca en ella varios archivos de configuración y programas de ASP.NET. Para un servicio Web XML con mucha carga, es posible que desee ajustar los parámetros almacenados en el archivo web.config. Para obtener información acerca de este archivo, consulte la documentación de IIS.

    La configuración de seguridad predeterminada para una aplicación COM+ expuesta como un servicio Web XML varía en función de la versión de la .NET Framework esté instalada. Si está instalada la versión 1,0, los servicios Web XML no son seguros de forma predeterminada; todas las llamadas se aceptan y no se utiliza ningún cifrado. Si está instalada la versión 1,1 o posterior, los servicios Web XML son seguros de forma predeterminada. los llamadores deben autenticarse y se requiere cifrado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Obtener acceso a los servicios Web XML en el modo de CAO](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[Obtener acceso a los servicios Web XML en modo WKO](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[Introducción al servicio SOAP de COM+](com--soap-service-overview.md)
</dt> <dt>

[Proteger los servicios Web XML](securing-xml-web-services.md)
</dt> </dl>

 

 



