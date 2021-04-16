---
description: Especifica una versión localizada del nombre del dispositivo.
ms.assetid: 67ebbca0-bdb2-4a6e-98d8-3d8d1029884f
title: elemento modelNameLS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e71be6ee3a2e1104858c0f51a4ff68a5cf8cb89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706143"
---
# <a name="modelnamels-element"></a>elemento modelNameLS

Especifica una versión localizada del nombre del dispositivo.

## <a name="usage"></a>Uso

``` syntax
<modelNameLS
  Language = "language identifier string"
  Data = "localized model name string"/>
```

## <a name="attributes"></a>Atributos



| Atributo               | Tipo                                   | Obligatorio       | Descripción                                                      |
|-------------------------|----------------------------------------|----------------|------------------------------------------------------------------|
| **Data**<br/>     | cadena de nombre de modelo localizado<br/> | Sí<br/> | Nombre del modelo localizado.<br/> <br/>                 |
| **Lenguaje**<br/> | cadena de identificador de idioma<br/>  | Sí<br/> | Lenguaje del nombre del modelo localizado.<br/> <br/> |



## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                   | Descripción                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**thisModelMetadata**](thismodelmetadata.md)<br/> | Define los metadatos del fabricante y del modelo para el dispositivo que se va a implementar.<br/> <br/> |



## <a name="element-information"></a>Información de elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




