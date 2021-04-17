---
description: El control DirectoryList publica IgnoreChange ControlEvent, cuando se cambia la carpeta seleccionada de un directorio a otro en el control. Este evento debe crearse en la tabla EventMapping.
ms.assetid: 4d3128a1-cbe3-457c-83b5-8f6ec1a7ba29
title: IgnoreChange ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9db909552e97f29b8ebcd9d58ac8688474788ec0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652586"
---
# <a name="ignorechange-controlevent"></a>IgnoreChange ControlEvent,

El [control DirectoryList](directorylist-control.md) publica IgnoreChange ControlEvent, cuando se cambia la carpeta seleccionada de un directorio a otro en el control. Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).

Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) . Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida. Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

[DirectoryList](directorylist-control.md)

## <a name="argument"></a>Argumento

Este ControlEvent, no utiliza un argumento.

## <a name="action-on-subscribers"></a>Acción en los suscriptores

Este ControlEvent, no realiza ninguna acción en los suscriptores.

## <a name="typical-use"></a>Uso típico

Normalmente, el [control DirectoryCombo](directorycombo-control.md) emplea el ControlEvent, de IgnoreChange.

 

 



