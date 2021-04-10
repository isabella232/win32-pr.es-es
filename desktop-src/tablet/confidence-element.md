---
description: Contiene la clasificación de confianza devuelta por Journal Ink Analyzer para InkWord.
ms.assetid: cb0ed0d0-5e2f-44a3-b72b-61cbfd22bae8
title: Elemento Confidence
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cef4869776a6cafc4e6ef4758649b918e0b5988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153753"
---
# <a name="confidence-element"></a>Elemento Confidence

Contiene la clasificación de confianza devuelta por Journal Ink Analyzer para [**InkWord**](inkword-element.md).

## <a name="definition"></a>Definición

``` syntax
<xs:element name="Confidence" type="xs:string" minOccurs="0" />
```

## <a name="parent-elements"></a>Elementos primarios

[**InkWord**](inkword-element.md)

## <a name="values"></a>Valores

Los valores válidos para este campo son "0", "1" y "2". 0 indica una confianza alta, 1 indica confianza intermedia y 2 indica una confianza deficiente.

## <a name="child-elements"></a>Elementos secundarios

Ninguno.

## <a name="attributes"></a>Atributos

Ninguno.

## <a name="element-information"></a>Información de elemento



|              |                                            |
|--------------|--------------------------------------------|
| Tipo de elemento | **xs:string**                              |
| Espacio de nombres    | urn: schemas-microsoft-com: TabletPC: richink |
| Nombre del esquema  | Lector de diario                             |



 

 

 



