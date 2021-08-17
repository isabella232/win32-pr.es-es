---
description: El control DirectoryList publica el control IgnoreChange ControlEvent cuando se cambia la carpeta seleccionada de un directorio a otro directorio del control. Este evento debe crearse en la tabla EventMapping.
ms.assetid: 4d3128a1-cbe3-457c-83b5-8f6ec1a7ba29
title: IgnoreChange ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8efc2750c4d1e2bd85f7c31348f507917f828725de95658095e964b22a110a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118634463"
---
# <a name="ignorechange-controlevent"></a>IgnoreChange ControlEvent

El [control DirectoryList](directorylist-control.md) publica el control IgnoreChange ControlEvent cuando se cambia la carpeta seleccionada de un directorio a otro directorio del control. Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).

Este control ControlEvent requiere que la interfaz de usuario se ejecute en el [*nivel completo de la interfaz de*](f-gly.md) usuario. Este evento no funcionará con una interfaz de usuario [*reducida o*](r-gly.md) una interfaz de [*usuario básica.*](b-gly.md) Para obtener información, [vea Interfaz de usuario Levels](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

[DirectoryList](directorylist-control.md)

## <a name="argument"></a>Argumento

Este control ControlEvent no usa un argumento.

## <a name="action-on-subscribers"></a>Acción en suscriptores

Este control ControlEvent no realiza ninguna acción en los suscriptores.

## <a name="typical-use"></a>Uso típico

El [control DirectoryCombo](directorycombo-control.md) emplea normalmente IgnoreChange ControlEvent.

 

 



