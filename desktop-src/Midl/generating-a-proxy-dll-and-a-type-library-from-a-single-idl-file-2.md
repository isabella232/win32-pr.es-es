---
title: Generar un archivo DLL de proxy y una biblioteca de tipos a partir de un único archivo IDL
description: Puede usar un único archivo IDL para generar el código auxiliar de proxy y los archivos de encabezado para serializar código y una biblioteca de tipos.
ms.assetid: faa647ac-765a-45bd-8193-b6ea90d064ff
keywords:
- Lenguaje de definición de interfaz de Microsoft MIDL, tareas, generación de un archivo DLL de proxy y una biblioteca de tipos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a81001bba7aeff416e765291d3e6660b705919a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159573"
---
# <a name="generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file"></a>Generar un archivo DLL de proxy y una biblioteca de tipos a partir de un único archivo IDL

Puede usar un único archivo IDL para generar el código auxiliar de proxy y los archivos de encabezado para serializar código y una biblioteca de tipos. Para ello, defina una interfaz fuera del bloque de biblioteca y, a continuación, haga referencia a esa interfaz desde dentro del bloque de biblioteca, como se muestra en este ejemplo:

``` syntax
//file: AllKnown.idl

[
    object, uuid(. . .), <other interface attributes>
]
interface IKnown : IUnknown 
{
    import "unknwn.idl";
    <declarations, etc. for IKnown interface go here>
};

[
    <library attributes>
]
library KnownLibrary 
{

    //reference interface IKnown:
    interface IKnown;

    //or create a new class:
    [
        <coclass attributes>
    ] 
    coclass KnowMore 
    {
       interface IKnown;
    };
};
```

Para obtener más información, vea [Serializar tipos de datos OLE](marshaling-ole-data-types.md) y Archivos [adicionales necesarios para generar una biblioteca de tipos](additional-files-required-to-generate-a-type-library-2.md).

 

 




