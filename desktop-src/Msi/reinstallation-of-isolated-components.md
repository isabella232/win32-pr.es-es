---
description: Windows El instalador realiza las siguientes acciones durante la reinstalación de una aplicación cuando el paquete contiene componentes aislados. Normalmente, El componente \_ compartido es un archivo DLL compartido por la aplicación de componentes y otros \_ ejecutables de cliente.
ms.assetid: 65909b47-dc09-4e9a-920a-9cb3f55b2e67
title: Reinstalación de componentes aislados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ad1c7fb53eb09e96882209f7738e95be9b4a64
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127274164"
---
# <a name="reinstallation-of-isolated-components"></a>Reinstalación de componentes aislados

Windows El instalador realiza las siguientes acciones durante la reinstalación de una aplicación cuando el paquete contiene componentes aislados. Normalmente, El componente \_ compartido es un archivo DLL compartido por la aplicación de componentes y otros \_ ejecutables de cliente.

## <a name="reinstallation"></a>Reinstalación

-   Vuelva a instalar los archivos de Componente compartido en la misma carpeta que aplicación de componente solo si también se vuelve a \_ instalar la aplicación de \_ \_ componentes.
-   No incremente la lista de clientes de Componente \_ compartido y no incremente el recuento de SharedDLL.
-   Vuelva a crear el archivo de cero bytes con el nombre de archivo corto del archivo de clave de aplicación \_ de componentes. Este archivo debe encontrarse en la misma carpeta que la aplicación \_ de componentes y tener la extensión . LOCAL.
-   Vuelva a instalar todos los recursos de la aplicación \_ de componentes como de costumbre.

Si el recuento de referencias de SharedDLL para El componente compartido es mayor que 1, o si otros productos permanecen en la lista de clientes \_ de Componente \_ compartido:

-   Vuelva a instalar ningún archivo en la ubicación compartida de Component \_ Shared.

Si el recuento de referencias de SharedDLL para Component Shared es igual a 1 o si no hay ningún otro cliente \_ restante de Component \_ Shared:

-   Vuelva a instalar los archivos de Componente \_ compartido en la ubicación compartida mediante las reglas de control de versiones de [archivos](file-versioning-rules.md).
-   Procese todas las acciones de reinstalación para Componente \_ compartido.
-   Si Componente compartido es un componente COM, registre la ruta de acceso COM completa de modo que las sintaxis del instalador $Component y FileKey apunten a la ubicación compartida de \_ \[ Componente \] \[ \# \] \_ compartido.

 

 



