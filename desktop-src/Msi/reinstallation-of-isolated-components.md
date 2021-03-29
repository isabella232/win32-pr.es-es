---
description: Windows Installer realiza las siguientes acciones durante la reinstalación de una aplicación cuando el paquete contiene componentes aislados. Normalmente, \_ el componente compartido es un archivo dll compartido por la \_ aplicación de componentes y otros ejecutables de cliente.
ms.assetid: 65909b47-dc09-4e9a-920a-9cb3f55b2e67
title: Reinstalación de componentes aislados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ad1c7fb53eb09e96882209f7738e95be9b4a64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909446"
---
# <a name="reinstallation-of-isolated-components"></a>Reinstalación de componentes aislados

Windows Installer realiza las siguientes acciones durante la reinstalación de una aplicación cuando el paquete contiene componentes aislados. Normalmente, \_ el componente compartido es un archivo dll compartido por la \_ aplicación de componentes y otros ejecutables de cliente.

## <a name="reinstallation"></a>Reinstalación

-   Vuelva a instalar los archivos de componentes \_ compartidos en la misma carpeta que la aplicación de componentes \_ solo si \_ también se está reinstalando la aplicación de componentes.
-   No incremente la lista de cliente del componente \_ compartido y no aumente el número de SharedDLL.
-   Vuelva a crear el archivo de cero bytes con el nombre de archivo corto del archivo de clave de la aplicación de componentes \_ . Este archivo debe estar ubicado en la misma carpeta que \_ la aplicación de componentes y tener la extensión. Localizar.
-   Vuelva a instalar todos los recursos de la aplicación de componentes de la \_ forma habitual.

Si el recuento de SharedDLL del componente \_ compartido es mayor que 1, o si otros productos permanecen en la lista de clientes \_ compartida:

-   Reinstalar ningún archivo en la ubicación compartida del componente \_ compartido.

Si el recuento de SharedDLL del componente \_ compartido es igual a 1, o si no hay otros clientes restantes del componente \_ compartido:

-   Vuelva a instalar los archivos de componentes \_ compartidos en la ubicación compartida con las [reglas de control de versiones de archivo](file-versioning-rules.md).
-   Procesa todas las acciones de reinstalación del componente \_ compartido.
-   Si \_ el componente compartido es un componente com, registre la ruta de acceso completa de com de forma que las sintaxis del instalador \[ $Component \] y \[ \# FileKey \] señalen a la ubicación compartida del componente \_ compartido.

 

 



