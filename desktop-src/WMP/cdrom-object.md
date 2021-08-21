---
title: Cdrom (objeto)
description: El objeto Cdrom proporciona una manera de acceder a un CD o DVD en su unidad.
ms.assetid: 9045b130-3e08-4880-a4e7-79b704c4c1f9
keywords:
- Cdrom Object Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Cdrom Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 60c4e1081dec3e44107778e45fd911e0c4bb673d27b5e19874508ddbacb270ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342649"
---
# <a name="cdrom-object"></a>Cdrom (objeto)

El **objeto Cdrom** proporciona una manera de acceder a un CD o DVD en su unidad.

El **objeto Cdrom** admite las siguientes propiedades.



| Propiedad                                   | Descripción                                                                                                                                             |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [driveSpecifier](cdrom-drivespecifier.md) | Recupera la letra de unidad de CD o DVD.                                                                                                                   |
| [Reproducción](cdrom-playlist.md)             | Recupera un objeto [Playlist que](playlist-object.md) representa las pistas del CD actualmente en la unidad de CD o las entradas de título de nivel raíz para DVD. |



 

El **objeto Cdrom** admite el método siguiente.



| Método                   | Descripción                          |
|--------------------------|--------------------------------------|
| [Expulsar](cdrom-eject.md) | Expulsa el CD o DVD de la unidad. |



 

Se accede al objeto **Cdrom** mediante el método siguiente.



| Object                                        | Método                           |
|-----------------------------------------------|----------------------------------|
| [CdromCollection](cdromcollection-object.md) | [item](cdromcollection-item.md) |



 

Para fines ilustrativos, se usa player.cdromCollection.item(*index*) en las secciones de sintaxis de referencia.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




