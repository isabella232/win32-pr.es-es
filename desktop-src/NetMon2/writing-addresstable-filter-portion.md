---
description: El filtro de direcciones notifica al controlador Monitor de red que acepte fotogramas que tengan uno de los distintos tipos de direcciones MAC especificados (Ethernet, Token Ring y FDDI).
ms.assetid: 23a38f49-2d63-4fc8-8113-29143493359c
title: Escribir la parte del filtro ADDRESSTABLE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b06b00d046d555dffc39561b817629f4f47ca4d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476714"
---
# <a name="writing-addresstable-filter-portion"></a>Escribir la parte del filtro ADDRESSTABLE

El filtro de direcciones notifica al controlador Monitor de red que acepte fotogramas que tengan uno de los distintos tipos de direcciones MAC especificados (Ethernet, Token Ring y FDDI). Puede especificar un máximo de ocho pares de direcciones. Un par de direcciones puede especificar un origen, un destino, ambos o ninguno.

La parte de la dirección del filtro consta de dos estructuras: [**ADDRESSTABLE**](addresstable.md) y [**ADDRESSPAIR.**](addresspair.md)

Si especifica no hay direcciones, todos los marcos pasarán el filtro de direcciones. Sin embargo, si especifica alguna dirección, solo pasarán los fotogramas que pasen el filtro de direcciones especificado.

La creación del filtro de direcciones implica asignar una [**estructura ADDRESSTABLE**](addresstable.md) y rellenar miembros de la [**estructura ADDRESSPAIR.**](addresspair.md)

**Para compilar la parte de dirección de un filtro de captura**

1.  Use la **marca CAPTUREFILTER \_ FLAGS \_ LOCAL \_ ONLY** de la estructura [**CAPTUREFILTER**](capturefilter.md) para restringir la captura al tráfico hacia y desde el equipo local.

    Al establecer esta marca, la NIC no se establecerá en modo promiscuo; el archivo de captura capturará solo el tráfico local.

2.  Use el código de ejemplo siguiente para definir la [**estructura ADDRESSTABLE:**](addresstable.md)

    ``` syntax
    typedef struct _ADDRESSTABLE
    {
        DWORD           nAddressPairs;
        DWORD           nNonMacAddressPairs;
        ADDRESSPAIR     AddressPair[MAX_ADDRESS_PAIRS];
    } ADDRESSTABLE;

    typedef ADDRESSTABLE *LPADDRESSTABLE;
     
    typedef struct _ADDRESSPAIR
    {
        WORD        AddressFlags;
        WORD        NalReserved;
        ADDRESS     DstAddress;
        ADDRESS     SrcAddress;
    } ADDRESSPAIR;

    typedef ADDRESSPAIR *LPADDRESSPAIR;
    ```

3.  Use la información que aparece en la tabla siguiente para seleccionar un [**tipo de marca ADDRESSPAIR.**](addresspair.md) 

    | Marca                             | Significado                                                                               |
    |----------------------------------|---------------------------------------------------------------------------------------|
    | LAS \_ MARCAS DE DIRECCIÓN COINCIDEN CON \_ \_ DST       | Coincide con una dirección de destino.                                                        |
    | LAS \_ MARCAS DE DIRECCIÓN COINCIDEN CON \_ \_ SRC       | Coincide con una dirección de origen                                                              |
    | EXCLUSIÓN \_ DE MARCAS DE \_ DIRECCIÓN          | Excluye el marco si se encuentra esta dirección (ya sea un origen o un destino definidos). |
    | MARCADOR \_ DE DIRECCIÓN \_ ADDR DE GRUPO \_ \_ DST | Coincide con el bit de grupo (de la dirección de destino) solo para los mensajes de tipo de difusión.      |
    | LAS \_ MARCAS DE DIRECCIÓN COINCIDEN CON \_ \_ AMBAS      | Coincide con las direcciones de destino y de origen.                                    |

    

     

4.  Rellene una dirección de destino, que se evalúa con la [**marca ADDRESSPAIR**](addresspair.md) que seleccione.
5.  Rellene una dirección de origen, que se evalúa con la [**marca ADDRESSPAIR**](addresspair.md) que seleccione.
6.  Rellene la [**estructura ADDRESSTABLE**](addresstable.md) con una matriz de estructuras [**ADDRESSPAIR,**](addresspair.md) que incluye los pares de direcciones que evalúa el controlador. Todos los pares de direcciones se evalúan como una instrucción OR lógica (ADDRESSPAIR 1 \| \| ADDRESSPAIR 2). Puede incluir un máximo de ocho pares de direcciones en un filtro de captura.

 

 



