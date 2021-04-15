---
title: Editar secuencias
description: Editar secuencias
ms.assetid: 1653ff90-e96a-43fc-b509-6d8ad4ddcd2c
keywords:
- CreateEditableStream función)
- EditStreamCut función)
- EditStreamCopy función)
- EditStreamPaste función)
- EditStreamClone función)
- EditStreamSetInfo función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29eb687eb36ff9dfe0b1d3477bff095bdd78a135
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486894"
---
# <a name="editing-streams"></a>Editar secuencias

Puede crear una secuencia que se puede editar mediante la función [**CreateEditableStream**](/windows/desktop/api/Vfw/nf-vfw-createeditablestream) . Esta función inicializa el entorno para editar una secuencia. Esto incluye la creación de una interfaz para el nuevo flujo y las tablas de edición internas que realizan el seguimiento de los cambios realizados en la secuencia. **CreateEditableStream** devuelve un puntero de secuencia a una secuencia editable que es necesaria para otras funciones de edición de secuencias. El puntero de secuencia editable también lo pueden usar otras funciones AVIFile que aceptan punteros de secuencia.

Puede cortar uno o más ejemplos de una secuencia modificable mediante la función [**EditStreamCut**](/windows/desktop/api/Vfw/nf-vfw-editstreamcut) . Para quitar ejemplos de la secuencia editable, esta función agrega una entrada a la tabla de edición. A continuación, la función coloca una copia de los ejemplos de corte en una nueva secuencia temporal cuyo puntero de interfaz se devuelve en una variable.

Puede copiar uno o más ejemplos de una secuencia modificable en una secuencia temporal mediante la función [**EditStreamCopy**](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy) . **EditStreamCopy** coloca copias de los ejemplos en una nueva secuencia temporal cuyo puntero de interfaz se devuelve en una variable.

Puede copiar uno o más ejemplos de una secuencia y pegarlos en una secuencia modificable mediante la función [**EditStreamPaste**](/windows/desktop/api/Vfw/nf-vfw-editstreampaste) . Para insertar los ejemplos en la posición especificada, esta función agrega una entrada en la tabla de edición de la secuencia modificable de destino.

Puede duplicar una secuencia modificable mediante la función [**EditStreamClone**](/windows/desktop/api/Vfw/nf-vfw-editstreamclone) . Esta función devuelve un puntero a la interfaz de flujo de la nueva secuencia. Puede copiar estos flujos en el portapapeles o utilizarlos para mantener un rastro de las ediciones realizadas en un flujo.

Puede cambiar algunas de las características de una secuencia modificable mediante la función [**EditStreamSetInfo**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetinfoa) . Esta función actualiza la configuración de prioridad, el idioma, la escala y la velocidad, la hora de inicio, la configuración de calidad, las coordenadas y las dimensiones del rectángulo de destino, y la descripción textual de la secuencia. Estos elementos se almacenan en la estructura [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) asociada al flujo modificable.

También puede cambiar la descripción textual de una secuencia modificable mediante la función [**EditStreamSetName**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetnamea) . Esta función actualiza el miembro **szName** de la estructura **AVISTREAMINFO** asociada al flujo modificable.

Las funciones de edición funcionan en secuencias. Debe cortar y pegar cada flujo individualmente y, a continuación, usar la función [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) para crear un nuevo puntero de archivo.

> [!Note]  
> Las tablas de edición de una secuencia modificable mantienen todos los cambios de una secuencia. La secuencia de origen nunca cambia.

 

 

 




