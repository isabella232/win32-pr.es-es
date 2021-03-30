---
description: Este evento selecciona y resalta un directorio en el control DirectoryList que el usuario ha elegido abrir. Para obtener información relacionada, vea cuadro de diálogo examinar.
ms.assetid: 95cdf345-e1bb-41d8-b1e0-2acf97e33110
title: DirectoryListOpen ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbeb3a570f49032adb0f5208514c26dd9cc16726
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279656"
---
# <a name="directorylistopen-controlevent"></a>DirectoryListOpen ControlEvent,

Este evento selecciona y resalta un directorio en el [control DirectoryList](directorylist-control.md) que el usuario ha elegido abrir. Para obtener información relacionada, vea [cuadro de diálogo examinar](browse-dialog.md).

Este evento debe publicarse con un [control Pushbutton](pushbutton-control.md) situado en el mismo cuadro de diálogo que el control que se suscribe a este evento. El evento debe crearse en la [tabla ControlEvent,](controlevent-table.md).

Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) . Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida. Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).

Si no se ha seleccionado ningún directorio en el [control DirectoryList](directorylist-control.md), un evento DirectoryListOpen deshabilita cualquier otro control que publique un evento DirectoryListOpen.

## <a name="published-by"></a>Publicado por

[DirectoryList](directorylist-control.md)

## <a name="argument"></a>Argumento

Este ControlEvent, no utiliza un argumento.

## <a name="action-on-subscribers"></a>Acción en los suscriptores

Este ControlEvent, no realiza ninguna acción en los suscriptores.

## <a name="typical-use"></a>Uso típico

Un control [Pushbutton](pushbutton-control.md) en el mismo cuadro de diálogo modal que el DirectoryList se usa para desencadenar la ejecución paso a paso en la ruta de acceso.

 

 



