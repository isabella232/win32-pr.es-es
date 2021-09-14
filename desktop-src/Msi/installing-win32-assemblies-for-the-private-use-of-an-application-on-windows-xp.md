---
description: El procedimiento de este tema identifica cómo crear un paquete Windows Installer para instalar un ensamblado win32.
ms.assetid: 2d4bc2be-cce6-45e6-b6a7-7ff96d28eb96
title: Instalación de ensamblados Win32 para el uso privado de una aplicación en Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e807e22c9c5dea67ece5ead0ded95f06ab203689
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072037"
---
# <a name="installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp"></a>Instalación de ensamblados Win32 para el uso privado de una aplicación en Windows XP

El procedimiento de este tema identifica cómo crear un paquete Windows Installer para instalar un ensamblado win32. El paquete instala el ensamblado y un archivo de manifiesto de aplicación en una carpeta de creación que usa la aplicación. El manifiesto de aplicación especifica la dependencia de la aplicación en el ensamblado privado. Después de instalar el paquete, el ensamblado privado está disponible para el uso exclusivo de la aplicación. La dependencia del ensamblado que se especifica en el manifiesto de aplicación invalida (para esta aplicación) cualquier otra dependencia global de ensamblado especificada en los archivos de manifiesto del ensamblado.

Antes de continuar, es una buena idea entender cómo crear un paquete Windows Installer sin ensamblados. Para obtener más información, vea [Un ejemplo de instalación](an-installation-example.md).

**Para instalar un ensamblado privado en Windows XP**

1.  Defina un Windows installer que incluya el ensamblado Win32 y el archivo de manifiesto de aplicación. Este componente puede contener otros recursos que siempre se deben instalar o quitar con el ensamblado. Los pasos restantes de este procedimiento describen cómo crear la base de datos de instalación para instalar este componente.
2.  Agregue una fila a la tabla [Component](component-table.md) para el componente que contiene el ensamblado Win32 y el archivo de manifiesto de aplicación. Escriba un guid Windows [instalador válido](guid.md) para este código de componente. Para obtener más información, vea [Cambiar el código de componente](changing-the-component-code.md) y ¿Qué ocurre si se han roto las reglas de [componente?](what-happens-if-the-component-rules-are-broken.md)
3.  El instalador copia el archivo de manifiesto de ensamblado en la carpeta que contiene el archivo especificado en el campo Aplicación de archivo \_ de la [tabla MsiAssembly](msiassembly-table.md).
4.  Agregue una fila a la [tabla FeatureComponents](featurecomponents-table.md) que acote el componente a una Windows installer. Para obtener más información, [vea Componentes y características](components-and-features.md). Una Windows installer debe ser una parte de la funcionalidad de la aplicación que un usuario puede reconocer. El ensamblado se activa cuando un usuario selecciona esta característica o una aplicación no puede hacer esto. Si el ensamblado define una característica adicional, agregue una fila adicional a la [tabla Característica](feature-table.md) para los atributos de la característica. Este paso no es necesario si se va a crear un módulo de combinación.
5.  Para los ensamblados en paralelo, la información de enlace y activación, por ejemplo, clases COM, interfaces y bibliotecas de tipos, se almacena en archivos de manifiesto en lugar del Registro. Los ensamblados privados almacenan esta información en un manifiesto de ensamblado. En los sistemas que admiten ensamblados en paralelo, el instalador omite el procesamiento de cualquier información sobre el componente que se escribe en la tabla extension [,](extension-table.md) [tabla Verb](verb-table.md), [tabla TypeLib](typelib-table.md), tabla [MIME](mime-table.md) [,](class-table.md)tabla class, [tabla ProgId](progid-table.md)y [tabla AppId](appid-table.md). La información de enlace y activación se puede especificar en las tablas para su uso por parte de sistemas que no admiten el uso compartido de ensamblados en paralelo.
6.  La instalación en paralelo no registra el ensamblado globalmente. El instalador omite el registro automático del componente si se introduce información de registro automático en la [tabla SelfReg](selfreg-table.md). La información de registro propio se puede especificar en la tabla SelfReg para el registro propio del componente en sistemas que no admiten el uso compartido de ensamblados en paralelo.
7.  Agregue cualquier otra información del Registro, exclusiva del enlace y la activación o el registro propio del componente, a la tabla del Registro [,](registry-table.md)a la tabla [RemoveRegistry](removeregistry-table.md)y a la [tabla Environment](environment-table.md).
8.  El instalador omite la tabla [IsolatedComponent para](isolatedcomponent-table.md) este componente en sistemas operativos que admiten el uso compartido en paralelo. Escriba información en esta tabla si desea que el ensamblado sea privado en sistemas que admiten archivos locales.
9.  Agregue una fila a la [tabla MsiAssembly](msiassembly-table.md) para el componente que contiene el ensamblado Win32. Escriba un valor de 1 en el campo Atributos de la tabla MsiAssembly para especificar que se trata de un ensamblado Win32. Escriba la clave de archivo del ensamblado privado en el campo Aplicación \_ de archivo de la tabla [MsiAssembly](msiassembly-table.md). Agregue la [acción MsiPublishAssemblies](msipublishassemblies-action.md) a la [tabla InstallExecuteSequence](installexecutesequence-table.md) o a la tabla [AdvtExecuteSequence](advtexecutesequence-table.md). Agregue la [acción MsiUnpublishAssemblies](msiunpublishassemblies-action.md) a la tabla InstallExecuteSequence. Cree una carpeta para el ensamblado y el archivo de manifiesto en la [tabla Directory](directory-table.md). Esta carpeta debe estar en el directorio raíz de la aplicación y contener el archivo especificado en el campo Aplicación de archivo \_ de la [tabla MsiAssembly](msiassembly-table.md). Durante la instalación de la aplicación, el instalador resuelve la tabla [Directory para](directory-table.md) la ruta de acceso a esta carpeta. Para obtener más información, [vea Usar la tabla de directorios](using-the-directory-table.md).
10. Agregue filas a la [tabla MsiAssemblyName](msiassemblyname-table.md) del componente. Agregue una fila para cada par de nombre y valor especificado en la sección assemblyIdentity del manifiesto. Para obtener más información, [vea Tabla MsiAssemblyName](msiassemblyname-table.md).

 

 



