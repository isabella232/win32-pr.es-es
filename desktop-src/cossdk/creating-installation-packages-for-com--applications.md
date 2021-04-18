---
description: Crear paquetes de instalación para aplicaciones COM+
ms.assetid: 3ef7b280-b521-4cd2-9906-013c9dfe16ab
title: Crear paquetes de instalación para aplicaciones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ec34852ab405d965fa1ad8f8fb5892616d1347
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705304"
---
# <a name="creating-installation-packages-for-com-applications"></a>Crear paquetes de instalación para aplicaciones COM+

Puede usar la herramienta administrativa Servicios de componentes o la biblioteca de administración de COM+ para crear paquetes de instalación para aplicaciones COM+ y proxies de aplicación.

COM+ genera paquetes de instalación de Windows Installer, que en un único archivo contiene todos los componentes necesarios para instalar una aplicación COM+ en otro equipo.

Al exportar una aplicación COM+, la herramienta administrativa Servicios de componentes determina el conjunto de clases, componentes y atributos de la aplicación, así como los atributos de nivel de aplicación. A partir de esta información, la herramienta administrativa Servicios de componentes genera un único archivo. msi, que contiene lo siguiente:

-   Windows Installer tablas con información de registro COM (consulte la documentación de Windows Installer para obtener más información).
-   Un archivo. APL que contiene los atributos de la aplicación. (Este es un archivo interno; el formato de este archivo no está documentado).
-   Dll y bibliotecas de tipos que describen las interfaces implementadas por las clases de la aplicación COM+.

Además del archivo. msi, la herramienta administrativa Servicios de componentes genera un archivo contenedor (. cab). Este archivo encapsula el archivo. msi, lo que permite al desarrollador implementar la aplicación COM+ a través de Microsoft Internet Explorer.

> [!Note]  
> Al exportar una aplicación COM+, la herramienta administrativa Servicios de componentes solo empaqueta las partes estándar de COM+ de la aplicación. No empaqueta, por ejemplo, los archivos DLL o de datos dependientes. Los archivos DLL dependientes deben instalarse primero en un equipo antes de instalar la aplicación COM+. Como alternativa, puede usar la herramienta de creación de Windows Installer para agregar estos archivos dependientes al archivo. msi generado por la herramienta administrativa Servicios de componentes. (Consulte la documentación de Windows Installer para obtener más información).

 

## <a name="installing-com-applications-on-other-computers"></a>Instalación de aplicaciones COM+ en otros equipos

El archivo Windows Installer (. msi) generado por la herramienta administrativa Servicios de componentes se puede usar para instalar la aplicación COM+ en otro equipo. El archivo. msi que contiene una aplicación COM+ solo se puede instalar en equipos que admitan servicios COM+. Para obtener procedimientos detallados sobre la implementación de aplicaciones COM+, vea "instalar aplicaciones COM+" en la ayuda de administración de servicios de componentes.

A menos que se modifique el archivo. msi mediante una herramienta de creación de Windows Installer, las aplicaciones COM+ instaladas mediante el Windows Installer aparecen en el panel de control Agregar o quitar programas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Implementación de servidores proxy de aplicación](deploying-application-proxies.md)
</dt> <dt>

[El catálogo de COM+](the-com--catalog.md)
</dt> </dl>

 

 



