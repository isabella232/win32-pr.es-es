---
description: Si una aplicación aislada especifica una dependencia de ensamblado, en paralelo busca el ensamblado entre los ensamblados compartidos de la carpeta WinSxS.
ms.assetid: 93496631-55cc-4dd9-9a51-b748c35fd477
title: Secuencia de búsqueda de ensamblado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc689ecb14c55f0e8a609c7e7497fce969e88b8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082882"
---
# <a name="assembly-searching-sequence"></a>Secuencia de búsqueda de ensamblado

Si una aplicación aislada especifica una dependencia de ensamblado, en paralelo busca el ensamblado entre los [ensamblados compartidos](/windows/desktop/Msi/shared-assemblies) de la carpeta WinSxS. Si no se encuentra el ensamblado necesario, en paralelo buscará un ensamblado privado instalado en una carpeta de la estructura de directorios de la aplicación.

Los [ensamblados privados](/windows/desktop/Msi/private-assemblies) se pueden implementar en las siguientes ubicaciones en la estructura de directorios de la aplicación:

-   En la carpeta de la aplicación. Normalmente, se trata de la carpeta que contiene el archivo ejecutable de la aplicación.
-   En una subcarpeta de la carpeta de la aplicación. La subcarpeta debe tener el mismo nombre que el ensamblado.
-   En una subcarpeta específica del lenguaje de la carpeta de la aplicación. El nombre de la subcarpeta es una cadena de códigos de lenguaje DHTML que indica una referencia cultural de idioma o un idioma.
-   En una subcarpeta de una subcarpeta específica del lenguaje en la carpeta de la aplicación. El nombre de la subcarpeta superior es una cadena de códigos de lenguaje DHTML que indica una referencia cultural de idioma o un idioma. La subcarpeta más profunda tiene el mismo nombre que el ensamblado.

La primera vez que realiza búsquedas en paralelo de un ensamblado privado, determina si existe una subcarpeta específica del lenguaje en la estructura de directorios de la aplicación. Si no existe ninguna subcarpeta específica del lenguaje, las búsquedas en paralelo del ensamblado privado se encuentran en las siguientes ubicaciones mediante la siguiente secuencia.

1.  En paralelo busca la carpeta WinSxS.
2.  \\\\< > \\ appdir < *AssemblyName* # C0.DLL
3.  \\\\< > \\ appdir < *assemblyname*>. manifest
4.  \\\\< > \\ appdir <  > \\ AssemblyName < *AssemblyName* # C0.DLL
5.  \\\\< > \\ appdir <  > \\ AssemblyName < *assemblyname*>. manifest

Si existe una subcarpeta específica del idioma, es posible que la estructura de directorios de la aplicación contenga el ensamblado privado localizado en varios idiomas. En paralelo busca en las subcarpetas específicas del lenguaje para asegurarse de que la aplicación usa el idioma especificado o el mejor idioma disponible. Las subcarpetas específicas del lenguaje se denominan mediante una cadena de códigos de lenguaje DHTML que especifican una referencia cultural de idioma o un idioma. Si existe una subcarpeta específica del lenguaje, en paralelo busca el ensamblado privado en las siguientes ubicaciones mediante la siguiente secuencia.

1.  En paralelo busca la carpeta WinSxS.
2.  \\\\< > \\ appdir < *referencia* > \\ cultural < de idioma *AssemblyName* # C0.DLL
3.  \\\\< > \\ appdir < *referencia* > \\ cultural < de idioma *assemblyname*>. manifest
4.  \\\\< > \\ appdir < *referencia* > \\ cultural < de idioma  > \\ AssemblyName < *AssemblyName* # C0.DLL
5.  \\\\< > \\ appdir < *referencia* > \\ cultural < de idioma  > \\ AssemblyName < *assemblyname*>. manifest

Tenga en cuenta que la secuencia de búsqueda en paralelo busca un archivo DLL con el nombre del ensamblado y se detiene antes de buscar un archivo de manifiesto con el nombre del ensamblado. La manera recomendada de controlar un ensamblado privado que es un archivo DLL es colocar el manifiesto del ensamblado en el archivo DLL como un recurso. El identificador de recurso debe ser igual a 1 y el nombre del ensamblado privado puede ser el mismo que el nombre del archivo DLL. Por ejemplo, si el nombre del archivo DLL es MICROSOFT.WINDOWS.MYSAMPLE.DLL, el valor del atributo name usado en el elemento **assemblyIdentity** del manifiesto del ensamblado también puede ser Microsoft. Windows. sample. Como alternativa, puede colocar el manifiesto del ensamblado en un archivo independiente; sin embargo, el nombre del ensamblado y su manifiesto deben ser distintos del nombre del archivo DLL. Por ejemplo, Microsoft. Windows. mysampleAsm, Microsoft. Windows. mysampleAsm. manifest y MICROSOFT.WINDOWS.MYSAMPLE.DLL.

Por ejemplo, si MyApp está instalado en la raíz de la unidad c: y requiere myasm en francés-belga, en paralelo utiliza la siguiente secuencia para buscar la mejor aproximación a una instancia localizada de myasm.

