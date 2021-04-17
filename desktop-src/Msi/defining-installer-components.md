---
description: A continuación se describe cómo organizar la aplicación en componentes de Windows Installer.
ms.assetid: 981a3def-1e59-4703-ad97-c8cd5431375d
title: Definir componentes del instalador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ade4476fa1bf54a0ab4f64d0d43d72265ac1eb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652835"
---
# <a name="defining-installer-components"></a>Definir componentes del instalador

A continuación se describe cómo organizar la aplicación en componentes de Windows Installer.

**Para organizar una aplicación en componentes**

1.  Comience por obtener un directorio y un árbol de archivos para todos los archivos y otros recursos utilizados en la aplicación.
2.  Identifique los archivos, las claves del registro, los accesos directos u otros recursos que se compartan entre aplicaciones y que puedan proporcionar los componentes existentes disponibles como [módulos de combinación](merge-modules.md). No debe incluir ninguno de estos recursos en los componentes que cree. En su lugar, Obtenga estos componentes combinando los módulos de combinación en el paquete de instalación. En los pasos siguientes se describe cómo organizar los recursos restantes de la aplicación en componentes de.
3.  Defina un nuevo componente para cada archivo. exe,. dll y. ocx. Designe estos archivos como los archivos de ruta de acceso de la clave de sus componentes. Asigne a cada componente un GUID de código de componente.
4.  Defina un nuevo componente para cada archivo de ayuda. hlp o. chm. Designe estos archivos como los archivos de ruta de acceso de la clave de sus componentes. Agregue los archivos. CNT o. Chi a los componentes que contienen sus archivos. HLP y. chm asociados. Asigne a cada componente un GUID de código de componente.
5.  Defina un nuevo componente para cada archivo que sirva como destino de un acceso directo. Designe estos archivos como los archivos de ruta de acceso de la clave de sus componentes. Asigne a cada componente un GUID de código de componente.
6.  Agrupe todos los recursos restantes en carpetas. Todos los recursos de cada carpeta deben distribuirse juntos. Si existe la posibilidad de que un par de recursos pueda distribuirse por separado en el futuro, colóquelos en carpetas independientes. Defina un componente nuevo para cada carpeta. Intente mantener el número total de componentes bajo para mejorar el rendimiento. Divida la aplicación en muchos componentes cuando sea necesario que el instalador Compruebe la validez de la instalación exhaustivamente. Designe cualquier archivo del componente como el archivo de ruta de acceso de la clave. Asigne a cada componente un GUID de código de componente.
7.  Agregue las claves del registro a los componentes. Cualquier clave del registro que apunte a un archivo debe incluirse en el componente de ese archivo. Otras claves del registro deben agruparse lógicamente con los archivos que las necesiten.

 

 



