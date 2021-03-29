---
description: Windows Installer realiza las siguientes acciones durante la instalación de una aplicación cuando el paquete contiene componentes aislados. Normalmente, \_ el componente compartido es un archivo dll compartido por la \_ aplicación de componentes y otros ejecutables de cliente.
ms.assetid: fbc5dd86-5d38-4ce8-ab38-03c84cc77e80
title: Instalación de componentes aislados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c1b9a7e21c212474701409e887d0afd5517774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811474"
---
# <a name="installation-of-isolated-components"></a>Instalación de componentes aislados

Windows Installer realiza las siguientes acciones durante la instalación de una aplicación cuando el paquete contiene componentes aislados. Normalmente, \_ el componente compartido es un archivo dll compartido por la \_ aplicación de componentes y otros ejecutables de cliente.

## <a name="installation"></a>Instalación

-   Copie los archivos de componentes \_ compartidos en la misma carpeta que la aplicación de componentes \_ solo si \_ también se está instalando la aplicación de componentes.
-   Cree un archivo de cero bytes con el nombre de archivo corto del archivo de clave de la aplicación de componentes \_ . Busque este archivo en la misma carpeta que la \_ aplicación de componentes. Anexe la extensión. LOCAL a este nombre de archivo.
-   Incremente el recuento de SharedDLL si el bit msidbComponentAttributesSharedDllRefCount se establece en la columna Attributes de la [tabla Component](component-table.md).
-   Registre \_ la aplicación de componentes como un cliente del componente \_ compartido y registre una ruta de acceso de clave que apunte a la ubicación compartida del componente \_ compartido.
-   Instale todos los recursos de la aplicación de componentes de la \_ forma habitual.

Si \_ el componente compartido o su archivo de clave ya está instalado en el equipo, no copie los archivos en la ubicación compartida del componente \_ compartido.

Si \_ el componente compartido o su archivo de clave todavía no está instalado en el equipo:

-   Copie los archivos del componente \_ compartido en la ubicación compartida.
-   Procesa todas las acciones de instalación del componente \_ compartido.
-   Si \_ el componente compartido es un componente com, registre la ruta de acceso completa de com de forma que la sintaxis \[ $Component \] y \[ \# FileKey \] señalen a la ubicación compartida del componente \_ compartido.

 

 



