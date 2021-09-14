---
description: La acción RegisterProduct registra la información del producto con el instalador y con Agregar o quitar programas. Además, esta acción almacena el paquete de base de Windows instalador en el equipo local.
ms.assetid: 689b09c7-9c17-42f5-ba31-cf9c6252e453
title: Acción RegisterProduct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5afa2d3e9f00f736b8c4c7864d8ec4baa3aa8ad9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069691"
---
# <a name="registerproduct-action"></a>Acción RegisterProduct

La acción RegisterProduct registra la información del producto con el instalador y con Agregar o quitar programas. Además, esta acción almacena el paquete de base de Windows instalador en el equipo local.

La acción RegisterProduct configura los controles mostrados por agregar o quitar programas en Panel de control. Para obtener más información, vea [Configuring Add/Remove Programs with Windows Installer](configuring-add-remove-programs-with-windows-installer.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

No hay restricciones de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción            |
|-------|---------------------------------------|
| \[1\] | Información sobre el producto registrado. |



 

## <a name="remarks"></a>Observaciones

La acción RegisterProduct no se realiza durante la instalación en un punto de instalación administrativa.

 

 



