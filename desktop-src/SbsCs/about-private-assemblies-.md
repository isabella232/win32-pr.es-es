---
description: Un ensamblado privado es un ensamblado que se implementa con una aplicación y está disponible para su uso exclusivo.
ms.assetid: 5E0E7423-85BD-4ED0-9149-9541F4D2371F
title: Acerca de los ensamblados privados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c7ccfe8c63a8435a33085f607c2040a0a42345c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271804"
---
# <a name="about-private-assemblies"></a>Acerca de los ensamblados privados

Un ensamblado privado es un ensamblado que se implementa con una aplicación y está disponible para su uso exclusivo. Es decir, otras aplicaciones no comparten el ensamblado privado. Los ensamblados privados son uno de los métodos que se pueden usar para crear [aplicaciones aisladas.](isolated-applications.md) Para obtener más información, vea Acerca de las aplicaciones aisladas y los [ensamblados en paralelo.](about-isolated-applications-and-side-by-side-assemblies.md)

Los ensamblados privados deben estar diseñados para funcionar en paralelo con otras versiones del ensamblado en el sistema. Para obtener más información, vea [Directrices para crear](guidelines-for-creating-side-by-side-assemblies.md)ensamblados en paralelo.

Los ensamblados privados deben ir acompañados de un [manifiesto de ensamblado](assembly-manifests.md). Tenga en cuenta que se aplican restricciones de nombre al empaquetar un archivo DLL como un ensamblado privado para adaptarse a la forma en que Windows busca ensamblados privados. Al buscar ensamblados privados, el método recomendado es incluir el manifiesto de ensamblado en el archivo DLL como un recurso. En este caso, el identificador de recurso debe ser igual a 1 y el nombre del ensamblado privado puede ser el mismo que el nombre del archivo DLL. Por ejemplo, si el nombre del archivo DLL es MICROSOFT.WINDOWS.MYSAMPLE.DLL, el valor del atributo name usado en el elemento **assemblyIdentity** del manifiesto también puede ser Microsoft. Windows.mysample. Un método alternativo para buscar ensamblados privados es proporcionar el manifiesto del ensamblado en un archivo independiente. En este caso, el nombre del ensamblado y su manifiesto deben ser diferentes del nombre del archivo DLL. Por ejemplo, Microsoft. Windows.mysampleAsm, Microsoft. Windows.mysampleAsm.manifest y Microsoft.Windows.mysample.dll. Para obtener más información sobre cómo busca ensamblados privados en paralelo, vea [Secuencia de búsqueda de ensamblados.](assembly-searching-sequence.md)

Los ensamblados privados se instalan en una carpeta de la estructura de directorios de la aplicación. Normalmente, esta es la carpeta que contiene el archivo ejecutable de la aplicación. Los ensamblados privados se pueden implementar en la misma carpeta que la aplicación, en una carpeta con el mismo nombre que el ensamblado o en una subcarpeta específica del lenguaje con el mismo nombre que el ensamblado. Por ejemplo, use una de las siguientes estructuras de directorio para implementar un ensamblado privado, Microsoft.tools.pop, sin ningún lenguaje especificado.



| Estructura de directorios                                       | Descripción                                                                                            |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| AppDIR \\MICROSOFT.TOOLS.POP.DLL                           | El manifiesto se implementa como un recurso en el archivo DLL.                                                     |
| Appdir \\ Microsoft.Tools.Pop.MANIFEST                      | El manifiesto se implementa como un archivo independiente.                                                           |
| APPDIR \\ MICROSOFT. HERRAMIENTAS. Pop \\MICROSOFT.TOOLS.POP.DLL      | El manifiesto se implementa como un recurso en el archivo DLL, que se encuentra en una subcarpeta con el nombre del ensamblado. |
| Appdir \\ Microsoft.Tools.Pop \\ Microsoft.Tools.Pop.MANIFEST | El manifiesto se implementa como un archivo independiente en una subcarpeta con el nombre del ensamblado.                 |



 

> [!IMPORTANT]
>
> Para las versiones del sistema operativo Windows anteriores a Windows 7 y Windows Server 2008 R2, los ensamblados privados nativos deben implementarse en la carpeta que contiene el archivo ejecutable de la aplicación. La instalación en una carpeta específica del lenguaje o en la carpeta con el mismo nombre que el ensamblado no se admite para los ensamblados privados nativos.

 

Use una de las siguientes estructuras de directorio para implementar un ensamblado privado, Microsoft.tools.pop, con un idioma especificado. En el ejemplo siguiente, el idioma que usa Microsoft.Tools.Pop es inglés (Estados Unidos) y el código de idioma es en-us. Debe sustituir el código de lenguaje DHTML correcto para el ensamblado.

``` syntax
appdir\en-us\Microsoft.tools.pop.DLL
appdir\en-us\Microsoft.tools.pop.MANIFEST
appdir\en-us\Microsoft.tools.pop\Microsoft.tools.pop.DLL
appdir\en-us\Microsoft.tools.pop\Microsoft.tools.pop.MANIFEST
```

Los ensamblados privados se pueden instalar mediante cualquier método de instalación que pueda copiar el archivo del ensamblado en esta carpeta, como el **comando xcopy.** Para obtener más información sobre cómo instalar ensamblados privados mediante Windows Installer, vea [Instalación de ensamblados Win32.](../msi/installation-of-win32-assemblies.md)

Los ensamblados privados también se pueden instalar en sistemas operativos anteriores a Windows XP. En este caso, el ensamblado debe estar registrado y en estos sistemas operativos no se usa el manifiesto. Una copia del ensamblado privado se instala en una carpeta privada para el uso exclusivo de la aplicación. Otra versión del ensamblado se puede registrar globalmente en el sistema y estar disponible para cualquier aplicación que se enlaza a él. La versión global del ensamblado puede ser la versión instalada con la aplicación o una versión anterior. Para obtener más información, vea [Redirección de DLL/COM en Windows](dll-com-redirection-on-windows.md). Un ensamblado también se puede instalar como un ensamblado compartido para que lo usen varias aplicaciones. Para obtener más información, vea [Ensamblados compartidos](/windows/desktop/Msi/shared-assemblies).

Tenga en cuenta que los pasos para crear un ensamblado privado son idénticos a los de creación de un ensamblado compartido con dos excepciones:

-   No es necesario firmar un ensamblado privado y **publickeyToken** no es necesario en el **elemento assemblyIdentity** del manifiesto del ensamblado.
-   Los ensamblados privados se pueden instalar en la carpeta de la aplicación mediante cualquier tecnología de instalación. No es necesario instalar ensamblados privados mediante el instalador Windows.

 

 
