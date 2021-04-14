---
description: Un ensamblado privado es un ensamblado que se implementa con una aplicación y está disponible para el uso exclusivo de esa aplicación.
ms.assetid: 5E0E7423-85BD-4ED0-9149-9541F4D2371F
title: Acerca de los ensamblados privados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c7ccfe8c63a8435a33085f607c2040a0a42345c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648373"
---
# <a name="about-private-assemblies"></a>Acerca de los ensamblados privados

Un ensamblado privado es un ensamblado que se implementa con una aplicación y está disponible para el uso exclusivo de esa aplicación. Es decir, otras aplicaciones no comparten el ensamblado privado. Los ensamblados privados son uno de los métodos que se pueden usar para crear [aplicaciones aisladas](isolated-applications.md). Para obtener más información, vea [acerca de las aplicaciones aisladas y los ensamblados en paralelo](about-isolated-applications-and-side-by-side-assemblies.md).

Los ensamblados privados deben diseñarse para funcionar en paralelo con otras versiones del ensamblado en el sistema. Para obtener más información, vea [instrucciones para crear ensamblados en paralelo](guidelines-for-creating-side-by-side-assemblies.md).

Los ensamblados privados deben ir acompañados de un [manifiesto del ensamblado](assembly-manifests.md). Tenga en cuenta que se aplican restricciones de nombre al empaquetar un archivo DLL como ensamblado privado para dar cabida al modo en que Windows busca ensamblados privados. Al buscar ensamblados privados, el método recomendado consiste en incluir el manifiesto del ensamblado en el archivo DLL como un recurso. En este caso, el identificador de recurso debe ser igual a 1 y el nombre del ensamblado privado puede ser el mismo que el nombre del archivo DLL. Por ejemplo, si el nombre del archivo DLL es MICROSOFT.WINDOWS.MYSAMPLE.DLL, el valor del atributo name usado en el elemento **assemblyIdentity** del manifiesto también puede ser Microsoft. Windows. sample. Un método alternativo para buscar ensamblados privados es proporcionar el manifiesto del ensamblado en un archivo independiente. En este caso, el nombre del ensamblado y su manifiesto deben ser diferentes del nombre del archivo DLL. Por ejemplo, Microsoft. Windows. mysampleAsm, Microsoft. Windows. mysampleAsm. manifest y Microsoft.Windows.mysample.dll. Para obtener más información sobre cómo las búsquedas en paralelo de ensamblados privados, vea [secuencia de búsqueda de ensamblados](assembly-searching-sequence.md).

Los ensamblados privados se instalan en una carpeta de la estructura de directorios de la aplicación. Normalmente, se trata de la carpeta que contiene el archivo ejecutable de la aplicación. Los ensamblados privados se pueden implementar en la misma carpeta que la aplicación, en una carpeta con el mismo nombre que el ensamblado o en una subcarpeta específica del lenguaje con el mismo nombre que el ensamblado. Por ejemplo, utilice una de las siguientes estructuras de directorio para implementar un ensamblado privado, Microsoft. Tools. pop, sin ningún idioma especificado.



| Estructura de directorios                                       | Descripción                                                                                            |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| \\MICROSOFT.TOOLS.POP.DLL APPDIR                           | El manifiesto se implementa como un recurso en el archivo DLL.                                                     |
| Appdir \\ Microsoft. Tools. pop. manifest                      | El manifiesto se implementa como un archivo independiente.                                                           |
| APPDIR \\ Microsoft. Necesarias. \\MICROSOFT.TOOLS.POP.DLL pop      | El manifiesto se implementa como un recurso en el archivo DLL, que se encuentra en una subcarpeta con el nombre del ensamblado. |
| Appdir \\ Microsoft. Tools. pop \\ Microsoft. Tools. pop. manifest | El manifiesto se implementa como un archivo independiente en una subcarpeta con el nombre del ensamblado.                 |



 

> [!IMPORTANT]
>
> En el caso de las versiones del sistema operativo Windows anteriores a Windows 7 y Windows Server 2008 R2, los ensamblados privados nativos deben implementarse en la carpeta que contiene el archivo ejecutable de la aplicación. La instalación en una carpeta específica del lenguaje o en la carpeta con el mismo nombre que el ensamblado no se admite para los ensamblados privados nativos.

 

Use una de las siguientes estructuras de directorio para implementar un ensamblado privado, Microsoft. Tools. pop, con un idioma especificado. En el ejemplo siguiente, el idioma usado por Microsoft. Tools. pop es el inglés (Estados Unidos) y el código de idioma es en-US. Debe sustituir el código de lenguaje DHTML correcto para el ensamblado.

``` syntax
appdir\en-us\Microsoft.tools.pop.DLL
appdir\en-us\Microsoft.tools.pop.MANIFEST
appdir\en-us\Microsoft.tools.pop\Microsoft.tools.pop.DLL
appdir\en-us\Microsoft.tools.pop\Microsoft.tools.pop.MANIFEST
```

Los ensamblados privados se pueden instalar mediante cualquier método de instalación que pueda copiar el archivo del ensamblado en esta carpeta, como el comando **xcopy** . Para obtener más información sobre cómo instalar ensamblados privados mediante el Windows Installer, vea [instalación de ensamblados Win32](../msi/installation-of-win32-assemblies.md).

Los ensamblados privados también se pueden instalar en sistemas operativos anteriores a Windows XP. En este caso, el ensamblado debe estar registrado y en estos sistemas operativos el manifiesto no se utiliza. Se instala una copia del ensamblado privado en una carpeta privada para el uso exclusivo de la aplicación. Otra versión del ensamblado se puede registrar globalmente en el sistema y estar disponible para cualquier aplicación que se enlaza a ella. La versión global del ensamblado puede ser la versión instalada con la aplicación o una versión anterior. Para obtener más información, vea [redirección de dll/com en Windows](dll-com-redirection-on-windows.md). Un ensamblado también se puede instalar como un ensamblado compartido para su uso por parte de varias aplicaciones. Para obtener más información, vea [ensamblados compartidos](/windows/desktop/Msi/shared-assemblies).

Tenga en cuenta que los pasos para crear un ensamblado privado son idénticos a los de la creación de un ensamblado compartido con dos excepciones:

-   No es necesario firmar un ensamblado privado y no se requiere **publickeyToken** en el elemento **assemblyIdentity** del manifiesto del ensamblado.
-   Los ensamblados privados se pueden instalar en la carpeta de la aplicación mediante cualquier tecnología de instalación. No es necesario instalar los ensamblados privados mediante el Windows Installer.

 

 
