---
description: El filtro de direcciones notifica al controlador de Monitor de red para que acepte fotogramas que tengan uno de los distintos tipos de direcciones MAC especificadas (Ethernet, token ring y FDDI).
ms.assetid: 23a38f49-2d63-4fc8-8113-29143493359c
title: Escribir la parte de filtro de ADDRESSTABLE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b06b00d046d555dffc39561b817629f4f47ca4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669674"
---
# <a name="writing-addresstable-filter-portion"></a>Escribir la parte de filtro de ADDRESSTABLE

El filtro de direcciones notifica al controlador de Monitor de red para que acepte fotogramas que tengan uno de los distintos tipos de direcciones MAC especificadas (Ethernet, token ring y FDDI). Puede especificar un máximo de ocho pares de direcciones. Un par de direcciones puede especificar un origen, un destino, ambos o ninguno.

La parte de la dirección del filtro consta de dos estructuras: [**ADDRESSTABLE**](addresstable.md) y [**ADDRESSPAIR**](addresspair.md).

Si NO especifica ninguna dirección, todos los marcos pasarán el filtro de direcciones. Sin embargo, si especifica cualquier dirección, solo se pasarán los fotogramas que pasen el filtro de dirección determinado.

La creación del filtro de direcciones implica la asignación de una estructura [**ADDRESSTABLE**](addresstable.md) y el rellenado de miembros de la estructura [**ADDRESSPAIR**](addresspair.md) .

**Para compilar la parte de la dirección de un filtro de captura**

1.  Use la marca **CAPTUREFILTER \_ Flags \_ local \_ Only** de la estructura [**CAPTUREFILTER**](capturefilter.md) para restringir la captura al tráfico hacia y desde el equipo local.

    Al establecer esta marca, no se establecerá la NIC en el modo promiscuo; el archivo de captura solo capturará el tráfico local.

2.  Use el código de ejemplo siguiente para definir la estructura [**ADDRESSTABLE**](addresstable.md) :

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

3.  Utilice la información que se muestra en la tabla siguiente para seleccionar un tipo de marca [**ADDRESSPAIR**](addresspair.md) . 

    | Marca                             | Significado                                                                               |
    |----------------------------------|---------------------------------------------------------------------------------------|
    | marcas de dirección \_ \_ Match \_ DST       | Coincide con una dirección de destino.                                                        |
    | coincidencia de marcas de dirección \_ \_ \_ src       | Coincide con una dirección de origen                                                              |
    | \_excluir marcas de dirección \_          | Excluye el marco si se encuentra esta dirección (ya sea un origen o un destino definidos). |
    | marcas de dirección \_ \_ grupo de DST \_ \_ | Coincide con el bit de grupo (de la dirección de destino) solo para mensajes de tipo difusión.      |
    | las \_ marcas de dirección \_ coinciden con \_ ambas      | Coincide con las direcciones de origen y de destino.                                    |

    

     

4.  Rellene una dirección de destino, que se evalúa con la marca [**ADDRESSPAIR**](addresspair.md) que seleccione.
5.  Rellene una dirección de origen, que se evalúa con la marca [**ADDRESSPAIR**](addresspair.md) que seleccione.
6.  Rellene la estructura [**ADDRESSTABLE**](addresstable.md) con una matriz de estructuras [**ADDRESSPAIR**](addresspair.md) , que incluye los pares de direcciones que el controlador evalúa. Todos los pares de direcciones se evalúan como una instrucción OR lógica (ADDRESSPAIR 1 \| \| ADDRESSPAIR 2). Puede incluir un máximo de ocho pares de direcciones en un filtro de captura.

 

 



