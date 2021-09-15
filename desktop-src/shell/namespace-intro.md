---
description: Obtenga información sobre el espacio de nombres de Shell y sus objetos de origen de datos. Este espacio de nombres ofrece opciones de extensibilidad en la interfaz Windows Shell.
ms.assetid: 539c4455-e1c7-45a0-b3c3-781f2b7a1617
title: Introducción al espacio de nombres del shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e1be0187094ffe7cf7b56b724c5990fe18321fa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360362"
---
# <a name="introduction-to-the-shell-namespace"></a>Introducción al espacio de nombres del shell

El espacio *de nombres shell* organiza el sistema de archivos y otros objetos administrados por shell en una única jerarquía estructurada en árbol. Conceptualmente, es una versión más grande e inclusiva del sistema de archivos.

-   [Introducción](#introduction)
-   [Identificar objetos de espacio de nombres](#identifying-namespace-objects)
    -   [IDs de elemento](#item-ids)
    -   [Listas de identificadores de elemento](#item-id-lists)
    -   [PIDL](#pidls)
    -   [Asignación de PIDL](#allocating-pidls)

## <a name="introduction"></a>Introducción

Una de las principales responsabilidades del Shell es administrar y proporcionar acceso a la amplia variedad de objetos que la conste. Los objetos más numerosos y conocidos son las carpetas y archivos que residen en unidades de disco del equipo. Sin embargo, shell también administra varios sistemas  que no son archivos o objetos virtuales. Estos son algunos ejemplos:

-   Impresoras de red
-   Otros equipos en red
-   Panel de control aplicaciones
-   La Papelera de reciclaje

Algunos objetos virtuales no implican almacenamiento físico en absoluto. Por ejemplo, el objeto de impresora contiene una colección de vínculos a impresoras en red. Otros objetos virtuales, como papelera de reciclaje, pueden contener datos almacenados en una unidad de disco, pero deben controlarse de forma diferente a los archivos normales. Por ejemplo, se puede usar un objeto virtual para representar los datos almacenados en una base de datos. En cuanto al espacio de nombres , los distintos elementos de la base de datos podrían aparecer en el Explorador de Windows como objetos independientes, aunque todos se almacenen en un único archivo de disco.

Los objetos virtuales incluso pueden encontrarse en equipos remotos. Por ejemplo, para facilitar la itinerancia, los archivos de documento de un usuario pueden almacenarse en un servidor. Para proporcionar a los usuarios acceso a sus archivos desde varios equipos de escritorio, la carpeta Mis documentos del equipo de escritorio que usa actualmente apuntará al servidor, no al disco duro del equipo de escritorio. Su ruta de acceso incluirá una unidad de red asignada o un nombre de ruta de acceso UNC.

Al igual que el sistema de archivos, el espacio de nombres incluye dos tipos básicos de objeto: carpetas y archivos. Los objetos de carpeta son *los nodos* del árbol; son contenedores para objetos de archivo y otras carpetas. Los objetos de archivo son *las hojas* del árbol; son archivos de disco normales u objetos virtuales, como vínculos de impresora. Las carpetas que no forman parte del sistema de archivos a veces se conocen como *carpetas virtuales.*

Al igual que las carpetas del sistema de archivos, la colección de carpetas virtuales suele variar de un sistema a otro. Hay tres clases de carpetas virtuales:

-   Carpetas virtuales estándar, como la papelera de reciclaje, que se encuentran en todos los sistemas.
-   Carpetas virtuales opcionales que tienen nombres y funcionalidades estándar, pero que pueden no estar presentes en todos los sistemas.
-   Carpetas no estándar instaladas por el usuario.

A diferencia de las carpetas del sistema de archivos, los usuarios no pueden crear carpetas virtuales. Solo pueden instalar los creados por desarrolladores que no son de Microsoft. Por lo tanto, el número de carpetas virtuales suele ser mucho menor que el número de carpetas del sistema de archivos. Para obtener una explicación sobre cómo implementar carpetas virtuales, vea [Extensiones de espacio de nombres](nse-works.md).

Puede ver una representación visual de cómo se estructura el espacio de nombres en la barra del explorador de Windows Explorer. Por ejemplo, la siguiente captura de pantalla de Windows Explorer muestra un espacio de nombres relativamente sencillo.

![una vista del espacio de nombres del shell](images/prog1.png)

La raíz final de la jerarquía de espacios de nombres es el escritorio. Inmediatamente debajo de la raíz hay varias carpetas virtuales, como Mi PC y el papelera de reciclaje.

Se puede ver que los sistemas de archivos de las distintas unidades de disco son subconjuntos de la jerarquía de espacios de nombres más grande. Las raíces de estos sistemas de archivos son subcarpetas de la carpeta Mi PC archivos. Mi PC también incluye las raíces de las unidades de red asignadas. Otros nodos del árbol, como Mis documentos, son carpetas virtuales.

## <a name="identifying-namespace-objects"></a>Identificar objetos de espacio de nombres

Para poder usar un objeto de espacio de nombres, primero debe tener una manera de identificarlo. Un objeto del sistema de archivos podría tener un nombre como MyFile.htm. Dado que puede haber otros archivos con ese nombre en otra parte del sistema, la identificación única de un archivo o carpeta requiere una ruta de acceso completa como "C: \\ MyDocs \\MyFile.htm". Esta ruta de acceso es básicamente una lista ordenada de todas las carpetas de una ruta de acceso de la raíz del sistema de archivos, C: \\ , que termina con el archivo.

En el contexto del espacio de nombres , las rutas de acceso siguen siendo bastante útiles para identificar objetos ubicados en la parte del sistema de archivos del espacio de nombres . Sin embargo, no se pueden usar para objetos virtuales. En su lugar, shell proporciona un medio alternativo de identificación que se puede usar con cualquier objeto de espacio de nombres.

### <a name="item-ids"></a>IDs de elemento

Dentro de una carpeta, cada objeto tiene un identificador *de elemento*, que es el equivalente funcional de un nombre de archivo o carpeta. El identificador de elemento es en realidad [**una estructura DE LA ESTRUCTURA DE LA PROPIEDAD:**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid)


```
typedef struct _SHITEMID { 
    USHORT cb; 
    BYTE   abID[1]; 
} SHITEMID, * LPSHITEMID; 
```



El **miembro abID** es el identificador del objeto. La longitud **de abID** no está definida y su valor viene determinado por la carpeta que contiene el objeto . Dado que no hay ninguna definición estándar de cómo las carpetas asignan los valores **abID,** solo son significativos para el objeto de carpeta asociado. Las aplicaciones simplemente deben tratarlas como un token que identifica un objeto en una carpeta determinada. Dado que la longitud **de abID** varía, el **miembro cb** contiene el tamaño de la estructura [**DESUSDAD,**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) en bytes.

Dado que los ID de elemento no son útiles para mostrar, la carpeta que contiene el objeto normalmente le asigna un nombre para mostrar. Este es el nombre que usa Windows Explorer cuando muestra el contenido de una carpeta. Para obtener más información sobre cómo se controlan los nombres para mostrar, vea [Obtener información de una carpeta](folder-info.md).

### <a name="item-id-lists"></a>Listas de identificadores de elemento

El identificador de elemento rara vez se usa por sí mismo. Normalmente, forma parte de una lista de identificadores de elemento, que tiene el mismo propósito que una ruta de acceso del sistema de archivos. Sin embargo, en lugar de la cadena de caracteres utilizada para las rutas de acceso, una lista de identificadores de elemento es una [**estructura ITEMIDLIST.**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) Esta estructura es una secuencia ordenada de uno o varios IDs de elemento, terminados por un VALOR NULL de **dos bytes.** Cada identificador de elemento de la lista de identificadores de elemento corresponde a un objeto de espacio de nombres. Su orden define una ruta de acceso en el espacio de nombres, de forma muy parecido a una ruta de acceso del sistema de archivos.

En la ilustración siguiente se muestra una representación esquemática de la [**estructura ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) que corresponde a C: \\ MyDocs \\MyFile.htm. El nombre para mostrar de cada identificador de elemento se muestra encima de él. Los anchos variables de los **miembros abID** son arbitrarios; ilustran el hecho de que el tamaño de este miembro puede variar.

![ilustración esquemática de un pidl](images/shell2.png)

### <a name="pidls"></a>PIDL

Para shell API, los objetos de espacio de nombres normalmente se identifican mediante un puntero a su [**estructura ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) o un puntero a una lista de identificadores de elemento (PIDL). Para mayor comodidad, el término PIDL generalmente hará referencia en esta documentación a la propia estructura en lugar del puntero a ella.

El PIDL que se muestra en la ilustración anterior se conoce como PIDL completo o absoluto. Un PIDL completo comienza desde el escritorio y contiene los iDs de elemento de todas las carpetas intermedias de la ruta de acceso. Termina con el identificador de elemento del objeto seguido de un null de dos bytes de **terminación.** Un PIDL completo es similar a una ruta de acceso completa e identifica de forma única el objeto en el espacio de nombres de Shell.

Los PIDL completos se usan con poca frecuencia. Muchas funciones y métodos esperan un *PIDL relativo.* La raíz de un PIDL relativo es una carpeta, no el escritorio. Al igual que con las rutas de acceso relativas, la serie de identificadores de elemento que la estructura define una ruta de acceso en el espacio de nombres entre dos objetos. Aunque no identifican de forma única el objeto, suelen ser más pequeños que un PIDL completo y suficientes para muchos propósitos.

Los PIDL relativos más usados, los *PIDL* de un solo nivel, son relativos a la carpeta primaria del objeto. Contienen solo el identificador de elemento del objeto y un valor **NULL de terminación.** Los PIDL de varios niveles también se usan para muchos fines. Contienen dos o más iDs de elemento y normalmente definen una ruta de acceso de una carpeta primaria a un objeto a través de una serie de una o varias subcarpetas. Tenga en cuenta que un PIDL de un solo nivel todavía puede ser un PIDL completo. En concreto, los objetos de escritorio son elementos secundarios del escritorio, por lo que sus PIDL completos contienen solo un identificador de elemento.

Como se describe en [Obtención](folder-id.md)del identificador de una carpeta, la API de Shell proporciona varias maneras de recuperar el PIDL de un objeto. Una vez que lo tenga, normalmente solo lo usará para identificar el objeto cuando llame a otras funciones y métodos de la API de Shell. En este contexto, el contenido interno de un PIDL es opaco e irrelevante. Para los fines de esta discusión, piense en los PIDL como tokens que representan objetos de espacio de nombres determinados y céntrate en cómo usarlos para tareas comunes.

### <a name="allocating-pidls"></a>Asignación de PIDL

Aunque los PIDL tienen cierta similitud con las rutas de acceso, su uso requiere un enfoque algo diferente. La principal diferencia radica en cómo asignar y desasignar memoria para ellos.

Al igual que la cadena utilizada para una ruta de acceso, se debe asignar memoria para un PIDL. Si una aplicación crea un PIDL, debe asignar suficiente memoria para la [**estructura ITEMIDLIST.**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) En la mayoría de los casos aquí analizados, el shell crea el PIDL y controla la asignación de memoria. Independientemente de lo que haya asignado el PIDL, la aplicación suele ser responsable de desasignar el PIDL cuando ya no sea necesario.

Use la [**función CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) para asignar el PIDL y la [**función CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para desasignarla.

 

 
