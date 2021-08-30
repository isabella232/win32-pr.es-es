---
description: Crear paquetes de instalación para aplicaciones COM+
ms.assetid: 3ef7b280-b521-4cd2-9906-013c9dfe16ab
title: Crear paquetes de instalación para aplicaciones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef766c222fc887742f060fa786ac6308e3d7569ca572fde216cb8055ee67a29c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991165"
---
# <a name="creating-installation-packages-for-com-applications"></a>Crear paquetes de instalación para aplicaciones COM+

Puede usar la herramienta administrativa Servicios de componentes o la Biblioteca de administración de COM+ para crear paquetes de instalación para aplicaciones COM+ y servidores proxy de aplicación.

COM+ genera Windows de instalación del instalador, que en un solo archivo contienen todas las piezas necesarias para instalar una aplicación COM+ en otro equipo.

Al exportar una aplicación COM+, la herramienta administrativa Servicios de componentes determina el conjunto de clases, componentes y sus atributos de la aplicación, así como los atributos de nivel de aplicación. A partir de esta información, la herramienta administrativa Servicios de componentes genera un único .msi, que contiene lo siguiente:

-   Windows Tablas del instalador con información de registro COM (consulte la documentación Windows Installer para obtener más información).
-   Un archivo .apl que contiene los atributos de la aplicación. (Se trata de un archivo interno; el formato de este archivo no está documentado).
-   Archivos DLL y bibliotecas de tipos que describen las interfaces implementadas por las clases de la aplicación COM+.

Además del archivo .msi, la herramienta administrativa Servicios de componentes genera un archivo de archivador (.cab). Este archivo encapsula el .msi, lo que permite al desarrollador implementar la aplicación COM+ a través de Microsoft Internet Explorer.

> [!Note]  
> Al exportar una aplicación COM+, la herramienta administrativa Servicios de componentes empaqueta solo las partes com+ estándar de la aplicación. No empaqueta, por ejemplo, ningún archivo DLL o de datos dependiente. Los archivos DLL dependientes deben instalarse primero en un equipo antes de instalar la aplicación COM+. Como alternativa, puede usar la herramienta de creación Windows Installer para agregar estos archivos dependientes al archivo .msi generado por la herramienta administrativa Servicios de componentes. (Consulte la documentación Windows Installer para obtener más información).

 

## <a name="installing-com-applications-on-other-computers"></a>Instalación de aplicaciones COM+ en otros equipos

El Windows instalador (.msi) generado por la herramienta administrativa Servicios de componentes se puede usar para instalar la aplicación COM+ en otro equipo. El .msi que contiene una aplicación COM+ solo se puede instalar en equipos que admiten servicios COM+. Para obtener procedimientos detallados sobre la implementación de aplicaciones COM+, vea "Instalación de aplicaciones COM+" en la Ayuda de administración de servicios de componentes.

A menos que el archivo .msi se modifique mediante una herramienta de creación del instalador de Windows, las aplicaciones COM+ instaladas mediante el instalador de Windows aparecen en el panel de control Agregar o quitar programas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Implementación de servidores proxy de aplicación](deploying-application-proxies.md)
</dt> <dt>

[El catálogo de COM+](the-com--catalog.md)
</dt> </dl>

 

 



