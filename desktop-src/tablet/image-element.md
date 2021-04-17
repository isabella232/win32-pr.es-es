---
description: Contiene datos binarios codificados para una imagen en el documento de diario, si está presente.
ms.assetid: fbb86bef-68f7-4aad-8a98-1c68e79ea2de
title: Elemento de imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8437495a4c248a8e5bc68a0f7b75a2cf7d761387
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697378"
---
# <a name="image-element"></a>Elemento de imagen

Contiene datos binarios codificados para una imagen en el documento de diario, si está presente.

## <a name="definition"></a>Definición

``` syntax
 Copy Code<xs:element name="Image" type="ImageType" />
```

## <a name="parent-elements"></a>Elementos primarios

[**Contenido**](content-element--journal-reader.md)

[**Groupnode BizTalk**](groupnode-element.md)

## <a name="child-elements"></a>Elementos secundarios

Ninguno.

## <a name="attributes"></a>Atributos



| Atributo  | Tipo                      | Obligatorio | Descripción                                                                             | Valores posibles           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Obligatorio | Distancia desde el origen hasta el punto situado más a la izquierda del cuadro de límite del elemento. | Cualquier número entero.              |
| **Top** (Principales)    | **xs:integer**            | Obligatorio | Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.  | Cualquier número entero.              |
| **Width**  | **xs:nonNegativeInteger** | Obligatorio | Ancho del cuadro de límite del elemento.                                          | Cualquier entero no negativo. |
| **Height** | **xs:nonNegativeInteger** | Obligatorio | Alto del cuadro de límite del elemento.                                         | Cualquier entero no negativo. |



 

## <a name="element-information"></a>Información de elemento



|              |                                                         |
|--------------|---------------------------------------------------------|
| Tipo de elemento | [**ImageType**](imagetype-complex-type.md) complexType |
| Espacio de nombres    | urn: schemas-microsoft-com: TabletPC: richink              |
| Nombre del esquema  | Lector de diario                                          |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Información previa**](background-element.md)
</dt> </dl>

 

 



