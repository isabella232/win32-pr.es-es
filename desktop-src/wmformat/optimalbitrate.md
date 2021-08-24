---
title: OptimalBitrate
description: El atributo OptimalBitrate contiene la velocidad de bits a la que se reproduce mejor el archivo.
ms.assetid: cd13b9b5-34d2-4ebb-9f10-3bf42dd9de81
keywords:
- Formato multimedia de Windows OptimalBitrate
topic_type:
- apiref
api_name:
- OptimalBitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f670c2acd2f2190a5ee2bfd76994c219c6f967dbbd933520a8d4627236a0d36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930635"
---
# <a name="optimalbitrate"></a>OptimalBitrate

El **atributo OptimalBitrate** contiene la velocidad de bits a la que se reproduce mejor el archivo.

## <a name="global-constant"></a>Constante global

g \_ wszWMOptimalBitrate

## <a name="data-type"></a>Tipo de datos

**DWORD \_ DE TIPO \_ WMT**

## <a name="remarks"></a>Comentarios

Se trata de un atributo codificado.

Para los archivos que contienen secuencias de velocidad de bits variable (VBR), este valor es la velocidad de bits máxima para las secuencias del archivo. Para los archivos sin VBR, este valor es igual que la [**velocidad de bits**](bit-rate.md).

Este atributo no se puede duplicar en el nivel de archivo. Si este atributo se usa para una secuencia individual, se tratará como metadatos personalizados y no transmitirá su significado normal a los objetos del SDK Windows Media Format.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




