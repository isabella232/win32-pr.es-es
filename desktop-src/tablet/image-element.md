---
description: Contiene datos binarios codificados para una imagen en el documento Journal, si está presente.
ms.assetid: fbb86bef-68f7-4aad-8a98-1c68e79ea2de
title: Elemento de imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9dd3b37a39ce45ee0294f46922fbab376523b64
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432587"
---
# <a name="image-element"></a>Elemento de imagen

Contiene datos binarios codificados para una imagen en el documento Journal, si está presente.

## <a name="definition"></a>Definición

``` syntax
 Copy Code<xs:element name="Image" type="ImageType" />
```

## <a name="parent-elements"></a>Elementos primarios

[**Contenido**](content-element--journal-reader.md)

[**GroupNode**](groupnode-element.md)

## <a name="child-elements"></a>Elementos secundarios

Ninguno.

## <a name="attributes"></a>Atributos



| Atributo  | Tipo                      | Requerido | Descripción                                                                             | Valores posibles           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Requerido | Distancia desde el origen hasta el punto más a la izquierda en el cuadro de límite del elemento. | Cualquier número entero.              |
| **Top** (Principales)    | **xs:integer**            | Requerido | Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.  | Cualquier número entero.              |
| **Width**  | **xs:nonNegativeInteger** | Requerido | Ancho del cuadro de límite del elemento.                                          | Cualquier entero no negativo. |
| **Height** | **xs:nonNegativeInteger** | Requerido | Alto del cuadro de límite del elemento.                                         | Cualquier entero no negativo. |



 

## <a name="element-information"></a>Información de elemento



|  Elemento     | Value                                                     |
|--------------|---------------------------------------------------------|
| Tipo de elemento | [**ImageType**](imagetype-complex-type.md) complexType |
| Espacio de nombres    | urn:schemas-microsoft-com:tabletpc:richink              |
| Nombre del esquema  | Lector de diario                                          |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Información previa**](background-element.md)
</dt> </dl>

 

 



