---
description: Especifica el tipo de puerto para el que se generará el código.
ms.assetid: 8a7762ae-2e39-46e1-b49f-09cae1af9b0d
title: elemento portType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a466ccdcfda133a2a314609e9698cd37c6bf31c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706381"
---
# <a name="porttype-element"></a>elemento portType

Especifica el tipo de puerto para el que se generará el código.

## <a name="usage"></a>Uso

``` syntax
<portType/>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                                                 | Descripción                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**functionDeclarations**](functiondeclarations.md)<br/>                                         | Genera declaraciones de implementación para las funciones de proxy para las operaciones de tipo de puerto.<br/> <br/>                                    |
| [**idlFunctionDeclarations**](idlfunctiondeclarations.md)<br/>                                   | Genera declaraciones IDL para las funciones de proxy para las operaciones de tipo de puerto.<br/> <br/>                                               |
| [**messageStructureDefinitions**](messagestructuredefinitions.md)<br/>                           | Genera definiciones de estructura de C para los tipos de mensaje.<br/> <br/>                                                                   |
| [**messageTypeDeclarations**](messagetypedeclarations.md)<br/>                                   | Genera declaraciones de constantes de C para las tablas de esquemas XML para los tipos de mensaje.<br/> <br/>                                             |
| [**messageTypeDefinitions**](messagetypedefinitions.md)<br/>                                     | Genera constantes de C para las tablas de esquemas XML para los tipos de mensaje.<br/> <br/>                                                         |
| [**portTypeDeclarations**](porttypedeclarations.md)<br/>                                         | Genera declaraciones de constantes de C para los tipos de puerto.<br/> <br/>                                                                      |
| [**portTypeDefinitions**](porttypedefinitions.md)<br/>                                           | Genera constantes de C para los tipos de puerto.<br/> <br/>                                                                                  |
| [**proxyFunctionImplementations**](proxyfunctionimplementations.md)<br/>                         | Genera implementaciones para las funciones de proxy para las operaciones de tipo de puerto.<br/> <br/>                                                |
| [**stubDeclarations**](stubdeclarations.md)<br/>                                                 | Genera declaraciones para las funciones de código auxiliar para las operaciones de tipo de puerto.<br/> <br/>                                                    |
| [**stubDefinitions**](stubdefinitions.md)<br/>                                                   | Genera implementaciones para las funciones de código auxiliar para las operaciones de tipo de puerto.<br/> <br/>                                                 |
| [**subscriptionFunctionDeclarations**](subscriptionfunctiondeclarations.md)<br/>                 | Genera declaraciones de implementación para las funciones de proxy de suscripción y cancelación de suscripción para las operaciones de notificación de tipo de puerto.<br/> <br/> |
| [**subscriptionIdlFunctionDeclarations**](subscriptionidlfunctiondeclarations.md)<br/>           | Genera declaraciones IDL para las funciones de proxy de suscripción y cancelación de suscripción para las operaciones de notificación de tipo de puerto.<br/> <br/>            |
| [**subscriptionProxyFunctionImplementations**](subscriptionproxyfunctionimplementations.md)<br/> | Genera implementaciones para las funciones de proxy de suscripción y cancelación de suscripción para las operaciones de notificación de tipo de puerto.<br/> <br/>             |



## <a name="remarks"></a>Observaciones

De forma predeterminada, se genera código para todos los tipos de puerto de los archivos de entrada WSDL.

## <a name="element-information"></a>Información de elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




