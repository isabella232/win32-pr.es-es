---
description: Contiene la clasificación de confianza devuelta por el analizador de entrada manuscrita Journal para InkWord.
ms.assetid: cb0ed0d0-5e2f-44a3-b72b-61cbfd22bae8
title: Elemento Confidence
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5fdaaed8d9c57822ad94ec49183a399ed317917
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360020"
---
# <a name="confidence-element"></a>Elemento Confidence

Contiene la clasificación de confianza devuelta por el analizador de entrada de lápiz Journal para [**InkWord.**](inkword-element.md)

## <a name="definition"></a>Definición

``` syntax
<xs:element name="Confidence" type="xs:string" minOccurs="0" />
```

## <a name="parent-elements"></a>Elementos primarios

[**InkWord**](inkword-element.md)

## <a name="values"></a>Valores

Los valores válidos para este campo incluyen "0", "1" y "2". 0 indica confianza fuerte, 1 indica confianza intermedia y 2 indica confianza baja.

## <a name="child-elements"></a>Elementos secundarios

Ninguno.

## <a name="attributes"></a>Atributos

Ninguno.

## <a name="element-information"></a>Información de elemento



|                  | Value                                      |
|------------------|--------------------------------------------|
| **Tipo de elemento** | xs:string                                  |
| **Espacio de nombres**    | urn:schemas-microsoft-com:tabletpc:richink |
| **Nombre del esquema**  | Lector de diario                             |



 

 

 



