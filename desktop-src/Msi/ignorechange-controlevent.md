---
description: El control DirectoryList publica el control IgnoreChange ControlEvent cuando la carpeta seleccionada cambia de un directorio a otro del control . Este evento debe crearse en la tabla EventMapping.
ms.assetid: 4d3128a1-cbe3-457c-83b5-8f6ec1a7ba29
title: IgnoreChange ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9db909552e97f29b8ebcd9d58ac8688474788ec0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074450"
---
# <a name="ignorechange-controlevent"></a>IgnoreChange ControlEvent

El [control DirectoryList](directorylist-control.md) publica el control IgnoreChange ControlEvent cuando la carpeta seleccionada cambia de un directorio a otro del control . Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).

Este control ControlEvent requiere que la interfaz de usuario se ejecute en el [*nivel completo de la interfaz de*](f-gly.md) usuario. Este evento no funcionará con una interfaz de usuario [*reducida o*](r-gly.md) una interfaz de [*usuario básica.*](b-gly.md) Para obtener información, [vea Interfaz de usuario Levels](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

[DirectoryList](directorylist-control.md)

## <a name="argument"></a>Argumento

Este control ControlEvent no usa ningún argumento.

## <a name="action-on-subscribers"></a>Acción en suscriptores

Este control ControlEvent no realiza ninguna acción en los suscriptores.

## <a name="typical-use"></a>Uso típico

El [control DirectoryCombo](directorycombo-control.md) emplea normalmente IgnoreChange ControlEvent.

 

 



