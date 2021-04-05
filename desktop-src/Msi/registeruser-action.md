---
description: La acción RegisterUser registra la información del usuario con el instalador para identificar al usuario de un producto.
ms.assetid: da615cb4-d36d-4180-8f97-c9f83c0df1c6
title: RegisterUser (acción)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 686628d29094f951994b072ad4451a383a405965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813643"
---
# <a name="registeruser-action"></a>RegisterUser (acción)

La acción RegisterUser registra la información del usuario con el instalador para identificar al usuario de un producto.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

No hay restricciones de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción   |
|-------|------------------------------|
| \[1\] | Información de usuario registrada. |



 

## <a name="remarks"></a>Observaciones

La acción RegisterUser no se realiza durante una instalación administrativa. Si el identificador de producto especificado por el usuario no se ha validado mediante la [Acción ValidateProductID](validateproductid-action.md), no se establece la propiedad [**ProductID**](productid.md) y esta acción no hace nada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**NOMBRE**](username.md)
</dt> <dt>

[**COMPAÑÍA**](companyname.md)
</dt> <dt>

[**IdProducto**](productid.md)
</dt> </dl>

 

 



