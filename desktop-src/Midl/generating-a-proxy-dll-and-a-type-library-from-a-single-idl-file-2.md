---
title: Generar un archivo DLL de proxy y una biblioteca de tipos a partir de un único archivo IDL
description: Puede usar un único archivo IDL para generar los archivos de encabezado y los códigos auxiliares de proxy para serializar código y una biblioteca de tipos.
ms.assetid: faa647ac-765a-45bd-8193-b6ea90d064ff
keywords:
- Lenguaje de definición de interfaz de Microsoft MIDL, tareas, generación de un archivo DLL de proxy y una biblioteca de tipos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92e7bf2694b791007b0f1da303525217cf55d75d574e083c6d1756bc2784d0ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384241"
---
# <a name="generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file"></a>Generar un archivo DLL de proxy y una biblioteca de tipos a partir de un único archivo IDL

Puede usar un único archivo IDL para generar los archivos de encabezado y los códigos auxiliares de proxy para serializar código y una biblioteca de tipos. Para ello, defina una interfaz fuera del bloque de biblioteca y, a continuación, haga referencia a esa interfaz desde dentro del bloque de biblioteca, como se muestra en este ejemplo:

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

Para obtener más información, vea [Serializar tipos de datos OLE](marshaling-ole-data-types.md) y archivos [adicionales necesarios para generar una biblioteca de tipos.](additional-files-required-to-generate-a-type-library-2.md)

 

 




