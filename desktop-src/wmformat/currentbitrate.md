---
title: CurrentBitrate
description: El atributo CurrentBitrate contiene la velocidad de bits total actual de las secuencias activas en el archivo.
ms.assetid: 961f36d5-a408-40d9-9ca1-0ed7c484858f
keywords:
- Formato multimedia de Windows CurrentBitrate
topic_type:
- apiref
api_name:
- CurrentBitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 028207ee152acac289da6608c682f5fc14a4fde69603a2aae05b841d0cfb46ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027953"
---
# <a name="currentbitrate"></a>CurrentBitrate

El atributo CurrentBitrate contiene la velocidad de bits total actual de las secuencias activas en el archivo.

## <a name="global-constant"></a>Constante global

g \_ wszWMCurrentBitrate

## <a name="data-type"></a>Tipo de datos

**DWORD \_ DE TIPO \_ WMT**

## <a name="remarks"></a>Comentarios

Se trata de un atributo codificado.

El valor recuperado para **CurrentBitrate** es diferente en función del objeto utilizado. En el lector o el objeto de lector sincrónico, el valor es la velocidad de bits real en el momento de la llamada. En el objeto del editor de metadatos, el valor es la velocidad de bits media del archivo.

La velocidad de bits real de un archivo es igual a la velocidad de bits de todas las secuencias activas, además de cierta sobrecarga. Este es el valor que, por ejemplo, se muestra al reproducir un archivo con el Reproductor de Windows Media.

Este atributo no se puede duplicar en el nivel de archivo. Si este atributo se usa para una secuencia individual, se tratará como metadatos personalizados y no transmitirá su significado normal a los objetos del SDK Windows Media Format.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




