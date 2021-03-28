---
description: El espacio de nombres de Shell organiza el sistema de archivos y otros objetos administrados por el Shell en una única jerarquía estructurada por árbol. Conceptualmente, es una versión más grande y más inclusiva del sistema de archivos.
title: Conceptos comunes del explorador
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 78136c36-bd3c-4114-8b69-fef4e307566d
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d5ea7d154ef0455576d91f99eb53dccd93c25339
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550757"
---
# <a name="common-explorer-concepts"></a>Conceptos comunes del explorador

El *espacio de nombres* de Shell organiza el sistema de archivos y otros objetos administrados por el Shell en una única jerarquía estructurada por árbol. Conceptualmente, es una versión más grande y más inclusiva del sistema de archivos.

-   [Introducción](#introduction)
-   [Identificar objetos de espacio de nombres](#identifying-namespace-objects)
    -   [Identificadores de elemento](#item-ids)
    -   [Listas de ID. de elemento](#item-id-lists)
    -   [PIDL](#pidls)
    -   [Asignar PIDL](#allocating-pidls)

## <a name="introduction"></a>Introducción

Una de las principales responsabilidades del shell es la administración y el acceso a la amplia variedad de objetos que componen el sistema. El más conocido de estos objetos son las carpetas y los archivos que residen en las unidades de disco del equipo. Sin embargo, el shell administra también una serie de sistemas que no son de archivos, o de objetos *virtuales* . Estos son algunos ejemplos:

-   Impresoras de red
-   Otros equipos conectados en red
-   Aplicaciones del panel de control
-   La Papelera de reciclaje

Algunos objetos virtuales no implican almacenamiento físico. Por ejemplo, el objeto Printer contiene una colección de vínculos a las impresoras en red. Otros objetos virtuales, como la papelera de reciclaje, pueden contener datos que se almacenan en una unidad de disco, pero deben tratarse de forma diferente a los archivos normales. Por ejemplo, se puede utilizar un objeto virtual para representar los datos almacenados en una base de datos. En términos del espacio de nombres, los distintos elementos de la base de datos podrían aparecer en el explorador de Windows como objetos independientes, aunque todos se almacenan en un único archivo de disco.

Los objetos virtuales se pueden encontrar incluso en equipos remotos. Por ejemplo, para facilitar la itinerancia, los archivos de documento de un usuario se pueden almacenar en un servidor. Para conceder a los usuarios acceso a sus archivos desde varios equipos de escritorio, la carpeta Mis documentos del equipo de escritorio que usa actualmente apuntará al servidor, no al disco duro del equipo de escritorio. Su ruta de acceso incluirá una unidad de red asignada o un nombre de ruta de acceso UNC.

Al igual que el sistema de archivos, el espacio de nombres incluye dos tipos básicos de objeto: carpetas y archivos. Los objetos de carpeta son los *nodos* del árbol; son contenedores de objetos de archivo y otras carpetas. Los objetos de archivo son las *hojas* del árbol; son archivos de disco normales u objetos virtuales, como vínculos de impresora. Las carpetas que no forman parte del sistema de archivos se denominan a veces *carpetas virtuales*.

Al igual que las carpetas del sistema de archivos, la colección de carpetas virtuales suele variar de un sistema a sistema. Hay tres clases de carpetas virtuales:

-   Carpetas virtuales estándar, como la papelera de reciclaje, que se encuentran en todos los sistemas.
-   Carpetas virtuales opcionales que tienen nombres y funciones estándar, pero que pueden no estar presentes en todos los sistemas.
-   Carpetas no estándar instaladas por el usuario.

A diferencia de las carpetas del sistema de archivos, los usuarios no pueden crear nuevas carpetas virtuales. Solo pueden instalar los creados por desarrolladores que no sean de Microsoft. Por lo tanto, el número de carpetas virtuales es normalmente mucho menor que el número de carpetas del sistema de archivos. Para obtener una explicación sobre cómo implementar carpetas virtuales, vea [extensiones de espacio de nombres](nse-works.md).

Puede ver una representación visual de cómo se estructura el espacio de nombres en la barra del explorador de Windows. Por ejemplo, la siguiente captura de pantalla del explorador de Windows muestra un espacio de nombres relativamente simple.

![captura de pantalla que muestra una vista del espacio de nombres del shell](images/prog1.png)

La raíz Ultimate de la jerarquía de espacios de nombres es el escritorio. Justo debajo de la raíz hay varias carpetas virtuales como Mi PC y la papelera de reciclaje.

Los sistemas de archivos de las distintas unidades de disco se pueden considerar como subconjuntos de la jerarquía de espacios de nombres más grande. Las raíces de estos sistemas de archivos son las subcarpetas de la carpeta Mi PC. Mi PC también incluye las raíces de las unidades de red asignadas. Otros nodos del árbol, como mis documentos, son carpetas virtuales.

## <a name="identifying-namespace-objects"></a>Identificar objetos de espacio de nombres

Antes de poder usar un objeto de espacio de nombres, primero debe tener una forma de identificarlo. Un objeto del sistema de archivos podría tener un nombre como MyFile.htm. Dado que puede haber otros archivos con ese nombre en otra parte del sistema, la identificación exclusiva de un archivo o una carpeta requiere una ruta de acceso completa como "C: mis \\ documentos \\MyFile.htm". Esta ruta de acceso es básicamente una lista ordenada de todas las carpetas de una ruta de acceso desde la raíz del sistema de archivos, C: \\ , que termina con el archivo.

En el contexto del espacio de nombres, las rutas de acceso siguen siendo bastante útiles para identificar los objetos ubicados en la parte del sistema de archivos del espacio de nombres. Sin embargo, no se pueden usar para objetos virtuales. En su lugar, el Shell proporciona un medio alternativo de identificación que se puede utilizar con cualquier objeto de espacio de nombres.

### <a name="item-ids"></a>Identificadores de elemento

Dentro de una carpeta, cada objeto tiene un *identificador de elemento*, que es el equivalente funcional de un nombre de archivo o carpeta. El ID. de elemento es realmente una estructura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) :


```
typedef struct _SHITEMID { 
    USHORT cb; 
    BYTE   abID[1]; 
} SHITEMID, * LPSHITEMID;
```



El miembro **atenerse** es el identificador del objeto. No **se ha definido la longitud de la** función y la carpeta que contiene el objeto determina su valor. Dado que no hay ninguna definición estándar para **el modo en** que las carpetas asignan los valores, solo son significativos para el objeto de carpeta asociado. Las aplicaciones deben tratarlas simplemente como un token que identifique un objeto en una carpeta determinada. Dado que la longitud de **acatar** varía, el miembro **CB** contiene el tamaño de la estructura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) , en bytes.

Dado que los identificadores de elemento no son útiles para la presentación, la carpeta que contiene el objeto normalmente le asigna un nombre para mostrar. Este es el nombre que utiliza el explorador de Windows cuando muestra el contenido de una carpeta. Para obtener más información sobre cómo se administran los nombres para mostrar, vea [obtener información de una carpeta](folder-info.md).

### <a name="item-id-lists"></a>Listas de ID. de elemento

El ID. del elemento rara vez se usa por sí mismo. Normalmente, forma parte de una lista de ID. de elemento, que sirve para el mismo propósito que una ruta de acceso del sistema de archivos. Sin embargo, en lugar de la cadena de caracteres que se usa para las rutas de acceso, una lista de ID. de elemento es una estructura [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) . Esta estructura es una secuencia ordenada de uno o varios identificadores de elemento, terminada por un **valor null** de dos bytes. Cada identificador de elemento de la lista de ID. de elemento corresponde a un objeto de espacio de nombres. Su orden define una ruta de acceso en el espacio de nombres, de forma similar a una ruta de acceso del sistema de archivos.

En la ilustración siguiente se muestra una representación esquemática de la estructura [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) que corresponde a C: mis \\ documentos \\MyFile.htm. El nombre para mostrar de cada identificador de elemento se muestra encima. Los distintos anchos de los miembros de **respetar** son arbitrarios; ilustran el hecho de que el tamaño de este miembro puede variar.

![Ilustración esquemática de un PIDL](images/shell2.png)

### <a name="pidls"></a>PIDL

En el caso de la API de Shell, los objetos de espacio de nombres normalmente se identifican mediante un puntero a su estructura [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) o un puntero a una lista de identificadores de elementos (PIDL). Para mayor comodidad, el término PIDL generalmente hará referencia en esta documentación a la propia estructura, en lugar de al puntero.

Los PIDL que se muestran en la ilustración anterior se conocen como PIDL *completos* o *absolutos*. Un PIDL completo se inicia desde el escritorio y contiene los identificadores de elemento de todas las carpetas intermedias de la ruta de acceso. Finaliza con el identificador de elemento del objeto seguido de un **null** de dos bytes de terminación. Un PIDL completo es similar a una ruta de acceso completa y identifica de forma única el objeto en el espacio de nombres del shell.

Los PIDL completos no se usan con frecuencia. Muchas funciones y métodos esperan un *PIDL relativo*. La raíz de un PIDL relativo es una carpeta, no el escritorio. Al igual que con las rutas de acceso relativas, la serie de identificadores de elemento que componen la estructura define una ruta de acceso en el espacio de nombres entre dos objetos. Aunque no identifican el objeto de forma exclusiva, suelen ser más pequeñas que un PIDL completo y suficientes para muchos propósitos.

La PIDL relativa más utilizada, *PIDL de un solo nivel*, son relativas a la carpeta principal del objeto. Contienen solo el identificador de elemento del objeto y un carácter **nulo** de terminación. Los PIDL de varios niveles también se usan para muchos propósitos. Contienen dos o más identificadores de elemento y, por lo general, definen una ruta de acceso de una carpeta primaria a un objeto a través de una serie de una o varias subcarpetas. Tenga en cuenta que un PIDL de un solo nivel puede seguir siendo PIDL completo. En concreto, los objetos de escritorio son elementos secundarios del escritorio, por lo que sus PIDL completos solo contienen un identificador de elemento.

Como se describe en [obtener el identificador de una carpeta](folder-id.md), la API de Shell proporciona varias maneras de recuperar el PIDL de un objeto. Una vez que lo haya hecho, normalmente solo se usa para identificar el objeto cuando se llama a otras funciones y métodos de la API de Shell. En este contexto, el contenido interno de un PIDL es opaco e irrelevante. Para los fines de este debate, piense en PIDL como tokens que representan objetos de espacio de nombres concretos y céntrese en cómo usarlos para tareas comunes.

### <a name="allocating-pidls"></a>Asignar PIDL

Aunque PIDL tienen cierta similitud con las rutas de acceso, el uso de ellas requiere un enfoque algo diferente. La principal diferencia radica en cómo asignar y desasignar memoria para ellos.

Al igual que la cadena usada para una ruta de acceso, se debe asignar memoria para un PIDL. Si una aplicación crea un PIDL, debe asignar suficiente memoria para la estructura [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) . Para la mayoría de los casos descritos aquí, el shell crea PIDL y controla la asignación de memoria. Independientemente de lo que haya asignado el PIDL, la aplicación suele ser responsable de desasignar el PIDL cuando ya no se necesita.

Use la función [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) para asignar el PIDL y la función [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para desasignarlo.

 

 
