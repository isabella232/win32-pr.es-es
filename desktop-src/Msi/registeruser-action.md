---
description: La acción RegisterUser registra la información del usuario con el instalador para identificar al usuario de un producto.
ms.assetid: da615cb4-d36d-4180-8f97-c9f83c0df1c6
title: Acción RegisterUser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 686628d29094f951994b072ad4451a383a405965
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069680"
---
# <a name="registeruser-action"></a>Acción RegisterUser

La acción RegisterUser registra la información del usuario con el instalador para identificar al usuario de un producto.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

No hay restricciones de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción   |
|-------|------------------------------|
| \[1\] | Información de usuario registrada. |



 

## <a name="remarks"></a>Observaciones

La acción RegisterUser no se realiza durante una instalación administrativa. Si la acción [ValidateProductID](validateproductid-action.md)no valida el identificador de producto especificado por el usuario , la propiedad [**ProductID**](productid.md) no se establece y esta acción no hace nada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**NOMBRE DE USUARIO**](username.md)
</dt> <dt>

[**COMPANYNAME**](companyname.md)
</dt> <dt>

[**Productid**](productid.md)
</dt> </dl>

 

 



