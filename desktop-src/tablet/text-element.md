---
description: Contiene información de texto de la nota de Journal.
ms.assetid: 09ec2e8a-bd50-4f82-8ce3-a1c61f48ddb7
title: Elemento Text
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed9c72fe584d0e796d4a6f897297aa60bbeddc5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002878"
---
# <a name="text-element"></a>Elemento Text

Contiene información de texto de la nota de Journal.

## <a name="definition"></a>Definición

Cuando se usa con [**contenido**](content-element--journal-reader.md):

``` syntax
<xs:element name="Text" type="TextType" />
```

O bien, cuando se usa con [**TitleInfo**](titleinfo-element.md) y [**groupnode BizTalk**](groupnode-element.md):

``` syntax
<xs:element name="Text" type="xs:string" />
```

## <a name="parent-elements"></a>Elementos primarios

[**Contenido**](content-element--journal-reader.md)

[**Groupnode BizTalk**](groupnode-element.md)

[**TitleInfo**](titleinfo-element.md)

## <a name="child-elements"></a>Elementos secundarios

Ninguno.

## <a name="attributes"></a>Atributos

No hay ningún atributo cuando se usa con [**TitleInfo**](titleinfo-element.md) y [**groupnode BizTalk**](groupnode-element.md). Cuando se usa con [**contenido**](content-element--journal-reader.md), los atributos son los siguientes.



| Atributo  | Tipo                      | Obligatorio | Descripción                                                                             | Valores posibles           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Obligatorio | Distancia desde el origen hasta el punto situado más a la izquierda del cuadro de límite del elemento. | Cualquier número entero.              |
| **Top** (Principales)    | **xs:integer**            | Obligatorio | Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.  | Cualquier número entero.              |
| **Width**  | **xs:nonNegativeInteger** | Obligatorio | Ancho del cuadro de límite del elemento.                                          | Cualquier entero no negativo. |
| **Height** | **xs:nonNegativeInteger** | Obligatorio | Alto del cuadro de límite del elemento.                                         | Cualquier entero no negativo. |



 

## <a name="element-information"></a>Información de elemento



|              |                                                                                                                                                                                                     |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo de elemento | [**TextType**](texttype-complex-type.md) complexType (con el elemento Content) o **xs: String** (con elementos [**groupnode BizTalk**](groupnode-element.md) y [**TitleInfo**](titleinfo-element.md) ) |
| Espacio de nombres    | urn: schemas-microsoft-com: TabletPC: richink<br/>                                                                                                                                               |
| Nombre del esquema  | Lector de diario<br/>                                                                                                                                                                           |



 

 

 




