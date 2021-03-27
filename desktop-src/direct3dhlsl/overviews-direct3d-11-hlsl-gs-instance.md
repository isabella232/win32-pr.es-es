---
title: Cómo instanciar un sombreador de geometría
description: La creación de instancias del sombreador de geometría permite que se ejecuten varias ejecuciones del mismo sombreador de geometría por primitiva.
ms.assetid: e3d8616b-7129-40e9-99fc-2852914a80b0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7858de7d8526a9468d3ebd0a07d57777983a66db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104996788"
---
# <a name="how-to-instance-a-geometry-shader"></a>Cómo: instanciar un sombreador de geometría

La creación de instancias del sombreador de geometría permite que se ejecuten varias ejecuciones del mismo sombreador de geometría por primitiva. Para instanciar un sombreador de geometría, agregue un atributo de instancia a la función de sombreador principal e identifique un parámetro de índice de instancia en el cuerpo de la función de sombreador.

Para instanciar un sombreador de geometría:

1.  Agregue el [atributo de instancia](sm5-attributes-instance.md) a la función main.

    ```
    [instance(24)]
    ```

    

    Define el número de instancias (un máximo de 32) que se va a ejecutar para cada primitiva.

2.  Adjunte el valor del sistema [VP \_ GSInstanceID](sv-gsinstanceid.md) a una variable de la lista de parámetros de función que se puede usar para realizar el seguimiento del identificador de la instancia que se está ejecutando.
    ```
    uint InstanceID : SV_GSInstanceID
    ```

    

3.  Compile y cree el sombreador tal como lo haría con cualquier otro sombreador de geometría.

Otros detalles incluyen:

-   El recuento máximo de instancias es 32.
-   El número máximo de vértices es un recuento máximo de vértices por instancia.
-   Cada invocación de instancia (como cualquier invocación del sombreador de geometría) aumenta el recuento de invocación y genera una RestartStrip implícita ().

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Características del sombreador de geometría](overviews-direct3d-11-hlsl-gs-features.md)
</dt> </dl>

 

 




