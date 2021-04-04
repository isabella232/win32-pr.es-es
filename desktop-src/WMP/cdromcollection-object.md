---
title: Objeto CdromCollection
description: El objeto CdromCollection proporciona una manera de organizar y obtener acceso a una colección de unidades de CD o DVD.
ms.assetid: 02429ba7-a053-42bf-9ed5-c05e13c964c0
keywords:
- Objeto CdromCollection Media Player de Windows
topic_type:
- apiref
api_name:
- CdromCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0d5367a6887290f06d36225f211f42048e98ba03
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076492"
---
# <a name="cdromcollection-object"></a>Objeto CdromCollection

El objeto **CdromCollection** proporciona una manera de organizar y obtener acceso a una colección de unidades de CD o DVD.

El objeto **CdromCollection** admite la siguiente propiedad.



| Propiedad                           | Descripción                                                        |
|------------------------------------|--------------------------------------------------------------------|
| [count](cdromcollection-count.md) | Recupera el número de unidades de CD y DVD disponibles en el sistema. |



 

El objeto **CdromCollection** admite los siguientes métodos.



| Método                                                         | Descripción                                                                               |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [getByDriveSpecifier](cdromcollection-getbydrivespecifier.md) | Recupera el objeto [CDROM](cdrom-object.md) asociado a una letra de unidad concreta. |
| [item](cdromcollection-item.md)                               | Recupera el objeto [CDROM](cdrom-object.md) en el índice especificado.                        |



 

Se tiene acceso al objeto **CdromCollection** a través de la propiedad siguiente.



| Object                      | Propiedad                                      |
|-----------------------------|-----------------------------------------------|
| [Reproductor](player-object.md) | [cdromCollection](player-cdromcollection.md) |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




