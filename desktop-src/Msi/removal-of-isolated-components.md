---
description: Windows El instalador realiza las siguientes acciones durante la eliminación de una aplicación cuando el paquete contiene componentes aislados. Normalmente, El componente \_ compartido es un archivo DLL compartido por la aplicación de componentes y otros \_ ejecutables de cliente.
ms.assetid: 26343a01-9a06-43d5-bbe3-959faf51739d
title: Eliminación de componentes aislados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf19769067230b82f68a35f7b9fbedcd1c56440
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069655"
---
# <a name="removal-of-isolated-components"></a>Eliminación de componentes aislados

Windows El instalador realiza las siguientes acciones durante la eliminación de una aplicación cuando el paquete contiene componentes aislados. Normalmente, El componente \_ compartido es un archivo DLL compartido por la aplicación de componentes y otros \_ ejecutables de cliente.

## <a name="uninstall"></a>Desinstalación

-   Quite los archivos de Componente compartido de la carpeta que contiene Aplicación de componente solo si también \_ \_ se está \_ quitando la aplicación de componentes.
-   Si el bit msidbComponentAttributesSharedDllRefCount se establece en la tabla [Component,](component-table.md) disminuye el recuento de referencias de SharedDLL.
-   Quite el . Archivo local de cero bytes de la carpeta que contiene aplicación de \_ componentes.
-   Quite Aplicación \_ de componente de la lista de cliente de Componente \_ compartido.
-   Quite todos los recursos de aplicación de \_ componentes como de costumbre.

Si quedan otros productos en la lista de clientes de Componente \_ compartido:

-   Quite ningún archivo de la ubicación compartida de Component \_ Shared.

Si el recuento de referencias de SharedDLL para Component Shared es 0 después de disminuir, o si no hay ningún otro cliente restante de \_ Component \_ Shared:

-   Quite los archivos de Component \_ Shared de la ubicación compartida.
-   Procese todas las acciones de desinstalación con respecto a este componente.

 

 



