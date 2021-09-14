---
description: Windows El instalador realiza las siguientes acciones durante la instalación de una aplicación cuando el paquete contiene componentes aislados. Normalmente, El componente \_ compartido es un archivo DLL compartido por la aplicación de componentes y otros \_ ejecutables de cliente.
ms.assetid: fbc5dd86-5d38-4ce8-ab38-03c84cc77e80
title: Instalación de componentes aislados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c1b9a7e21c212474701409e887d0afd5517774
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171778"
---
# <a name="installation-of-isolated-components"></a>Instalación de componentes aislados

Windows El instalador realiza las siguientes acciones durante la instalación de una aplicación cuando el paquete contiene componentes aislados. Normalmente, El componente \_ compartido es un archivo DLL compartido por la aplicación de componentes y otros \_ ejecutables de cliente.

## <a name="installation"></a>Instalación

-   Copie los archivos de Componente compartido en la misma carpeta que aplicación de componente solo si también \_ \_ se está \_ instalando la aplicación de componentes.
-   Cree un archivo de cero bytes con el nombre de archivo corto del archivo de clave de aplicación \_ de componentes. Busque este archivo en la misma carpeta que aplicación \_ de componentes. Anexe la extensión . LOCAL a este nombre de archivo.
-   Incremente el recuento de referencias de SharedDLL si el bit msidbComponentAttributesSharedDllRefCount está establecido en la columna Atributos de la [tabla Component](component-table.md).
-   Registre aplicación de componente como cliente de Componente compartido y registre una ruta de acceso clave que apunte \_ a la ubicación compartida de Componente \_ \_ compartido.
-   Instale todos los recursos de aplicación de \_ componentes como de costumbre.

Si el componente Compartido o su archivo de clave ya está instalado en el equipo, no copie los archivos en la \_ ubicación compartida de Componente \_ compartido.

Si el \_ componente Compartido o su archivo de clave aún no están instalados en el equipo:

-   Copie los archivos de Componente \_ compartido en la ubicación compartida.
-   Procese todas las acciones de instalación de Component \_ Shared.
-   Si Componente compartido es un componente COM, registre la ruta de acceso COM completa de modo que la sintaxis $Component y FileKey apunten a la ubicación compartida \_ \[ de Componente \] \[ \# \] \_ compartido.

 

 



