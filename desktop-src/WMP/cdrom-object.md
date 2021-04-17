---
title: CDROM (objeto)
description: El objeto CDROM proporciona una manera de tener acceso a un CD o DVD en su unidad.
ms.assetid: 9045b130-3e08-4880-a4e7-79b704c4c1f9
keywords:
- Objeto CDROM Media Player de Windows
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
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104357901"
---
# <a name="cdrom-object"></a>CDROM (objeto)

El objeto **CDROM** proporciona una manera de tener acceso a un CD o DVD en su unidad.

El objeto **CDROM** admite las siguientes propiedades.



| Propiedad                                   | Descripción                                                                                                                                             |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [driveSpecifier](cdrom-drivespecifier.md) | Recupera la letra de unidad de CD o DVD.                                                                                                                   |
| [automáticas](cdrom-playlist.md)             | Recupera un objeto de [lista de reproducción](playlist-object.md) que representa las pistas del CD que se encuentran actualmente en la unidad de CD o en las entradas de título de nivel de raíz de DVD. |



 

El objeto **CDROM** admite el método siguiente.



| Método                   | Descripción                          |
|--------------------------|--------------------------------------|
| [expulsar](cdrom-eject.md) | Expulsa el CD o DVD de la unidad. |



 

Se tiene acceso al objeto **CDROM** mediante el método siguiente.



| Object                                        | Método                           |
|-----------------------------------------------|----------------------------------|
| [CdromCollection](cdromcollection-object.md) | [item](cdromcollection-item.md) |



 

A efectos de Ilustración, se usa Player. cdromCollection. Item (*index*) en las secciones de sintaxis de referencia.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




