---
description: Especifica una versión localizada del nombre del dispositivo.
ms.assetid: 67ebbca0-bdb2-4a6e-98d8-3d8d1029884f
title: elemento modelNameLS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e47d2f83d1b636efc30e98dff8c46600bcee555d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995502"
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
| **Data**<br/>     | cadena de nombre de modelo localizada<br/> | Sí<br/> | Nombre del modelo localizado.<br/> <br/>                 |
| **Lenguaje**<br/> | cadena de identificador de idioma<br/>  | Sí<br/> | Idioma del nombre del modelo localizado.<br/> <br/> |



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



 

 




