---
title: CdromCollection (objeto)
description: El objeto CdromCollection proporciona una manera de organizar y acceder a una colección de unidades de CD o DVD.
ms.assetid: 02429ba7-a053-42bf-9ed5-c05e13c964c0
keywords:
- CdromCollection Object Reproductor de Windows Media
topic_type:
- apiref
api_name:
- CdromCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0f8fe20bc138feb3eb1ad5bc937ef1f53f0e6b08e5757bbe03791177fe4c3531
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863955"
---
# <a name="cdromcollection-object"></a>CdromCollection (objeto)

El **objeto CdromCollection** proporciona una manera de organizar y acceder a una colección de unidades de CD o DVD.

El **objeto CdromCollection** admite la siguiente propiedad.



| Propiedad                           | Descripción                                                        |
|------------------------------------|--------------------------------------------------------------------|
| [count](cdromcollection-count.md) | Recupera el número de unidades de CD y DVD disponibles en el sistema. |



 

El **objeto CdromCollection** admite los métodos siguientes.



| Método                                                         | Descripción                                                                               |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [getByDriveSpecifier](cdromcollection-getbydrivespecifier.md) | Recupera el objeto [Cdrom](cdrom-object.md) asociado a una letra de unidad determinada. |
| [item](cdromcollection-item.md)                               | Recupera el [objeto Cdrom](cdrom-object.md) en el índice especificado.                        |



 

Se **tiene acceso al objeto CdromCollection** a través de la propiedad siguiente.



| Object                      | Propiedad                                      |
|-----------------------------|-----------------------------------------------|
| [Reproductor](player-object.md) | [cdromCollection](player-cdromcollection.md) |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




