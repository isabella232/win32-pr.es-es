---
description: Genera declaraciones de constantes de C para los tipos de puerto.
ms.assetid: 05a06206-3cc4-428d-b9f2-b7945e63922c
title: elemento portTypeDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c4e202f1451d93b519bd59ea51f591c37a92957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706139"
---
# <a name="porttypedeclarations-element"></a>elemento portTypeDeclarations

Genera declaraciones de constantes de C para los tipos de puerto.

## <a name="usage"></a>Uso

``` syntax
<portTypeDeclarations>
  child elements
</portTypeDeclarations>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                   | Descripción                                                                                                                                                               |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Nombre**](codename.md)<br/>   | Especifica el nombre que se va a usar para el tipo de puerto en el código generado. De forma predeterminada, el nombre del código se genera a partir del nombre completo del tipo de puerto.<br/> <br/> |
| [**sesión**](operation.md)<br/> | Especifica una operación para la que se va a generar código.<br/> <br/>                                                                                          |
| [**portType**](porttype.md)<br/>   | Especifica el tipo de puerto para el que se generará el código.<br/> <br/>                                                                                         |



### <a name="child-element-sequence"></a>Secuencia de elementos secundarios

``` syntax
(
  portType?, 
  operation*, 
  codeName?
)
```

## <a name="parent-elements"></a>Elementos primarios



| Elemento                         | Descripción                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**archivo**](file.md)<br/> | Genera un archivo desde el generador de código.<br/> <br/> |



## <a name="remarks"></a>Observaciones

La aplicación hace referencia a las declaraciones de tipo de puerto y gran parte del código generado. Este elemento se usa para generar archivos de inclusión.

## <a name="element-information"></a>Información de elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




