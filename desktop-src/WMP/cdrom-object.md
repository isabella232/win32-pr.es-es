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
ms.openlocfilehash: 17c2de88749b4dd4a0ab756b77866c16e8878486
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242553"
---
# <a name="cdrom-object"></a>Cdrom (objeto)

El **objeto Cdrom** proporciona una manera de acceder a un CD o DVD en su unidad.

El **objeto Cdrom** admite las siguientes propiedades.



| Propiedad                                   | Descripción                                                                                                                                             |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [driveSpecifier](cdrom-drivespecifier.md) | Recupera la letra de unidad de CD o DVD.                                                                                                                   |
| [Reproducción](cdrom-playlist.md)             | Recupera un objeto [Playlist que](playlist-object.md) representa las pistas del CD actualmente en la unidad de CD o las entradas de título de nivel de raíz para DVD. |



 

El **objeto Cdrom** admite el método siguiente.



| Método                   | Descripción                          |
|--------------------------|--------------------------------------|
| [Expulsar](cdrom-eject.md) | Expulsa el CD o DVD de la unidad. |



 

Se **accede al objeto Cdrom** mediante el método siguiente.



| Object                                        | Método                           |
|-----------------------------------------------|----------------------------------|
| [CdromCollection](cdromcollection-object.md) | [item](cdromcollection-item.md) |



 

Para fines ilustrativos, se usa player.cdromCollection.item(*index*) en las secciones de sintaxis de referencia.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




