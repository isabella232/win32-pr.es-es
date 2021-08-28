---
description: Si una aplicación aislada especifica una dependencia de ensamblado, primero busca en paralelo el ensamblado entre los ensamblados compartidos de la carpeta WinSxS.
ms.assetid: 93496631-55cc-4dd9-9a51-b748c35fd477
title: Secuencia de búsqueda de ensamblados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 983466954d6cb9619d3fb0595c96f81fed7c9b73a29bfbf2f609b3f14203a957
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127545"
---
# <a name="assembly-searching-sequence"></a>Secuencia de búsqueda de ensamblados

Si una aplicación aislada especifica una dependencia de ensamblado, primero busca [](/windows/desktop/Msi/shared-assemblies) en paralelo el ensamblado entre los ensamblados compartidos de la carpeta WinSxS. Si no se encuentra el ensamblado necesario, busca en paralelo un ensamblado privado instalado en una carpeta de la estructura de directorios de la aplicación.

[Los ensamblados privados](/windows/desktop/Msi/private-assemblies) se pueden implementar en las siguientes ubicaciones de la estructura de directorios de la aplicación:

-   En la carpeta de la aplicación. Normalmente, esta es la carpeta que contiene el archivo ejecutable de la aplicación.
-   En una subcarpeta de la carpeta de la aplicación. La subcarpeta debe tener el mismo nombre que el ensamblado.
-   En una subcarpeta específica del idioma de la carpeta de la aplicación. El nombre de la subcarpeta es una cadena de códigos de idioma DHTML que indican un idioma o referencia cultural del idioma.
-   En una subcarpeta de una subcarpeta específica del idioma en la carpeta de la aplicación. El nombre de la subcarpeta superior es una cadena de códigos de idioma DHTML que indican un idioma o referencia cultural del idioma. La subcarpeta más profunda tiene el mismo nombre que el ensamblado.

La primera vez que busca en paralelo un ensamblado privado, determina si existe una subcarpeta específica del lenguaje en la estructura de directorios de la aplicación. Si no existe ninguna subcarpeta específica del lenguaje, busca en paralelo el ensamblado privado en las siguientes ubicaciones mediante la secuencia siguiente.

1.  En paralelo, busca en la carpeta WinSxS.
2.  \\\\< > \\ appdir < *assemblyname*>.DLL
3.  \\\\< > \\ appdir < *assemblyname*>.manifest
4.  \\\\< > \\ appdir <  > \\ assemblyname < *assemblyname*>.DLL
5.  \\\\< > \\ appdir <  > \\ assemblyname < *assemblyname*>.manifest

Si existe una subcarpeta específica del idioma, la estructura de directorios de la aplicación puede contener el ensamblado privado localizado en varios idiomas. En paralelo, busca en las subcarpetas específicas del idioma para asegurarse de que la aplicación usa el idioma especificado o el mejor idioma disponible. Las subcarpetas específicas del idioma se denominan mediante una cadena de códigos de idioma DHTML que especifican un idioma o referencia cultural del idioma. Si existe una subcarpeta específica del lenguaje, busca en paralelo el ensamblado privado en las siguientes ubicaciones mediante la secuencia siguiente.

1.  En paralelo, busca en la carpeta WinSxS.
2.  \\\\< > \\ appdir < *language-culture* > \\ < *assemblyname*>.DLL
3.  \\\\< > \\ appdir < *language-culture* > \\ < *assemblyname*>.manifest
4.  \\\\< > \\ appdir < *language-culture* > \\ <  > \\ assemblyname < *assemblyname*>.DLL
5.  \\\\< > \\ appdir < *language-culture* > \\ <  > \\ assemblyname < *assemblyname*>.manifest

Tenga en cuenta que la secuencia de búsqueda en paralelo busca un archivo DLL con el nombre del ensamblado y se detiene antes de buscar un archivo de manifiesto que tenga el nombre del ensamblado. La manera recomendada de controlar un ensamblado privado que es un archivo DLL es colocar el manifiesto de ensamblado en el archivo DLL como un recurso. El identificador de recurso debe ser igual a 1 y el nombre del ensamblado privado puede ser el mismo que el nombre del archivo DLL. Por ejemplo, si el nombre del archivo DLL es MICROSOFT.WINDOWS.MYSAMPLE.DLL, el valor del atributo name usado en el elemento **assemblyIdentity** del manifiesto del ensamblado también puede ser Microsoft. Windows.mysample. Como alternativa, puede colocar el manifiesto del ensamblado en un archivo independiente; sin embargo, el nombre del ensamblado y su manifiesto deben ser diferentes del nombre del archivo DLL. Por ejemplo, Microsoft. Windows.mysampleAsm, Microsoft. Windows.mysampleAsm.manifest y MICROSOFT.WINDOWS.MYSAMPLE.DLL.

Por ejemplo, si myapp se instala en la raíz de la unidad c: y requiere myasm en francés-Desaprobación, en paralelo usa la secuencia siguiente para buscar la mejor aproximación a una instancia localizada de myasm.

