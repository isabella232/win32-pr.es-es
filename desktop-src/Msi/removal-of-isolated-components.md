---
description: Windows Installer realiza las siguientes acciones durante la eliminación de una aplicación cuando el paquete contiene componentes aislados. Normalmente, \_ el componente compartido es un archivo dll compartido por la \_ aplicación de componentes y otros ejecutables de cliente.
ms.assetid: 26343a01-9a06-43d5-bbe3-959faf51739d
title: Eliminación de componentes aislados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf19769067230b82f68a35f7b9fbedcd1c56440
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652853"
---
# <a name="removal-of-isolated-components"></a>Eliminación de componentes aislados

Windows Installer realiza las siguientes acciones durante la eliminación de una aplicación cuando el paquete contiene componentes aislados. Normalmente, \_ el componente compartido es un archivo dll compartido por la \_ aplicación de componentes y otros ejecutables de cliente.

## <a name="uninstall"></a>Desinstalación

-   Quite los archivos de componentes \_ compartidos de la carpeta que contiene la aplicación de componentes \_ solo si \_ también se está quitando la aplicación de componentes.
-   Si el bit msidbComponentAttributesSharedDllRefCount se establece en la [tabla de componentes](component-table.md) , se reduce el recuento de SharedDLL.
-   Quite el. Archivo de cero bytes LOCAL de la carpeta que contiene la aplicación de componentes \_ .
-   Quite \_ la aplicación de componentes de la lista de clientes de componentes \_ compartidos.
-   Quite todos los recursos de la aplicación de componentes de la \_ forma habitual.

Si quedan otros productos en la lista de clientes del componente \_ compartido:

-   No se quita ningún archivo de la ubicación compartida del componente \_ compartido.

Si el recuento de SharedDLL del componente \_ compartido es 0 después de haber disminuido, o si no hay otros clientes restantes del componente \_ compartido:

-   Quite los archivos del componente \_ compartido de la ubicación compartida.
-   Procesa todas las acciones de desinstalación con respecto a este componente.

 

 



