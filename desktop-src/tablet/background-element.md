---
description: Contiene el fondo de un elemento JournalDocument o un elemento JournalPage.
ms.assetid: 48527c4e-50fb-4800-ac87-1646234783ba
title: Elemento Background
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3585b8ca37fe86bd1c687601975ea0ad189d5746
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579508"
---
# <a name="background-element"></a>Elemento Background

Contiene el fondo de un [**elemento JournalDocument**](journaldocument-element.md) o [**un elemento JournalPage.**](journalpage-element.md)

## <a name="definition"></a>Definición

``` syntax
<xs:element name="Background" type="BackgroundType" minOccurs="0" />
```

## <a name="parent-elements"></a>Elementos primarios

[**Diseño de fondo**](stationery-element.md)

## <a name="child-elements"></a>Elementos secundarios

[**Imagen**](image-element.md)

## <a name="attributes"></a>Atributos




| Atributo | Tipo | Obligatorio | Descripción | Valores posibles | 
|-----------|------|----------|-------------|-----------------|
| <strong>Estilo</strong> | <strong>xs:string</strong> | Obligatorio | Especifica el estilo del fondo. | <ul><li>None</li><li>Sólido</li></ul> | 
| <strong>Color</strong> | <a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType | Opcional | Especifica el color del fondo. | Consulte <a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType. | 




 

## <a name="element-information"></a>Información de elemento



|                  | Value                                                             |
|------------------|-------------------------------------------------------------------|
| **Tipo de elemento** | [**BackgroundType**](backgroundtype-complex-type.md) complexType |
| **Espacio de nombres**    | urn:schemas-microsoft-com:tabletpc:richink                        |
| **Nombre del esquema**  | Lector de diario                                                    |



 

 

 



