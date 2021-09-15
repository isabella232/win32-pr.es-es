---
title: CurrentBitrate
description: El atributo CurrentBitrate contiene la velocidad de bits total actual de las secuencias activas en el archivo.
ms.assetid: 961f36d5-a408-40d9-9ca1-0ed7c484858f
keywords:
- CurrentBitrate windows Media Format
topic_type:
- apiref
api_name:
- CurrentBitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdcd8db7d60c65bcb7ceedcac4498ac650f90d9a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572220"
---
# <a name="currentbitrate"></a>CurrentBitrate

El atributo CurrentBitrate contiene la velocidad de bits total actual de las secuencias activas en el archivo.

## <a name="global-constant"></a>Constante global

g \_ wszWMCurrentBitrate

## <a name="data-type"></a>Tipo de datos

**DWORD \_ DE TIPO \_ WMT**

## <a name="remarks"></a>Observaciones

Se trata de un atributo codificado.

El valor recuperado para **CurrentBitrate** es diferente en función del objeto utilizado. En el lector o el objeto de lector sincrónico, el valor es la velocidad de bits real en el momento de la llamada. En el objeto del editor de metadatos, el valor es la velocidad de bits media del archivo.

La velocidad de bits real de un archivo es igual a las velocidades de bits de todas las secuencias activas más alguna sobrecarga. Este es el valor que se muestra, por ejemplo, al reproducir un archivo con el Reproductor de Windows Media.

Este atributo no se puede duplicar en el nivel de archivo. Si este atributo se usa para una secuencia individual, se tratará como metadatos personalizados y no transmitirá su significado normal a los objetos del SDK Windows Media Format.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




