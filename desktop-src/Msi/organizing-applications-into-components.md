---
description: Windows Installer instala y quita una aplicación o un producto en elementos denominados componentes.
ms.assetid: 949d8b8c-8f1a-4fde-9a7d-824d33436e62
title: Organizar aplicaciones en componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3fc2db794bef2a29025bf7ebc54c65691145ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909014"
---
# <a name="organizing-applications-into-components"></a>Organizar aplicaciones en componentes

Windows Installer instala y quita una aplicación o un producto en elementos denominados [componentes](windows-installer-components.md). Los componentes son colecciones de recursos que siempre se instalan o se quitan como una unidad del sistema de un usuario. Un recurso puede ser un archivo, una clave del registro, un acceso directo o cualquier otro elemento que se pueda instalar. A cada componente se le asigna un [GUID](guid.md)de código de componente único.

Los autores de los paquetes de instalación solo deben crear componentes y versiones de componentes que se puedan instalar y quitar sin dañar otros componentes. Además, la eliminación de un componente no debe quedar detrás de ningún recurso huérfano en el equipo del usuario, como archivos no usados, claves del registro o accesos directos. Para garantizar esto, los autores deben cumplir las siguientes reglas generales al organizar los recursos en componentes:

-   No cree nunca dos componentes que instalen un recurso con el mismo nombre y la misma ubicación de destino. Si un recurso se debe duplicar en varios componentes, cambie su nombre o ubicación de destino en cada componente. Esta regla debe aplicarse a todas las aplicaciones, productos, versiones de producto y compañías.
-   Tenga en cuenta que la regla anterior significa que dos componentes no deben tener el mismo archivo de ruta de acceso de clave. El valor de la ruta de acceso de la clave apunta a un archivo o carpeta determinado perteneciente al componente que el instalador usa para detectar el componente. Si dos componentes tenían el mismo archivo de ruta de acceso de clave, el instalador no puede distinguir qué componente está instalado. Sin embargo, dos componentes pueden compartir una carpeta de ruta de acceso de clave.
-   No cree una versión de un componente que sea incompatible con todas las versiones anteriores del componente. El componente puede ser compartido por otras aplicaciones, productos, versiones de producto y compañías. En su lugar, cree un nuevo componente.
-   No cree componentes que contengan recursos que deberán instalarse en más de un directorio en el sistema del usuario. El instalador instala todos los recursos de un componente en el mismo directorio. No es posible instalar algunos recursos en subdirectorios.
-   No incluya más de un servidor COM por componente. Si un componente contiene un servidor COM, debe ser la ruta de acceso de la clave del componente.
-   No especifique más de un archivo por componente como destino para el menú **Inicio** o un acceso directo del escritorio.

Al organizar una aplicación en componentes de, es posible que los autores de paquetes necesiten agregar, quitar o modificar los recursos de una instalación de existente. En este caso, el autor debe decidir si proporcionar los recursos mediante la introducción de un nuevo componente o la modificación de los componentes existentes y su cambio en una nueva versión del componente. Dado que se debe asignar un código de componente único cuando se introduce un componente nuevo, los autores deben determinar si los cambios requieren cambiar el código de componente. Para obtener más información, vea [cambiar el código del componente](changing-the-component-code.md), [¿Qué ocurre si se interrumpen las reglas del componente?](what-happens-if-the-component-rules-are-broken.md)y [definir los componentes del instalador](defining-installer-components.md).

 

 



