---
description: Genera constantes de C para tablas de esquema XML para tipos de mensaje.
ms.assetid: 0b322acb-3326-42a2-a852-07251585b314
title: elemento messageTypeDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54f1b6563254a93122960b4a990fe0bd18ab1453
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473272"
---
# <a name="messagetypedefinitions-element"></a>elemento messageTypeDefinitions

Genera constantes de C para tablas de esquema XML para tipos de mensaje.

## <a name="usage"></a>Uso

``` syntax
<messageTypeDefinitions>
  child elements
</messageTypeDefinitions>
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



## <a name="remarks"></a>Observaciones

Este elemento se usa generalmente en los archivos de código fuente de C para proporcionar las tablas de esquema declaradas por [**messageTypeDeclarations**](messagetypedeclarations.md).

## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




