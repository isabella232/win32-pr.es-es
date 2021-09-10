---
title: Edición Secuencias
description: Edición Secuencias
ms.assetid: 1653ff90-e96a-43fc-b509-6d8ad4ddcd2c
keywords:
- Función CreateEditableStream
- Función EditStreamCut
- Función EditStreamCopy
- Función EditStreamPaste
- Función EditStreamClone
- Función EditStreamSetInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29eb687eb36ff9dfe0b1d3477bff095bdd78a135
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372206"
---
# <a name="editing-streams"></a>Edición Secuencias

Puede crear una secuencia que puede editar mediante la [**función CreateEditableStream.**](/windows/desktop/api/Vfw/nf-vfw-createeditablestream) Esta función inicializa el entorno para editar una secuencia. Esto incluye la creación de una interfaz para la nueva secuencia y tablas de edición internas que realizan un seguimiento de los cambios realizados en la secuencia. **CreateEditableStream** devuelve un puntero de secuencia a una secuencia editable que requieren otras funciones de edición de secuencias. Otras funciones AVIFile que aceptan punteros de secuencia también pueden usar el puntero de secuencia editable.

Puede cortar uno o varios ejemplos de una secuencia editable mediante la [**función EditStreamCut.**](/windows/desktop/api/Vfw/nf-vfw-editstreamcut) Para quitar ejemplos de la secuencia editable, esta función agrega una entrada a la tabla de edición. A continuación, la función coloca una copia de los ejemplos de corte en una nueva secuencia temporal cuyo puntero de interfaz se devuelve en una variable.

Puede copiar uno o varios ejemplos de una secuencia editable en una secuencia temporal mediante la [**función EditStreamCopy.**](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy) **EditStreamCopy coloca** copias de los ejemplos en una nueva secuencia temporal cuyo puntero de interfaz se devuelve en una variable.

Puede copiar uno o varios ejemplos de una secuencia y pegarlos en una secuencia editable mediante la [**función EditStreamPaste.**](/windows/desktop/api/Vfw/nf-vfw-editstreampaste) Para insertar los ejemplos en la posición especificada, esta función agrega una entrada en la tabla de edición de la secuencia editable de destino.

Puede duplicar una secuencia editable mediante la [**función EditStreamClone.**](/windows/desktop/api/Vfw/nf-vfw-editstreamclone) Esta función devuelve un puntero a la interfaz de secuencia de la nueva secuencia. Puede copiar estas secuencias en el Portapapeles o usarlas para mantener un seguimiento de las modificaciones realizadas en una secuencia.

Puede cambiar varias de las características de una secuencia editable mediante la [**función EditStreamSetInfo.**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetinfoa) Esta función actualiza la configuración de prioridad, el idioma, la escala y la velocidad, la hora de inicio, la configuración de calidad, las dimensiones y coordenadas del rectángulo de destino y la descripción textual de la secuencia. Estos elementos se almacenan en la [**estructura AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) asociada a la secuencia editable.

También puede cambiar la descripción textual de una secuencia editable mediante la [**función EditStreamSetName.**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetnamea) Esta función actualiza el **miembro szName** de la **estructura AVISTREAMINFO** asociada a la secuencia editable.

Las funciones de edición funcionan en secuencias. Debe cortar y pegar cada secuencia individualmente y, a continuación, usar la [**función AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) para crear un nuevo puntero de archivo.

> [!Note]  
> Las tablas de edición de una secuencia editable mantienen todos los cambios de una secuencia. La secuencia de origen nunca cambia.

 

 

 




