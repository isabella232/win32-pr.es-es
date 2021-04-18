---
title: OptimalBitrate
description: El atributo OptimalBitrate contiene la velocidad de bits a la que se reproduce el archivo.
ms.assetid: cd13b9b5-34d2-4ebb-9f10-3bf42dd9de81
keywords:
- OptimalBitrate formato de Windows Media
topic_type:
- apiref
api_name:
- OptimalBitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff71c6b64cbc4bf4ccc4f346e62a5eae066e78ce
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105704853"
---
# <a name="optimalbitrate"></a>OptimalBitrate

El atributo **OptimalBitrate** contiene la velocidad de bits a la que se reproduce el archivo.

## <a name="global-constant"></a>Constante global

g \_ wszWMOptimalBitrate

## <a name="data-type"></a>Tipo de datos

**tipo de WMT \_ \_ DWORD**

## <a name="remarks"></a>Observaciones

Se trata de un atributo codificado.

En el caso de los archivos que contienen secuencias de velocidad de bits variable (VBR), este valor es la velocidad de bits máxima de las secuencias del archivo. En el caso de los archivos sin VBR, este valor es igual que la [**velocidad de bits**](bit-rate.md).

Este atributo no se puede duplicar en el nivel de archivo. Si este atributo se usa para una secuencia individual, se tratará como metadatos personalizados y no enviará su significado normal a los objetos del SDK de Windows Media Format.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




