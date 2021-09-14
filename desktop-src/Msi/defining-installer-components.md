---
description: A continuación se describe cómo organizar la aplicación en Windows installer.
ms.assetid: 981a3def-1e59-4703-ad97-c8cd5431375d
title: Definir componentes del instalador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ade4476fa1bf54a0ab4f64d0d43d72265ac1eb6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158610"
---
# <a name="defining-installer-components"></a>Definir componentes del instalador

A continuación se describe cómo organizar la aplicación en Windows installer.

**Para organizar una aplicación en componentes**

1.  Comience por obtener un directorio y un árbol de archivos para todos los archivos y otros recursos usados en la aplicación.
2.  Identifique los archivos, las claves del Registro, los accesos directos u otros recursos que se comparten entre aplicaciones y que pueden proporcionar los componentes existentes disponibles como módulos [de combinación.](merge-modules.md) No debe incluir ninguno de estos recursos en los componentes que cree. En su lugar, obtenga estos componentes combinando los módulos de combinación en el paquete de instalación. En los pasos siguientes se describe cómo organizar los recursos restantes de la aplicación en componentes.
3.  Defina un nuevo componente para cada archivo .exe, .dll y .ocx. Designe estos archivos como los archivos de ruta de acceso clave de sus componentes. Asigne a cada componente un GUID de código de componente.
4.  Defina un nuevo componente para cada archivo de ayuda .hlp o .chm. Designe estos archivos como los archivos de ruta de acceso clave de sus componentes. Agregue los archivos .cnt o .chi a los componentes que mantienen sus archivos .hlp y .chm asociados. Asigne a cada componente un GUID de código de componente.
5.  Defina un nuevo componente para cada archivo que actúa como destino de un acceso directo. Designe estos archivos como los archivos de ruta de acceso clave de sus componentes. Asigne a cada componente un GUID de código de componente.
6.  Agrupa todos los recursos restantes en carpetas. Todos los recursos de cada carpeta deben enviarse juntos. Si existe la posibilidad de que un par de recursos se puedan enviar por separado en el futuro, coloque estos recursos en carpetas independientes. Defina un nuevo componente para cada carpeta. Intente mantener bajo el número total de componentes para mejorar el rendimiento. Divida la aplicación en muchos componentes cuando sea necesario que el instalador compruebe exhaustivamente la validez de la instalación. Designe cualquier archivo del componente como archivo de ruta de acceso de clave. Asigne a cada componente un GUID de código de componente.
7.  Agregue claves del Registro a los componentes. Cualquier clave del Registro que apunta a un archivo debe incluirse en el componente de ese archivo. Otras claves del Registro deben agruparse lógicamente con los archivos que las requieran.

 

 



