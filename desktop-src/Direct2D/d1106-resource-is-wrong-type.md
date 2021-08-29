---
title: El recurso D1106 es un tipo incorrecto
ms.assetid: 79a618cb-1d05-4895-b801-7663890b456a
description: El recurso especificado no es de un tipo esperado.
keywords:
- El recurso D1106 es de tipo incorrecto Direct2D
topic_type:
- apiref
api_name:
- D1106 Resource Is Wrong Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 1bbfd6d58eeb155002fbf5e7dbe243bd8d942ddaf4fa7d7715c6211523015476
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911195"
---
# <a name="d1106-resource-is-wrong-type"></a>D1106: El tipo de recurso es incorrecto

El recurso especificado \[ *no* \] es de un tipo esperado.

## <a name="placeholders"></a>Marcadores de posición

<dl> <dt>

<span id="resource"></span><span id="RESOURCE"></span>*Recursos*
</dt> <dd>

Dirección del recurso.

</dd> </dl> 




 

## <a name="possible-causes"></a>Causas posibles

Una interfaz se ha conversión incorrectamente y se ha usado como parámetro para un método o función.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se pasa [**id2D1SolidColorBrush cuando**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) se [**espera un id2D1Geometry.**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)


```C++
        m_pRenderTarget->FillGeometry(
            (ID2D1Geometry*)m_pYellowGreenBrush,
            m_pYellowGreenBrush
            );
```



En este ejemplo se genera el siguiente mensaje de depuración:

``` syntax
DEBUG ERROR - The given resource[003A2C98] is not of an expected type
```

## <a name="fixes"></a>Correcciones

Use el tipo requerido por el método .

 

 
