---
description: Genera definiciones de estructura de C para los tipos de mensaje.
ms.assetid: 68459b22-0f35-444a-969e-29695e735774
title: elemento messageStructureDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8840e4493cb97d33cb0dac8ce1ace97cc1789e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696908"
---
# <a name="messagestructuredefinitions-element"></a>elemento messageStructureDefinitions

Genera definiciones de estructura de C para los tipos de mensaje.

## <a name="usage"></a>Uso

``` syntax
<messageStructureDefinitions>
  child elements
</messageStructureDefinitions>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                   | Descripción                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [**sesión**](operation.md)<br/> | Especifica una operación para la que se va a generar código.<br/> <br/>  |
| [**portType**](porttype.md)<br/>   | Especifica el tipo de puerto para el que se generará el código.<br/> <br/> |



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
| [**archivo**](file.md)<br/> | Genera un archivo desde el generador de código.<br/> <br/> |



## <a name="remarks"></a>Observaciones

El código auxiliar y el proxy generado hacen referencia a las estructuras de mensajes. Este elemento se usa para generar archivos de inclusión.

## <a name="element-information"></a>Información de elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




