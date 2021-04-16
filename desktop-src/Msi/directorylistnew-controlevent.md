---
description: Este evento notifica al control DirectoryList que se debe crear una nueva carpeta; crea la nueva carpeta y selecciona el campo de nombre de la carpeta para su edición.
ms.assetid: dc5859b9-f4b4-4ed7-93d5-369a3d2b9805
title: DirectoryListNew ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c99ce9398cb2780ab6042acb6ad6eaeeff83f6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105670000"
---
# <a name="directorylistnew-controlevent"></a>DirectoryListNew ControlEvent,

Este evento notifica al [control DirectoryList](directorylist-control.md) que se debe crear una nueva carpeta; crea la nueva carpeta y selecciona el campo de nombre de la carpeta para su edición. El nombre predeterminado de la nueva carpeta se puede crear en la [tabla UIText](uitext-table.md). Escriba "NuevaCarpeta" en la columna de clave. Escriba el valor del nombre predeterminado de la nueva carpeta en la columna de texto. Este valor debe tener el formato de un tipo de datos de columna de [nombre de archivo](filename.md) y usar la sintaxis de SFN \| LFN. Si este valor no se encuentra en la tabla UIText o es un valor no válido, el instalador usa un valor predeterminado de "FLDR \| nueva carpeta". Para obtener información relacionada, vea [cuadro de diálogo examinar](browse-dialog.md).

Este evento debe publicarse con un [control Pushbutton](pushbutton-control.md) situado en el mismo cuadro de diálogo que el control que se suscribe a este evento. El evento debe crearse en la [tabla ControlEvent,](controlevent-table.md).

Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) . Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida. Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).

Tenga en cuenta que si se vuelve a llamar a este ControlEvent, cuando ya existe una nueva carpeta, no se creará una segunda carpeta nueva. En este caso, al llamar a DirectoryListNew se selecciona el nombre de la nueva carpeta existente para su edición.

## <a name="published-by"></a>Publicado por

[DirectoryList](directorylist-control.md)

## <a name="argument"></a>Argumento

Este ControlEvent, no utiliza un argumento.

## <a name="action-on-subscribers"></a>Acción en los suscriptores

Este ControlEvent, no realiza ninguna acción en los suscriptores.

## <a name="typical-use"></a>Uso típico

Un control [Pushbutton](pushbutton-control.md) en el mismo cuadro de diálogo modal que el DirectoryList se usa para desencadenar la creación de una nueva carpeta.

 

 



