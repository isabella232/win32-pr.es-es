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
ms.openlocfilehash: 5c38ef36319b8021de918a798c94a3be0683a7b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164130"
---
# <a name="d1106-resource-is-wrong-type"></a>D1106: El tipo de recurso es incorrecto

El recurso de \[ *recurso especificado* \] no es de un tipo esperado.

## <a name="placeholders"></a>Marcadores de posición

<dl> <dt>

<span id="resource"></span><span id="RESOURCE"></span>*Recursos*
</dt> <dd>

Dirección del recurso.

</dd> </dl> 




 

## <a name="possible-causes"></a>Causas posibles

Una interfaz se ha conversión incorrectamente y se ha usado como parámetro para un método o función.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se pasa [**un ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) cuando se [**espera un ID2D1Geometry.**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)


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

 

 
