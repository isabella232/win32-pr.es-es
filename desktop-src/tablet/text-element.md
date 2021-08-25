---
description: Contiene información de texto de la nota de diario.
ms.assetid: 09ec2e8a-bd50-4f82-8ce3-a1c61f48ddb7
title: Elemento Text
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae4e9fa123f1f43bd92d902158fc3fbc5b1c1de8e074b57aadeb339a0a7b6f15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119819945"
---
# <a name="text-element"></a>Elemento Text

Contiene información de texto de la nota de diario.

## <a name="definition"></a>Definición

Cuando se usa con [**contenido**](content-element--journal-reader.md):

``` syntax
<xs:element name="Text" type="TextType" />
```

O bien, cuando se [**usa con TitleInfo**](titleinfo-element.md) [**y GroupNode**](groupnode-element.md):

``` syntax
<xs:element name="Text" type="xs:string" />
```

## <a name="parent-elements"></a>Elementos primarios

[**Contenido**](content-element--journal-reader.md)

[**GroupNode**](groupnode-element.md)

[**TitleInfo**](titleinfo-element.md)

## <a name="child-elements"></a>Elementos secundarios

Ninguno.

## <a name="attributes"></a>Atributos

No hay ningún atributo cuando se usa [**con TitleInfo**](titleinfo-element.md) y [**GroupNode**](groupnode-element.md). Cuando se usa con [**Content**](content-element--journal-reader.md), los atributos son los siguientes.



| Atributo  | Tipo                      | Requerido | Descripción                                                                             | Valores posibles           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Requerido | Distancia desde el origen hasta el punto más a la izquierda en el cuadro de límite del elemento. | Cualquier número entero.              |
| **Top** (Principales)    | **xs:integer**            | Requerido | Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.  | Cualquier número entero.              |
| **Width**  | **xs:nonNegativeInteger** | Requerido | Ancho del cuadro de límite del elemento.                                          | Cualquier entero no negativo. |
| **Height** | **xs:nonNegativeInteger** | Requerido | Alto del cuadro de límite del elemento.                                         | Cualquier entero no negativo. |



 

## <a name="element-information"></a>Información de elemento



|   Elemento           |   Value                                |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo de elemento | [**TextType**](texttype-complex-type.md) complexType (con el elemento Content) o **xs:string** (con [**elementos GroupNode**](groupnode-element.md) [**y TitleInfo)**](titleinfo-element.md) |
| Espacio de nombres    | urn:schemas-microsoft-com:tabletpc:richink<br/>                                                                                                                                               |
| Nombre del esquema  | Lector de diario<br/>                                                                                                                                                                           |



 

 

 




