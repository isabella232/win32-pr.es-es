---
description: La acción RegisterUser registra la información del usuario con el instalador para identificar al usuario de un producto.
ms.assetid: da615cb4-d36d-4180-8f97-c9f83c0df1c6
title: Acción RegisterUser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f89d43d18839e806939b7a084d37840b9895fdc81efb79fc03867eebe4c5c57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626720"
---
# <a name="registeruser-action"></a>Acción RegisterUser

La acción RegisterUser registra la información del usuario con el instalador para identificar al usuario de un producto.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

No hay restricciones de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción   |
|-------|------------------------------|
| \[1\] | Información de usuario registrada. |



 

## <a name="remarks"></a>Comentarios

La acción RegisterUser no se realiza durante una instalación administrativa. Si la acción [ValidateProductID](validateproductid-action.md)no valida el identificador de producto especificado por el usuario , la propiedad [**ProductID**](productid.md) no se establece y esta acción no hace nada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**nombre de usuario**](username.md)
</dt> <dt>

[**Companyname**](companyname.md)
</dt> <dt>

[**Productid**](productid.md)
</dt> </dl>

 

 