1.  Búsquedas en paralelo de WinSxS para la versión fr.
2.  c: \\ MyApp \\ fr: se \\myasm.dll
3.  c: \\ MyApp \\ fr-is \\ myasm. manifest
4.  c: \\ MyApp \\ fr-ser \\ myasm \\myasm.dll
5.  c: \\ MyApp \\ fr-is \\ myasm \\ myasm. manifest
6.  Búsquedas en paralelo de WinSxS para la versión fr.
7.  c: \\ MyApp \\ fr \\myasm.dll
8.  c: \\ MyApp \\ fr \\ myasm. manifest
9.  c: \\ MyApp \\ fr \\ myasm \\myasm.dll
10. c: \\ MyApp \\ fr \\ myasm \\ myasm. manifest
11. Búsquedas en paralelo de WinSxS para la versión en-US.
12. c: \\ MyApp \\ en-US \\myasm.dll
13. c: \\ MyApp \\ en-US \\ myasm. manifest
14. c: \\ MyApp \\ en-us \\ myasm \\myasm.dll
15. c: \\ MyApp \\ en-US \\ myasm \\ myasm. manifest
16. Búsquedas en paralelo de WinSxS para la versión en.
17. c: \\ MyApp \\ en \\myasm.dll
18. c: \\ MyApp \\ en \\ myasm. manifest
19. c: \\ MyApp \\ en \\ myasm \\myasm.dll
20. c: \\ MyApp \\ en \\ myasm \\ myasm. manifest
21. Las búsquedas en paralelo de WinSxS no tienen la versión de lenguaje.
22. c: \\ myapp \\myasm.dll
23. c: \\ MyApp \\ myasm. manifest
24. c: \\ MyApp \\ myasm \\myasm.dll
25. c: \\ MyApp \\ myasm \\ myasm. manifest

Si la búsqueda en paralelo alcanza una versión independiente del lenguaje del ensamblado, y una versión de la [interfaz de usuario multilingüe (MUI)](/windows/desktop/Intl/multilingual-user-interface) de Windows está presente en el sistema, en paralelo intenta enlazar a <*AssemblyName*>. MUI. En paralelo, no intenta enlazar a <*assemblyname*>. mui si la búsqueda alcanza una versión localizada del ensamblado. El [manifiesto del ensamblado](assembly-manifests.md) de un ensamblado independiente del lenguaje no tendrá un atributo Language en su elemento **assemblyIdentity** . Si en paralelo llega a un ensamblado independiente del lenguaje y se instala MUI, busca en paralelo las siguientes ubicaciones mediante la siguiente secuencia para <*assemblyname*>. MUI. En paralelo usa la misma secuencia de búsqueda si el ensamblado es independiente de la referencia cultural, excepto <no se busca en ningún> de *idioma* .

1.  En paralelo busca en la carpeta WinSxS <*assemblyname*>. MUI.
2.  \\\\<*referencia* > \\ cultural < del idioma del usuario *assemblyname*>. MUI
3.  \\\\< > idioma \\ del < usuario *assemblyname*>. MUI
4.  \\\\<*referencia* > \\ cultural < del idioma del sistema *assemblyname*>. MUI
5.  \\\\< > idioma \\ del < sistema *assemblyname*>. MUI
6.  \\\\<*sin* > \\ idioma < *assemblyname*>. MUI

Por ejemplo, si la búsqueda en paralelo encuentra el ensamblado privado en c: \\ MyApp \\ myasm \\ myasm. manifest y myasm es un ensamblado independiente del lenguaje. En paralelo, se usa la siguiente secuencia para buscar myasm. MUI. Tenga en cuenta que, en paralelo, no buscará un ensamblado MUI independiente del idioma.

1.  Búsquedas en paralelo de WinSxS para la versión fr del ensamblado MUI.
2.  c: \\ MyApp \\ fr: se \\myasm.mui.dll
3.  c: \\ MyApp \\ fr-is \\ myasm. MUI. manifest
4.  c: \\ MyApp \\ fr-ser \\ myasm \\myasm.mui.dll
5.  c: \\ MyApp \\ fr-is \\ myasm \\ myasm. MUI. manifest
6.  Búsquedas en paralelo de WinSxS para la versión fr del ensamblado MUI.
7.  c: \\ MyApp \\ fr \\myasm.mui.dll
8.  c: \\ MyApp \\ fr \\ myasm. MUI. manifest
9.  c: \\ MyApp \\ fr \\ myasm \\myasm.mui.dll
10. c: \\ MyApp \\ fr \\ myasm \\ myasm. MUI. manifest
11. Búsquedas en paralelo de WinSxS para la versión en-US del ensamblado MUI.
12. c: \\ MyApp \\ en-US \\myasm.mui.dll
13. c: \\ MyApp \\ en-US \\ myasm. MUI. manifest
14. c: \\ MyApp \\ en-us \\ myasm \\myasm.mui.dll
15. c: \\ MyApp \\ en-US \\ myasm \\ myasm. MUI. manifest
16. Búsquedas en paralelo de WinSxS para la versión en en el ensamblado MUI.
17. c: \\ MyApp \\ en \\myasm.mui.dll
18. c: \\ MyApp \\ en \\ myasm. MUI. manifest
19. c: \\ MyApp \\ en \\ myasm \\myasm.mui.dll
20. c: \\ MyApp \\ en \\ myasm \\ myasm. MUI. manifest

 

 
