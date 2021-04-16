---
description: En el procedimiento de este tema se identifica cómo crear un paquete de Windows Installer para instalar un ensamblado Win32.
ms.assetid: 2d4bc2be-cce6-45e6-b6a7-7ff96d28eb96
title: Instalar ensamblados Win32 para el uso privado de una aplicación en Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e807e22c9c5dea67ece5ead0ded95f06ab203689
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686884"
---
# <a name="installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp"></a>Instalar ensamblados Win32 para el uso privado de una aplicación en Windows XP

En el procedimiento de este tema se identifica cómo crear un paquete de Windows Installer para instalar un ensamblado Win32. El paquete instala el ensamblado y un archivo de manifiesto de aplicación en una carpeta creada que utiliza la aplicación. El manifiesto de aplicación especifica la dependencia de la aplicación en el ensamblado privado. Después de instalar el paquete, el ensamblado privado está disponible para el uso exclusivo de la aplicación. La dependencia del ensamblado que se especifica en el manifiesto de aplicación invalida (para esta aplicación) cualquier otra dependencia global de ensamblados que se especifica en los archivos de manifiesto del ensamblado.

Antes de continuar, es una buena idea comprender cómo crear un paquete de Windows Installer sin ensamblados. Para obtener más información, vea [un ejemplo de instalación](an-installation-example.md).

**Para instalar un ensamblado privado en Windows XP**

1.  Defina un componente de Windows Installer que incluya el ensamblado Win32 y el archivo de manifiesto de la aplicación. Este componente puede contener otros recursos que se deben instalar o quitar siempre con el ensamblado. En los pasos restantes de este procedimiento se describe cómo crear la base de datos de instalación para instalar este componente.
2.  Agregue una fila a la [tabla de componentes](component-table.md) del componente que contiene el ensamblado de Win32 y el archivo de manifiesto de la aplicación. Escriba un [GUID](guid.md) de Windows Installer válido para este código de componente. Para obtener más información, vea [cambiar el código de componente](changing-the-component-code.md) y [lo que sucede si se interrumpen las reglas de componentes](what-happens-if-the-component-rules-are-broken.md) .
3.  El instalador copia el archivo de manifiesto del ensamblado en la carpeta que contiene el archivo especificado en el \_ campo de la aplicación de archivo de la [tabla MsiAssembly](msiassembly-table.md).
4.  Agregue una fila a la [tabla FeatureComponents](featurecomponents-table.md) que asocia el componente a una característica Windows Installer. Para obtener más información, vea [componentes y características](components-and-features.md). Una característica Windows Installer debe ser una parte de la funcionalidad de la aplicación que un usuario pueda reconocer. El ensamblado se activa cuando el usuario selecciona esta característica o la aplicación produce un error. Si el ensamblado define una característica adicional, agregue una fila adicional a la [tabla de características](feature-table.md) para los atributos de la característica. Este paso no es necesario si se crea un módulo de combinación.
5.  En el caso de los ensamblados en paralelo, la información de enlace y activación, por ejemplo, las clases COM, las interfaces y las bibliotecas de tipos, se almacena en archivos de manifiesto en lugar de en el registro. Los ensamblados privados almacenan esta información en un manifiesto del ensamblado. En los sistemas que admiten ensamblados en paralelo, el instalador omite el procesamiento de toda la información sobre el componente que se especifica en la [tabla de extensión](extension-table.md), la [tabla de verbos](verb-table.md), la [tabla typelib](typelib-table.md), la [tabla MIME](mime-table.md), la tabla de [clases](class-table.md), la [tabla ProgID](progid-table.md)y la [tabla AppID](appid-table.md). La información de enlace y activación se puede incluir en las tablas para que las usen los sistemas que no admiten el uso compartido de ensamblados en paralelo.
6.  La instalación en paralelo no registra el ensamblado globalmente. El instalador omite el registro automático del componente si se especifica cualquier información de registro automático en la [tabla SelfReg](selfreg-table.md). La información de registro automático se puede escribir en la tabla SelfReg para el registro automático del componente en sistemas que no admiten el uso compartido de ensamblados en paralelo.
7.  Agregue cualquier otra información del registro, exclusiva del enlace y activación o el registro automático del componente, a la tabla [del registro](registry-table.md), la [tabla RemoveRegistry](removeregistry-table.md)y la [tabla de entorno](environment-table.md).
8.  El instalador omite la [tabla IsolatedComponent](isolatedcomponent-table.md) para este componente en los sistemas operativos que admiten el uso compartido en paralelo. Escriba información en esta tabla si desea que el ensamblado sea privado en sistemas que admitan archivos locales.
9.  Agregue una fila a la [tabla MsiAssembly](msiassembly-table.md) para el componente que contiene el ensamblado Win32. Escriba un valor de 1 en el campo atributos de la tabla MsiAssembly para especificar que se trata de un ensamblado Win32. Escriba la clave de archivo del ensamblado privado en el \_ campo aplicación de archivo de la [tabla MsiAssembly](msiassembly-table.md). Agregue la [acción MsiPublishAssemblies](msipublishassemblies-action.md) a la [tabla InstallExecuteSequence](installexecutesequence-table.md) o a la [tabla AdvtExecuteSequence](advtexecutesequence-table.md). Agregue la [acción MsiUnpublishAssemblies](msiunpublishassemblies-action.md) a la tabla InstallExecuteSequence. Cree una carpeta para el archivo de ensamblado y de manifiesto en la [tabla de directorio](directory-table.md). Esta carpeta debe estar en el directorio raíz de la aplicación y contener el archivo especificado en el \_ campo aplicación de archivo de la [tabla MsiAssembly](msiassembly-table.md). Durante la instalación de la aplicación, el instalador resuelve la tabla de [directorio](directory-table.md) de la ruta de acceso a esta carpeta. Para obtener más información, consulte [uso de la tabla de directorios](using-the-directory-table.md).
10. Agregue filas a la [tabla MsiAssemblyName](msiassemblyname-table.md) para el componente. Agregue una fila para cada par de nombre y valor especificado en la sección assemblyIdentity del manifiesto. Para obtener más información, consulte [tabla MsiAssemblyName](msiassemblyname-table.md).

 

 



