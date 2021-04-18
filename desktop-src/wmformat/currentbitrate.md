---
title: CurrentBitrate
description: El atributo CurrentBitrate contiene la velocidad de bits total actual de las secuencias activas en el archivo.
ms.assetid: 961f36d5-a408-40d9-9ca1-0ed7c484858f
keywords:
- CurrentBitrate formato de Windows Media
topic_type:
- apiref
api_name:
- CurrentBitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdcd8db7d60c65bcb7ceedcac4498ac650f90d9a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105714301"
---
# <a name="currentbitrate"></a>CurrentBitrate

El atributo CurrentBitrate contiene la velocidad de bits total actual de las secuencias activas en el archivo.

## <a name="global-constant"></a>Constante global

g \_ wszWMCurrentBitrate

## <a name="data-type"></a>Tipo de datos

**tipo de WMT \_ \_ DWORD**

## <a name="remarks"></a>Observaciones

Se trata de un atributo codificado.

El valor recuperado para **CurrentBitrate** es diferente en función del objeto usado. En el objeto lector o lector sincrónico, el valor es la velocidad de bits real en el momento de la llamada. En el objeto editor de metadatos, el valor es la velocidad de bits promedio del archivo.

La velocidad de bits real de un archivo es igual a la velocidad de bits de todas las secuencias activas más la sobrecarga. Este es el valor que se muestra, por ejemplo, cuando se reproduce un archivo con la Media Player de Windows.

Este atributo no se puede duplicar en el nivel de archivo. Si este atributo se usa para una secuencia individual, se tratará como metadatos personalizados y no enviará su significado normal a los objetos del SDK de Windows Media Format.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




