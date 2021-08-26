---
title: Cómo crear instancias de un sombreador de geometría
description: La creación de instancias del sombreador de geometría permite ejecutar varias ejecuciones del mismo sombreador de geometría por primitiva.
ms.assetid: e3d8616b-7129-40e9-99fc-2852914a80b0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 866b0cedb4de0fe2f8bf9087df6637d3a6340505289b4b773eaccd380fa4b367
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067925"
---
# <a name="how-to-instance-a-geometry-shader"></a>Cómo: Crear instancias de un sombreador de geometría

La creación de instancias del sombreador de geometría permite ejecutar varias ejecuciones del mismo sombreador de geometría por primitiva. Para crear instancias de un sombreador de geometría, agregue un atributo de instancia a la función de sombreador principal e identifique un parámetro de índice de instancia en el cuerpo de la función del sombreador.

Para crear instancias de un sombreador de geometría:

1.  Agregue el [atributo de instancia](sm5-attributes-instance.md) a la función main.

    ```
    [instance(24)]
    ```

    

    Esto define el número de instancias (un máximo de 32) que se ejecutarán para cada primitiva.

2.  Adjunte el valor del sistema [ \_ SV GSInstanceID](sv-gsinstanceid.md) a una variable de la lista de parámetros de función que se puede usar para realizar un seguimiento del identificador de la instancia que se ejecuta.
    ```
    uint InstanceID : SV_GSInstanceID
    ```

    

3.  Compile y cree el sombreador como haría con cualquier otro sombreador de geometría.

Otros detalles incluyen:

-   El número máximo de instancias es 32.
-   El recuento máximo de vértices es un recuento máximo de vértices por instancia.
-   Cada invocación de instancia (como cualquier invocación de sombreador de geometría) aumenta el recuento de invocaciones y genera un restartStrip() implícito.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Características del sombreador de geometría](overviews-direct3d-11-hlsl-gs-features.md)
</dt> </dl>

 

 




