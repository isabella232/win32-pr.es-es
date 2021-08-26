---
description: El filtro de direcciones notifica al controlador Monitor de red que acepte fotogramas que tengan uno de los distintos tipos de direcciones MAC especificados (Ethernet, Token Ring y FDDI).
ms.assetid: 23a38f49-2d63-4fc8-8113-29143493359c
title: Escribir la parte del filtro ADDRESSTABLE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efbf0a18f8004ea4c38607d6c1c7b8fa741315b41fefe5b4d31b103167d415eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128795"
---
# <a name="writing-addresstable-filter-portion"></a>Escribir la parte del filtro ADDRESSTABLE

El filtro de direcciones notifica al controlador Monitor de red que acepte fotogramas que tengan uno de los distintos tipos de direcciones MAC especificados (Ethernet, Token Ring y FDDI). Puede especificar un máximo de ocho pares de direcciones. Un par de direcciones puede especificar un origen, un destino, ambos o ninguno.

La parte de la dirección del filtro consta de dos estructuras: [**ADDRESSTABLE**](addresstable.md) y [**ADDRESSPAIR.**](addresspair.md)

Si especifica DIRECCIONES NO, TODOS los fotogramas pasarán el filtro de direcciones. Sin embargo, si especifica alguna dirección, solo pasarán los fotogramas que pasen el filtro de direcciones especificado.

La creación del filtro de direcciones implica asignar una [**estructura ADDRESSTABLE**](addresstable.md) y rellenar los miembros de la [**estructura ADDRESSPAIR.**](addresspair.md)

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
    | \_ADICIÓNR \_ DE GRUPO DST DE MARCAS \_ DE \_ DIRECCIONES | Coincide con el bit de grupo (de la dirección de destino) solo para los mensajes de tipo de difusión.      |
    | LAS \_ MARCAS DE DIRECCIÓN COINCIDEN CON \_ \_ AMBAS      | Coincide con las direcciones de destino y de origen.                                    |

    

     

4.  Rellene una dirección de destino, que se evalúa con la [**marca ADDRESSPAIR**](addresspair.md) que seleccione.
5.  Rellene una dirección de origen, que se evalúa con la [**marca ADDRESSPAIR**](addresspair.md) que seleccione.
6.  Rellene la [**estructura ADDRESSTABLE**](addresstable.md) con una matriz de estructuras [**ADDRESSPAIR,**](addresspair.md) que incluye los pares de direcciones que evalúa el controlador. Todos los pares de direcciones se evalúan como una instrucción OR lógica (ADDRESSPAIR 1 \| \| ADDRESSPAIR 2). Puede incluir un máximo de ocho pares de direcciones en un filtro de captura.

 

 



