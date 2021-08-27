---
title: Ver marcas
description: Use las marcas de vista para controlar las vistas de tabla de enrutamiento.
ms.assetid: 836e3400-0dca-4a21-9a5c-7da357ed72ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ae9763587cf7972aab3ca9880d5ad26350c3161955c17940484cc1cbd801bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024955"
---
# <a name="view-flags"></a>Ver marcas

Use las marcas de vista para controlar las vistas de tabla de enrutamiento.



| Constante                 | Value      | Descripción                                                      |
|--------------------------|------------|------------------------------------------------------------------|
| RTM \_ MAX \_ ADDRESS \_ SIZE | 16         | Tamaño máximo de dirección para una familia de direcciones.                          |
| VISTAS \_ MÁXIMAS DE RTM \_          | 32         | Número máximo de vistas que pueden estar activas en la tabla de enrutamiento. |
| ID. DE VISTA DE RTM \_ \_ \_ UCAST     | 0          | Especifica una vista de unidifusión.                                        |
| MCAST \_ DEL IDENTIFICADOR DE VISTA \_ \_ DE RTM     | 1          | Especifica una vista de multidifusión.                                      |
| TAMAÑO DE MÁSCARA \_ DE \_ VISTA RTM \_    | 0x20       | Especifica el número máximo de vistas que se pueden configurar.    |
| MÁSCARA DE \_ VISTA \_ RTM \_ NONE    | 0x00000000 | Devuelve información independientemente de la vista.                      |
| RTM \_ VIEW \_ MASK \_ ANY     | 0x00000000 | Devuelve destinos de todas las vistas. Este es el valor predeterminado.  |
| RTM \_ VIEW \_ MASK \_ UCAST   | 0x00000001 | Devuelve los destinos de la vista de unidifusión.                      |
| MCAST \_ DE MÁSCARA DE VISTA \_ \_ RTM   | 0x00000002 | Devuelve destinos de la vista de multidifusión.                    |
| RTM \_ VIEW \_ MASK \_ ALL     | 0xFFFFFFFF | Devuelve información de todas las vistas.                              |



 

 

 




