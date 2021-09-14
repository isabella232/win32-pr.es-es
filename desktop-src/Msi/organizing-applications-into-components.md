---
description: Windows El instalador instala y quita una aplicación o un producto en partes denominadas componentes.
ms.assetid: 949d8b8c-8f1a-4fde-9a7d-824d33436e62
title: Organización de aplicaciones en componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3fc2db794bef2a29025bf7ebc54c65691145ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250995"
---
# <a name="organizing-applications-into-components"></a>Organización de aplicaciones en componentes

Windows El instalador instala y quita una aplicación o un producto en partes denominadas [componentes](windows-installer-components.md). Los componentes son colecciones de recursos que siempre se instalan o quitan como una unidad del sistema de un usuario. Un recurso puede ser un archivo, una clave del Registro, un acceso directo o cualquier otra cosa que se pueda instalar. A cada componente se le asigna un GUID de código de [componente único.](guid.md)

Los autores de paquetes de instalación solo deben crear componentes y versiones de componentes que se puedan instalar y quitar sin dañar otros componentes. Además, la eliminación de un componente no debe dejar ningún recurso huérfano en el equipo del usuario, como archivos sin usar, claves del Registro o accesos directos. Para garantizar esto, los autores deben cumplir las siguientes reglas generales al organizar los recursos en componentes:

-   Nunca cree dos componentes que instalen un recurso con el mismo nombre y ubicación de destino. Si un recurso debe estar duplicado en varios componentes, cambie su nombre o ubicación de destino en cada componente. Esta regla debe aplicarse entre aplicaciones, productos, versiones de productos y empresas.
-   Tenga en cuenta que la regla anterior significa que dos componentes no deben tener el mismo archivo de ruta de acceso de clave. El valor de ruta de acceso de clave apunta a un archivo o carpeta determinados que pertenecen al componente que el instalador usa para detectar el componente. Si dos componentes tuvieran el mismo archivo de ruta de acceso de clave, el instalador no podría distinguir qué componente está instalado. Sin embargo, dos componentes pueden compartir una carpeta de ruta de acceso de clave.
-   No cree una versión de un componente que no sea compatible con todas las versiones anteriores del componente. El componente puede ser compartido por otras aplicaciones, productos, versiones de productos y empresas. En su lugar, cree un nuevo componente.
-   No cree componentes que contengan recursos que deban instalarse en más de un directorio del sistema del usuario. El instalador instala todos los recursos de un componente en el mismo directorio. No es posible instalar algunos recursos en subdirectorios.
-   No incluya más de un servidor COM por componente. Si un componente contiene un servidor COM, debe ser la ruta de acceso de clave para el componente.
-   No especifique más de un archivo por componente como destino para el **menú** Inicio o un acceso directo de escritorio.

Al organizar una aplicación en componentes, es posible que los autores de paquetes deba agregar, quitar o modificar los recursos de una instalación existente. En este caso, el autor debe decidir si se deben proporcionar los recursos mediante la introducción de un nuevo componente o modificando los componentes existentes y cambiándolos a una nueva versión del componente. Dado que se debe asignar un código de componente único cuando se introduce un nuevo componente, los autores deben determinar si sus cambios requieren cambiar el código del componente. Para obtener más información, vea [Cambiar el código de](changing-the-component-code.md)componente , ¿Qué ocurre si se han roto las reglas de [componentes?](what-happens-if-the-component-rules-are-broken.md)y [Definir componentes del instalador](defining-installer-components.md).

 

 



