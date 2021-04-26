---
description: Genera declaraciones constantes de C para tablas de esquema XML para tipos de mensaje.
ms.assetid: 17556708-9350-444f-84a3-d982270b31d1
title: elemento messageTypeDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 696cd6d30e6a791f68c152e0d0c5d0b1a7300769
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998732"
---
# <a name="messagetypedeclarations-element"></a>elemento messageTypeDeclarations

Genera declaraciones constantes de C para tablas de esquema XML para tipos de mensaje.

## <a name="usage"></a>Uso

``` syntax
<messageTypeDeclarations>
  child elements
</messageTypeDeclarations>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                   | Descripción                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [**Operación**](operation.md)<br/> | Especifica una operación para la que se va a generar código.<br/> <br/>  |
| [**portType**](porttype.md)<br/>   | Especifica el tipo de puerto para el que se va a generar el código.<br/> <br/> |



### <a name="child-element-sequence"></a>Secuencia de elementos secundarios

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a>Elementos primarios



| Elemento                         | Descripción                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Archivo**](file.md)<br/> | Genera un archivo desde el generador de código.<br/> <br/> |



## <a name="remarks"></a>Comentarios

Las definiciones de tipo de puerto hacen referencia a las tablas de esquema. Por lo tanto, este elemento se usa normalmente justo antes de los [**elementos portTypeDefinitions.**](porttypedefinitions.md)

## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




