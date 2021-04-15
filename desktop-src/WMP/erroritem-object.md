---
title: Objeto ErrorItem
description: El objeto ErrorItem proporciona una manera de tener acceso a la información de errores.
ms.assetid: 14bc9c12-98c6-4b72-9ae5-d6afeb1303f9
keywords:
- Objeto ErrorItem Media Player de Windows
topic_type:
- apiref
api_name:
- ErrorItem Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c273d00477363c66c49dfa1f77a66dab42c711cb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105695504"
---
# <a name="erroritem-object"></a>Objeto ErrorItem

El objeto **ErrorItem** proporciona una manera de tener acceso a la información de errores.

El objeto **ErrorItem** admite las siguientes propiedades.



| Propiedad                                           | Descripción                                                                                     |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [condition](erroritem-condition.md)               | Recupera un valor que indica la condición del error.                                       |
| [customUrl](erroritem-customurl.md)               | Recupera la dirección URL de un sitio web que muestra información específica sobre el error de descarga de códec. |
| [errorCode](erroritem-errorcode.md)               | Recupera el código de error actual.                                                               |
| [errorContext](erroritem-errorcontext.md)         | Recupera un valor que indica el contexto del error.                                          |
| [errorDescription](erroritem-errordescription.md) | Recupera una descripción del error.                                                           |
| **remedio**                                         | Reservado para uso futuro.                                                                        |



 

Se tiene acceso al objeto **ErrorItem** a través de los métodos siguientes.



| Object                    | Método                   |
|---------------------------|--------------------------|
| [Error](error-object.md) | [item](error-item.md)   |
| [Elementos multimedia](media-object.md) | [error](media-error.md) |



 

Para fines de Ilustración, *reproductor*. *error*. *Item*(*index*) se usa en las secciones de sintaxis de referencia.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




