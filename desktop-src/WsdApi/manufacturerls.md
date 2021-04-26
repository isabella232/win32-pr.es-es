---
description: Especifica una versión localizada del nombre del fabricante.
ms.assetid: e87de50f-60ec-4c18-b21c-81f7b6928752
title: elemento manufacturerLS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d24950355c5439d9a99c4ef451f1330772f3459
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993682"
---
# <a name="manufacturerls-element"></a>elemento manufacturerLS

Especifica una versión localizada del nombre del fabricante.

## <a name="usage"></a>Uso

``` syntax
<manufacturerLS
  Language = "language identifier string"
  Data = "localized manufacturer name string"/>
```

## <a name="attributes"></a>Atributos



| Atributo               | Tipo                                          | Obligatorio       | Descripción                                                             |
|-------------------------|-----------------------------------------------|----------------|-------------------------------------------------------------------------|
| **Data**<br/>     | cadena de nombre de fabricante localizada<br/> | Sí<br/> | Nombre del fabricante localizado.<br/> <br/>                 |
| **Lenguaje**<br/> | cadena de identificador de idioma<br/>         | Sí<br/> | Idioma del nombre del fabricante localizado.<br/> <br/> |



## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                   | Descripción                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**thisModelMetadata**](thismodelmetadata.md)<br/> | Define los metadatos del fabricante y del modelo para el dispositivo que se va a implementar.<br/> <br/> |



## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




