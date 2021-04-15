---
description: La acción ExecuteAction inicia la secuencia de ejecución mediante la propiedad EXECUTEACTION para determinar el tipo de instalación que se va a realizar.
ms.assetid: 61878317-ac87-4f6e-9375-12a78969e29e
title: Acción ExecuteAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2970a0fb4e9297264071769ac7415cd2acf866b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497794"
---
# <a name="executeaction-action"></a>Acción ExecuteAction

La acción ExecuteAction inicia la secuencia de ejecución mediante la propiedad [**ExecuteAction**](executeaction.md) para determinar el tipo de instalación que se va a realizar.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

Esta acción se debe secuenciar después de que se complete toda la recopilación de información necesaria para iniciar la instalación. Se pueden secuenciar acciones adicionales después de la acción ExecuteAction en la [tabla InstallUISequence](installuisequence-table.md)y la [tabla AdminUISequence](adminuisequence-table.md). Normalmente, una secuencia comienza con acciones de [*costo*](c-gly.md) , como la [acción CostInitialize](costinitialize-action.md), seguida de las acciones de la interfaz de usuario y, a continuación, la acción ExecuteAction.

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay mensajes ActionData.

## <a name="remarks"></a>Observaciones

La acción ExecuteAction se ejecuta con privilegios del sistema si está habilitado el servicio de instalador. Las acciones de nivel superior, como la [acción de instalación](install-action.md), la [acción de anuncio](advertise-action.md)y la acción de [Administrador](admin-action.md) incluyen lógica interna que determina si la llamada a la acción de ExecuteAction requiere la secuencia de ejecución o la secuencia de interfaz de usuario para ejecutarse.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tabla InstallUISequence](installuisequence-table.md)
</dt> <dt>

[Tabla AdminUISequence](adminuisequence-table.md)
</dt> <dt>

[Acción CostInitialize](costinitialize-action.md)
</dt> </dl>

 

 



