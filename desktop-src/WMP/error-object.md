---
title: Objeto Error (SDK de WMP)
description: El objeto Error proporciona acceso a una colección de objetos ErrorItem.
ms.assetid: 1f026ad4-0240-48fe-90ad-739a24e8a7ca
keywords:
- Error Object Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Error Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c8e5b7627db2c55eb41a267f6c8d3a7a779e2f20190ca3061a49a41eb8577adb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748474"
---
# <a name="error-object"></a>Objeto de error

El **objeto Error** proporciona acceso a una colección de objetos [ErrorItem.](erroritem-object.md)

El **objeto Error** admite la siguiente propiedad.



| Propiedad                           | Descripción                                        |
|------------------------------------|----------------------------------------------------|
| [errorCount](error-errorcount.md) | Recupera el número de errores de la cola de errores. |



 

El **objeto Error** admite los métodos siguientes.



| Método                                       | Descripción                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------|
| [clearErrorQueue](error-clearerrorqueue.md) | Borra los errores de la cola de errores.                                                         |
| [item](error-item.md)                       | Recupera un objeto [ErrorItem](erroritem-object.md) de la cola de errores.                     |
| [Webhelp](error-webhelp.md)                 | Inicia la página Reproductor de Windows Media Web Help para mostrar más información sobre el error. |



 

Se **tiene** acceso al objeto Error a través de la propiedad siguiente.



| Object                      | Propiedad                  |
|-----------------------------|---------------------------|
| [Reproductor](player-object.md) | [error](player-error.md) |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




