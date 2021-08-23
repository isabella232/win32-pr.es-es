---
description: A continuación se describe cómo crear un paquete Windows Installer para instalar un ensamblado Win32.
ms.assetid: 1234e904-fc7f-4eb7-8c50-0c959bbf5261
title: Instalación de ensamblados Win32 para uso compartido en paralelo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c62607b37a9abd26ce031d922e67fa3f48963193af054e1d71c6903474220e82
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500705"
---
# <a name="installing-win32-assemblies-for-side-by-side-sharing"></a>Instalación de ensamblados Win32 para uso compartido en paralelo

A continuación se describe cómo crear un paquete Windows Installer para instalar un ensamblado Win32. El paquete instala un ensamblado en paralelo en la carpeta Winsxs para el uso compartido de la aplicación. Después de instalar el paquete, el ensamblado compartido está disponible globalmente para cualquier aplicación que especifique una dependencia del ensamblado en un archivo de manifiesto de ensamblado. El instalador no registra globalmente el ensamblado en paralelo en el sistema.

Tenga en cuenta que puede instalar ensamblados compartidos en paralelo mediante [módulos de combinación](merge-modules.md).

Antes de continuar, debe entender cómo crear un paquete Windows Installer sin ensamblados. Para obtener un ejemplo de cómo crear una instalación simple, vea [Un ejemplo de instalación](an-installation-example.md).

**Para instalar un ensamblado compartido en paralelo**

1.  Defina un Windows installer que incluya el ensamblado Win32. Este componente puede contener otros recursos que siempre se deben instalar o quitar con el ensamblado. Todos los demás componentes de la aplicación se pueden crear igual que para una instalación sin ensamblados. Agregue una fila a la [tabla Component](component-table.md) para el componente que contiene el ensamblado Win32. Escriba un GUID Windows instalador [válido](guid.md) para este código de componente. No use el archivo de manifiesto como ruta de acceso de clave para este componente.
2.  Agregue una fila a la [tabla FeatureComponents](featurecomponents-table.md) que acote el componente a una Windows installer. Para obtener información, vea [Componentes y características](components-and-features.md). Una Windows installer debe ser una parte de la funcionalidad de la aplicación que un usuario pueda reconocer. El ensamblado se activa cuando un usuario selecciona esta característica o una aplicación ha registrado un error. Si el ensamblado define una característica adicional, agregue una fila adicional a la [tabla Característica](feature-table.md) para los atributos de la característica. Este paso no es necesario al crear un módulo de combinación.
3.  Para los ensamblados en paralelo, la información de enlace y activación, como clases COM, interfaces y bibliotecas de tipos, se almacena en archivos de manifiesto en lugar del Registro. Los ensamblados compartidos almacenan esta información en un manifiesto de ensamblado. En los sistemas que admiten ensamblados en paralelo, el instalador omite el procesamiento de cualquier información sobre el componente especificado en la tabla de extensión [,](extension-table.md)tabla verbo [,](verb-table.md)tabla [TypeLib,](typelib-table.md)tabla [MIME,](mime-table.md)tabla de [clases,](class-table.md)tabla [ProgId](progid-table.md)y [tabla AppId](appid-table.md). La información de enlace y activación se puede especificar en estas tablas para su uso por parte de sistemas que no admiten el uso compartido de ensamblados en paralelo.
4.  La instalación en paralelo no registra globalmente el ensamblado, el instalador omite el registro automático del componente si se ha especificado alguna información de registro automático en la [tabla SelfReg](selfreg-table.md). Se puede especificar información de registro propio en la tabla SelfReg para el registro propio del componente en sistemas que no admiten el uso compartido de ensamblados en paralelo.
5.  Agregue cualquier otra información del Registro, exclusiva del enlace y la activación o el registro propio del componente, a la tabla Registro [,](registry-table.md)a la tabla [RemoveRegistry](removeregistry-table.md)y a la [tabla Environment](environment-table.md).
6.  Dado que se trata de un ensamblado compartido, no se genera un archivo .local. No incluya información para este componente en la [tabla IsolatedComponent](isolatedcomponent-table.md). El instalador omite la tabla IsolatedComponent para este componente en sistemas operativos que admiten el uso compartido en paralelo. Agregue información a la tabla IsolatedComponent si desea que el ensamblado sea privado en sistemas que admiten archivos .local.
7.  Para habilitar el uso compartido en paralelo, el ensamblado Win32 debe instalarse en la carpeta Winsxs. Para ello, deja la columna Aplicación \_ de archivo de la tabla [MsiAssembly en](msiassembly-table.md) null para el ensamblado. Esto indica al instalador que instale el ensamblado en la carpeta WinSxS, en lugar de en la carpeta del componente. Agregue una fila a la [tabla MsiAssembly](msiassembly-table.md) para el componente que contiene el ensamblado Win32. Escriba un valor de 1 en el campo Atributos de la tabla MsiAssembly para especificar que se trata de un ensamblado Win32. Para un ensamblado compartido, deje vacío el campo Aplicación \_ de archivo. Agregue la [acción MsiPublishAssemblies](msipublishassemblies-action.md) a la [tabla InstallExecuteSequence](installexecutesequence-table.md) o a la tabla [AdvtExecuteSequence](advtexecutesequence-table.md). Agregue la [acción MsiUnpublishAssemblies a](msiunpublishassemblies-action.md) la tabla InstallExecuteSequence.
8.  Agregue filas a la [tabla MsiAssemblyName](msiassemblyname-table.md) para el componente. Agregue una fila por cada par de nombre y valor especificado en la sección assemblyIdentity del manifiesto. Para obtener un ejemplo, vea [la tabla MsiAssemblyName](msiassemblyname-table.md).

 

 



