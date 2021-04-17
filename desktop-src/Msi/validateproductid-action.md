---
description: La Acción ValidateProductID establece la propiedad ProductID en el identificador de producto completo.
ms.assetid: 31b2f9d2-98d5-4cf3-af02-f12de2740bb8
title: Acción ValidateProductID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4d0f9f58641e8e24d73a1acae0b79cc0b875aba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652460"
---
# <a name="validateproductid-action"></a>Acción ValidateProductID

La Acción ValidateProductID establece la propiedad [**ProductID**](productid.md) en el identificador de producto completo.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

Esta acción se debe secuenciar antes del Asistente para la interfaz de usuario en la [tabla InstallUISequence](installuisequence-table.md) y antes de la [acción RegisterUser](registeruser-action.md) en la [tabla InstallExecuteSequence](installexecutesequence-table.md).

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay mensajes ActionData.

## <a name="remarks"></a>Observaciones

El instalador comprueba si un producto se ha validado correctamente mediante la comprobación de la propiedad [**ProductID**](productid.md) . El instalador establece la propiedad **ProductID** en el identificador de producto completo después de una validación correcta. La Acción ValidateProductID no hace nada si la propiedad **ProductID** ya se ha establecido mediante una validación correcta u otro método.

La Acción ValidateProductID siempre devuelve un resultado correcto, tanto si el identificador de producto es válido como si no, para que el identificador de producto se pueda escribir en la línea de comandos la primera vez que se ejecute el producto.

El identificador de producto se puede validar sin que el usuario vuelva a escribir esta información estableciendo la propiedad [**PIDKEY**](pidkey.md) en la línea de comandos o mediante una transformación. La presentación del cuadro de diálogo que solicita al usuario que escriba el identificador de producto se puede hacer condicional según la presencia de la propiedad [**ProductID**](productid.md) , que se establece cuando se valida la propiedad **PIDKEY** .

 

 



