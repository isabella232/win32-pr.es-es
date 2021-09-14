---
description: La acción ExecuteAction inicia la secuencia de ejecución mediante la propiedad EXECUTEACTION para determinar qué tipo de instalación se va a realizar.
ms.assetid: 61878317-ac87-4f6e-9375-12a78969e29e
title: Acción ExecuteAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2970a0fb4e9297264071769ac7415cd2acf866b9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158434"
---
# <a name="executeaction-action"></a>Acción ExecuteAction

La acción ExecuteAction inicia la secuencia de ejecución mediante la [**propiedad EXECUTEACTION**](executeaction.md) para determinar qué tipo de instalación se va a realizar.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

Esta acción debe secuenciarse una vez completada toda la recopilación de información necesaria para iniciar la instalación. Se pueden secuenciar acciones adicionales después de la acción ExecuteAction en la [tabla InstallUISequence](installuisequence-table.md)y la [tabla AdminUISequence](adminuisequence-table.md). Normalmente, una secuencia [](c-gly.md) comienza con acciones de cálculo del costo, como la acción [CostInitialize](costinitialize-action.md), seguidas de las acciones de la interfaz de usuario y, a continuación, la acción ExecuteAction.

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay ningún mensaje ActionData.

## <a name="remarks"></a>Observaciones

La acción ExecuteAction se ejecuta con privilegios del sistema si el servicio de instalador está habilitado. Las acciones de nivel superior, como la acción [INSTALL](install-action.md), la acción [ADVERTISE](advertise-action.md)y la acción [ADMIN](admin-action.md) incluyen lógica interna que determina si la llamada a la acción ExecuteAction requiere que se ejecute la secuencia de ejecución o la secuencia de la interfaz de usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tabla InstallUISequence](installuisequence-table.md)
</dt> <dt>

[Tabla AdminUISequence](adminuisequence-table.md)
</dt> <dt>

[Acción CostInitialize](costinitialize-action.md)
</dt> </dl>

 

 



