---
title: Monikers de elementos
description: Otra clase de moniker implementada por OLE es el moniker de elemento, que se puede usar para identificar un objeto contenido en otro objeto.
ms.assetid: ddcf3669-4ad0-4a4e-80a6-eb78058cff09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57b692502ba44519a2c51a661ef62a51e133ac04
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359851"
---
# <a name="item-monikers"></a>Monikers de elementos

Otra clase de moniker implementada por OLE es el *moniker* de elemento , que se puede usar para identificar un objeto contenido en otro objeto. Un tipo de objeto contenido es un objeto OLE incrustado en un documento compuesto. Un documento compuesto podría identificar los objetos incrustados que contiene asignando a cada uno un nombre arbitrario, como "embedobj1", "embedobj2", etc. Otro tipo de objeto contenido es una selección de usuario en un documento, como un intervalo de celdas en una hoja de cálculo o un intervalo de caracteres en un documento de texto. Un objeto que consta de una selección se denomina *pseudo object* porque no se trata como un objeto distinto hasta que un usuario marca la selección. Una hoja de cálculo podría identificar un intervalo de celdas mediante un nombre como "1A:7F", mientras que un documento de procesamiento de palabras podría identificar un intervalo de caracteres mediante el nombre de un marcador.

Un moniker de elemento es útil principalmente cuando se concatena, o se *compone,* con otro moniker, que identifica el contenedor. Normalmente, se crea un moniker de elemento y, a continuación, se compone en (por ejemplo) un moniker de archivo para crear el equivalente de una ruta de acceso completa al objeto. Por ejemplo, puede crear el moniker de archivo "c: workreport.doc" (que identifica el objeto contenedor) con el moniker de elemento "embedobj1" (que identifica un objeto dentro del contenedor) para formar el \\ \\ moniker "c: \\ work \\report.doc\\ embedobj1", que identifica de forma única un objeto determinado dentro de un archivo determinado. También puede concatenar monikers de elementos adicionales para identificar objetos profundamente anidados. Por ejemplo, si "embedobj1" es el nombre de un objeto de hoja de cálculo, para identificar un determinado intervalo de celdas en ese objeto de hoja de cálculo, podría anexar otro moniker de elemento para crear un moniker que sería el equivalente de "c: \\ work \\report.doc\\ embedobj1 \\ 1A:7F".

Cuando se combina con un moniker de archivo, un moniker de elemento forma una ruta de acceso completa. Por lo tanto, los monikers de elementos amplían la noción de nombres de ruta de acceso más allá del sistema de archivos, definiendo nombres de ruta de acceso para identificar objetos individuales, no solo archivos.

Hay una diferencia significativa entre un moniker de elemento y un moniker de archivo. La ruta de acceso contenida en un moniker de archivo es significativa para cualquier persona que comprenda el sistema de archivos, mientras que la ruta de acceso parcial contenida en un moniker de elemento solo es significativa para un contenedor determinado. Todo el mundo sabe a qué hace referencia "c: workreport.doc", pero solo un objeto contenedor determinado sabe a qué hace referencia \\ \\ "1A:7F". Un contenedor no puede interpretar un moniker de elemento creado por otra aplicación; El único contenedor que sabe a qué objeto hace referencia un moniker de elemento es el contenedor que asignó el moniker de elemento al objeto en primer lugar. Por este motivo, el origen del objeto denominado por la combinación de un archivo y un moniker de elemento no solo debe implementar [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)para facilitar el enlace del moniker de archivo, sino también [**IOleItemContainer**](/windows/desktop/api/OleIdl/nn-oleidl-ioleitemcontainer) para facilitar la resolución del nombre del moniker de elemento en el objeto adecuado, en el contexto de un archivo.

La ventaja de los monikers es que alguien que usa un moniker para buscar un objeto no necesita comprender el nombre contenido en el moniker de elemento, siempre y cuando el moniker de elemento sea parte de un compuesto. Por lo general, no tendría sentido que un moniker de elemento existiera por sí solo. En su lugar, crearía un moniker de elemento en un moniker de archivo. A continuación, llamaría a [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) en la composición, que enlaza los monikers individuales dentro de él, interpretando los nombres.

Para crear un objeto de moniker de elemento y devolver su puntero al proveedor de moniker, OLE proporciona la función auxiliar [**CreateItemMoniker**](/windows/desktop/api/Objbase/nf-objbase-createitemmoniker). Esta función crea un objeto moniker de elemento y devuelve su puntero al proveedor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Anti monikers](anti-monikers.md)
</dt> <dt>

[Monikers de clase](class-monikers.md)
</dt> <dt>

[Monikers compuestos](composite-monikers.md)
</dt> <dt>

[Monikers de archivo](file-monikers.md)
</dt> <dt>

[Monikers de puntero](pointer-monikers.md)
</dt> </dl>

 

 




