---
title: Error (objeto, WMP SDK)
description: El objeto error proporciona acceso a una colección de objetos ErrorItem.
ms.assetid: 1f026ad4-0240-48fe-90ad-739a24e8a7ca
keywords:
- Objeto de error de Windows Media Player
topic_type:
- apiref
api_name:
- Error Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0aae4c86dc3f5282be7a16207923e1238e217a9e
ms.sourcegitcommit: 6f7576b297d54c0b8f9c79e02c912b83041aa4fb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/09/2019
ms.locfileid: "105695520"
---
# <a name="error-object"></a>Objeto de error

El objeto **error** proporciona acceso a una colección de objetos [ErrorItem](erroritem-object.md) .

El objeto **error** admite la siguiente propiedad.



| Propiedad                           | Descripción                                        |
|------------------------------------|----------------------------------------------------|
| [errorCount](error-errorcount.md) | Recupera el número de errores en la cola de errores. |



 

El objeto **error** admite los métodos siguientes.



| Método                                       | Descripción                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------|
| [clearErrorQueue](error-clearerrorqueue.md) | Borra los errores de la cola de errores.                                                         |
| [item](error-item.md)                       | Recupera un objeto [ErrorItem](erroritem-object.md) de la cola de errores.                     |
| [WebHelp](error-webhelp.md)                 | Inicia la página de ayuda Web de Windows Media Player para mostrar información adicional sobre el error. |



 

Se tiene acceso al objeto de **error** a través de la propiedad siguiente.



| Object                      | Propiedad                  |
|-----------------------------|---------------------------|
| [Reproductor](player-object.md) | [error](player-error.md) |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




