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
ms.openlocfilehash: ff71c6b64cbc4bf4ccc4f346e62a5eae066e78ce
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467083"
---
# <a name="optimalbitrate"></a>OptimalBitrate

El **atributo OptimalBitrate** contiene la velocidad de bits a la que se reproduce mejor el archivo.

## <a name="global-constant"></a>Constante global

g \_ wszWMOptimalBitrate

## <a name="data-type"></a>Tipo de datos

**DWORD \_ DE TIPO \_ WMT**

## <a name="remarks"></a>Observaciones

Se trata de un atributo codificado.

Para los archivos que contienen secuencias de velocidad de bits variable (VBR), este valor es la velocidad de bits máxima para las secuencias del archivo. Para los archivos sin VBR, este valor es igual que la [**velocidad de bits**](bit-rate.md).

Este atributo no se puede duplicar en el nivel de archivo. Si este atributo se usa para una secuencia individual, se tratará como metadatos personalizados y no transmitirá su significado normal a los objetos del SDK Windows Media Format.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




