---
description: A continuación se describe cómo crear un paquete de Windows Installer para instalar un ensamblado Win32.
ms.assetid: 1234e904-fc7f-4eb7-8c50-0c959bbf5261
title: Instalación de ensamblados Win32 para el uso compartido en paralelo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea72c9bcb7bd85ac38dfc8857030d6b9d6afbf23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688450"
---
# <a name="installing-win32-assemblies-for-side-by-side-sharing"></a>Instalación de ensamblados Win32 para el uso compartido en paralelo

A continuación se describe cómo crear un paquete de Windows Installer para instalar un ensamblado Win32. El paquete instala un ensamblado en paralelo en la carpeta WinSxS para el uso compartido de la aplicación. Después de instalar el paquete, el ensamblado compartido está disponible globalmente para cualquier aplicación que especifique una dependencia en el ensamblado en un archivo de manifiesto del ensamblado. El instalador no registra globalmente el ensamblado en paralelo en el sistema.

Tenga en cuenta que puede instalar ensamblados en paralelo compartidos mediante [módulos de combinación](merge-modules.md).

Antes de continuar, debe comprender cómo crear un paquete de Windows Installer sin ensamblados. Para obtener un ejemplo de cómo crear una instalación simple, vea [un ejemplo de instalación](an-installation-example.md).

**Para instalar un ensamblado compartido en paralelo**

1.  Defina un componente de Windows Installer que incluya el ensamblado Win32. Este componente puede contener otros recursos que se deben instalar o quitar siempre con el ensamblado. Todos los demás componentes de la aplicación se pueden crear como para una instalación sin ensamblados. Agregue una fila a la [tabla de componentes](component-table.md) del componente que contiene el ensamblado Win32. Escriba un [GUID](guid.md) de Windows Installer válido para este código de componente. No use el archivo de manifiesto como la ruta de acceso de la clave para este componente.
2.  Agregue una fila a la [tabla FeatureComponents](featurecomponents-table.md) que asocia el componente a una característica Windows Installer. Para obtener información, vea [componentes y características](components-and-features.md). Una característica Windows Installer debe ser una parte de la funcionalidad de la aplicación que sea reconocible para un usuario. El ensamblado se activa cuando el usuario selecciona esta característica o la aplicación produce un error. Si el ensamblado define una característica adicional, agregue una fila adicional a la [tabla de características](feature-table.md) para los atributos de la característica. Este paso no es necesario cuando se crea un módulo de combinación.
3.  En el caso de los ensamblados en paralelo, la información de enlace y activación, como las clases COM, las interfaces y las bibliotecas de tipos, se almacena en archivos de manifiesto en lugar de en el registro. Los ensamblados compartidos almacenan esta información en un manifiesto del ensamblado. En los sistemas que admiten ensamblados en paralelo, el instalador omite el procesamiento de toda la información sobre el componente especificado en la tabla de [extensión](extension-table.md), la [tabla de verbos](verb-table.md), la [tabla typelib](typelib-table.md), la [tabla MIME](mime-table.md), la tabla de [clases](class-table.md), la [tabla ProgID](progid-table.md)y la [tabla AppID](appid-table.md). La información de enlace y activación se puede incluir en estas tablas para que las usen los sistemas que no admiten el uso compartido de ensamblados en paralelo.
4.  La instalación en paralelo no registra el ensamblado globalmente, el instalador omite el registro automático del componente si se ha especificado información de registro automático en la [tabla SelfReg](selfreg-table.md). La información de registro automático se puede escribir en la tabla SelfReg para el registro automático del componente en sistemas que no admiten el uso compartido de ensamblados en paralelo.
5.  Agregue cualquier otra información del registro, exclusiva del enlace y activación o el registro automático del componente, a la tabla [del registro](registry-table.md), la [tabla RemoveRegistry](removeregistry-table.md)y la [tabla de entorno](environment-table.md).
6.  Dado que se trata de un ensamblado compartido, no se genera un archivo. local. No incluya información para este componente en la [tabla IsolatedComponent](isolatedcomponent-table.md). El instalador omite la tabla IsolatedComponent para este componente en los sistemas operativos que admiten el uso compartido en paralelo. Agregue información a la tabla IsolatedComponent si desea que el ensamblado sea privado en los sistemas que admiten archivos. local.
7.  Para habilitar el uso compartido simultáneo, el ensamblado Win32 debe instalarse en la carpeta WinSxS. Esto se logra al mantener la \_ columna de aplicación de archivo de la [tabla MsiAssembly](msiassembly-table.md) null para el ensamblado. Esto indica al instalador que instale el ensamblado en la carpeta WinSxS, en lugar de en la carpeta del componente. Agregue una fila a la [tabla MsiAssembly](msiassembly-table.md) para el componente que contiene el ensamblado Win32. Escriba un valor de 1 en el campo atributos de la tabla MsiAssembly para especificar que se trata de un ensamblado Win32. Para un ensamblado compartido, deje vacío el campo de la aplicación de archivo \_ . Agregue la [acción MsiPublishAssemblies](msipublishassemblies-action.md) a la [tabla InstallExecuteSequence](installexecutesequence-table.md) o a la [tabla AdvtExecuteSequence](advtexecutesequence-table.md). Agregue la [acción MsiUnpublishAssemblies](msiunpublishassemblies-action.md) a la tabla InstallExecuteSequence.
8.  Agregue filas a la [tabla MsiAssemblyName](msiassemblyname-table.md) para el componente. Agregue una fila para cada par de nombre y valor especificado en la sección assemblyIdentity del manifiesto. Para ver un ejemplo, consulte la [tabla MsiAssemblyName](msiassemblyname-table.md).

 

 



