---
description: Este evento notifica al control DirectoryList que el usuario desea seleccionar el elemento primario del directorio actual. Para obtener información relacionada, vea cuadro de diálogo examinar.
ms.assetid: 83fdb160-ce3b-42e1-8688-42d3ba39d6dd
title: DirectoryListUp ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0fa8b3fcb19c46e00ad24030c9608cc73c57e9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003219"
---
# <a name="directorylistup-controlevent"></a>DirectoryListUp ControlEvent,

Este evento notifica al [control DirectoryList](directorylist-control.md) que el usuario desea seleccionar el elemento primario del directorio actual. Para obtener información relacionada, vea [cuadro de diálogo examinar](browse-dialog.md).

Este evento debe publicarse con un [control Pushbutton](pushbutton-control.md) situado en el mismo cuadro de diálogo que el control que se suscribe a este evento. El evento debe crearse en la [tabla ControlEvent,](controlevent-table.md).

Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) . Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida. Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).

Si el directorio actual es el directorio raíz de la unidad, un evento DirectoryListUp deshabilita cualquier otro control que publique un evento DirectoryListUp.

## <a name="published-by"></a>Publicado por

[DirectoryList](directorylist-control.md)

## <a name="argument"></a>Argumento

Este ControlEvent, no utiliza un argumento.

## <a name="action-on-subscribers"></a>Acción en los suscriptores

Este ControlEvent, no realiza ninguna acción en los suscriptores.

## <a name="typical-use"></a>Uso típico

Un control [Pushbutton](pushbutton-control.md) en el mismo cuadro de diálogo modal que el DirectoryList se usa para desencadenar la ejecución paso a paso en la ruta de acceso.

 

 