1.  En paralelo, busca en WinSxS la versión fr-be.
2.  c: \\ myapp \\ fr-be \\myasm.dll
3.  c: \\ myapp \\ fr-be \\ myasm.manifest
4.  c: \\ myapp \\ fr-be \\ myasm \\myasm.dll
5.  c: \\ myapp \\ fr-be \\ myasm \\ myasm.manifest
6.  En paralelo, busca WinSxS en la versión fr.
7.  c: \\ myapp \\ fr \\myasm.dll
8.  c: \\ myapp \\ fr \\ myasm.manifest
9.  c: \\ myapp \\ fr \\ myasm \\myasm.dll
10. c: \\ myapp \\ fr \\ myasm \\ myasm.manifest
11. En paralelo, busca en WinSxS la versión en-us.
12. c: \\ myapp \\ en-us \\myasm.dll
13. c: \\ myapp \\ en-us \\ myasm.manifest
14. c: \\ myapp \\ en-us \\ myasm \\myasm.dll
15. c: \\ myapp \\ en-us \\ myasm \\ myasm.manifest
16. En paralelo, busca WinSxS en la versión en .
17. c: \\ myapp \\ en \\myasm.dll
18. c: \\ myapp \\ en \\ myasm.manifest
19. c: \\ myapp \\ en \\ myasm \\myasm.dll
20. c: \\ myapp \\ en \\ myasm \\ myasm.manifest
21. En paralelo, busca en WinSxS la versión sin idioma.
22. c: \\ myapp \\myasm.dll
23. c: \\ myapp \\ myasm.manifest
24. c: \\ myapp \\ myasm \\myasm.dll
25. c: \\ myapp \\ myasm \\ myasm.manifest

Si la búsqueda en paralelo alcanza una versión sin idioma del ensamblado y hay una versión [multilenguaje Interfaz de usuario (MUI)](/windows/desktop/Intl/multilingual-user-interface) de Windows en el sistema, en paralelo intenta enlazar *<* un nombre de ensamblado>.mui. En paralelo, no intenta enlazar a <*assemblyname*>.mui si la búsqueda alcanza una versión localizada del ensamblado. El [manifiesto de](assembly-manifests.md) ensamblado de un ensamblado neutral del lenguaje no tendrá un atributo de lenguaje en su elemento **assemblyIdentity.** Si llega en paralelo a un ensamblado con idioma neutro y se instala MUI, busca en paralelo las siguientes ubicaciones mediante la siguiente secuencia para <*assemblyname*>.mui. En paralelo, usa la misma secuencia de búsqueda si el ensamblado es neutral en la referencia cultural, excepto <*no* se busca ningún> idioma.

1.  En paralelo, busca en la carpeta WinSxS <*assemblyname*>.mui.
2.  \\\\<*idioma-referencia cultural del usuario* > \\ < *assemblyname*>.mui
3.  \\\\<*idioma del usuario* > \\ < *assemblyname*>.mui
4.  \\\\<*idioma-referencia cultural del sistema* > \\ < *assemblyname*>.mui
5.  \\\\<*idioma del sistema* > \\ < *assemblyname*>.mui
6.  \\\\<*sin idioma* > \\ < *assemblyname*>.mui

Por ejemplo, si la búsqueda en paralelo encuentra el ensamblado privado en c: \\ myapp \\ myasm \\ myasm.manifest y myasm es un ensamblado neutral del lenguaje. A continuación, en paralelo, usa la siguiente secuencia para buscar myasm.mui. Tenga en cuenta que, en paralelo, no buscará un ensamblado DE BLOC neutro en el lenguaje.

1.  En paralelo, busca en WinSxS la versión fr-be del ensamblado DE LAA.
2.  c: \\ myapp \\ fr-be \\myasm.mui.dll
3.  c: \\ myapp \\ fr-be \\ myasm.mui.manifest
4.  c: \\ myapp \\ fr-be \\ myasm \\myasm.mui.dll
5.  c: \\ myapp \\ fr-be \\ myasm \\ myasm.mui.manifest
6.  En paralelo, busca en WinSxS la versión fr del ensamblado DE LA.
7.  c: \\ myapp \\ fr \\myasm.mui.dll
8.  c: \\ myapp \\ fr \\ myasm.mui.manifest
9.  c: \\ myapp \\ fr \\ myasm \\myasm.mui.dll
10. c: \\ myapp \\ fr \\ myasm \\ myasm.mui.manifest
11. En paralelo, busca en WinSxS la versión en-us del ensamblado DEI.
12. c: \\ myapp \\ en-us \\myasm.mui.dll
13. c: \\ myapp \\ en-us \\ myasm.mui.manifest
14. c: \\ myapp \\ en-us \\ myasm \\myasm.mui.dll
15. c: \\ myapp \\ en-us \\ myasm \\ myasm.mui.manifest
16. En paralelo, busca en WinSxS la versión en del ensamblado DEA.
17. c: \\ myapp \\ en \\myasm.mui.dll
18. c: \\ myapp \\ en \\ myasm.mui.manifest
19. c: \\ myapp \\ en \\ myasm \\myasm.mui.dll
20. c: \\ myapp \\ en \\ myasm \\ myasm.mui.manifest

 

 
