---
description: La acción ValidateProductID establece la propiedad ProductID en el identificador de producto completo.
ms.assetid: 31b2f9d2-98d5-4cf3-af02-f12de2740bb8
title: Acción ValidateProductID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4d0f9f58641e8e24d73a1acae0b79cc0b875aba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473894"
---
# <a name="validateproductid-action"></a>Acción ValidateProductID

La acción ValidateProductID establece la [**propiedad ProductID**](productid.md) en el identificador de producto completo.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

Esta acción debe secuenciarse antes que el Asistente para la interfaz de usuario en la tabla [InstallUISequence](installuisequence-table.md) y antes de la acción [RegisterUser](registeruser-action.md) en la [tabla InstallExecuteSequence](installexecutesequence-table.md).

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay ningún mensaje ActionData.

## <a name="remarks"></a>Observaciones

El instalador comprueba si un producto se ha validado correctamente comprobando la [**propiedad ProductID.**](productid.md) El instalador establece la **propiedad ProductID** en el identificador completo del producto después de una validación correcta. La acción ValidateProductID no hace nada si la **propiedad ProductID** ya se ha establecido mediante una validación correcta o por otro método.

La acción ValidateProductID siempre devuelve un resultado correcto, independientemente de si el identificador del producto es válido o no, para que el identificador del producto se pueda especificar en la línea de comandos la primera vez que se ejecute el producto.

El identificador del producto se puede validar sin que el usuario vuelva a escribir esta información estableciendo la [**propiedad PIDKEY**](pidkey.md) en la línea de comandos o mediante una transformación. La presentación del cuadro de diálogo en el que se solicita al usuario que escriba el identificador del producto se puede hacer condicional después de la presencia de la propiedad [**ProductID,**](productid.md) que se establece cuando se valida la **propiedad PIDKEY.**

 

 



