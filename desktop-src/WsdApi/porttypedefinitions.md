---
description: Genera constantes de C para tipos de puerto.
ms.assetid: 6ad0d163-df51-48b6-aad7-a4b018688872
title: elemento portTypeDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af9beb5b6697f53ecc3a9f7c805338c6ccebd9901d483607b100f5d1602ff4c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071395"
---
# <a name="porttypedefinitions-element"></a>elemento portTypeDefinitions

Genera constantes de C para tipos de puerto.

## <a name="usage"></a>Uso

``` syntax
<portTypeDefinitions>
  child elements
</portTypeDefinitions>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                   | Descripción                                                                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Codename**](codename.md)<br/>                   | Especifica el nombre que se usará para el tipo de puerto en el código generado. De forma predeterminada, el nombre del código se genera a partir del nombre completo del tipo de puerto.<br/> <br/>         |
| [**eventStubFunction**](eventstubfunction.md)<br/> | Especifica si las referencias de función de código auxiliar deben incluirse en las estructuras de operación en las definiciones de tipo de puerto para las operaciones de notificación.<br/> <br/>        |
| [**operation**](operation.md)<br/>                 | Especifica una operación para la que se va a generar código.<br/> <br/>                                                                                                  |
| [**portType**](porttype.md)<br/>                   | Especifica el tipo de puerto para el que se va a generar el código.<br/> <br/>                                                                                                 |
| [**stubFunction**](stubfunction.md)<br/>           | Especifica si las referencias de función de código auxiliar deben incluirse en las estructuras de operación en las definiciones de tipo de puerto para las operaciones un solo sentido y dos.<br/> <br/> |



### <a name="child-element-sequence"></a>Secuencia de elementos secundarios

``` syntax
(
  portType?, 
  operation*, 
  stubFunction?, 
  eventStubFunction?, 
  codeName?
)
```

## <a name="parent-elements"></a>Elementos primarios



| Elemento                         | Descripción                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Archivo**](file.md)<br/> | Genera un archivo desde el generador de código.<br/> <br/> |



## <a name="remarks"></a>Comentarios

Este elemento se usa generalmente en los archivos de código fuente de C para proporcionar las constantes de tipo de puerto declaradas por [**portTypeDeclarations**](porttypedeclarations.md).

## <a name="element-information"></a>Información de elemento



| Etiqueta | Valor |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




