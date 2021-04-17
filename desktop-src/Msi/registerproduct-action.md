---
description: La acción RegisterProduct registra la información del producto con el instalador y con agregar o quitar programas. Además, esta acción almacena el paquete de base de datos de Windows Installer en el equipo local.
ms.assetid: 689b09c7-9c17-42f5-ba31-cf9c6252e453
title: Acción RegisterProduct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5afa2d3e9f00f736b8c4c7864d8ec4baa3aa8ad9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677760"
---
# <a name="registerproduct-action"></a>Acción RegisterProduct

La acción RegisterProduct registra la información del producto con el instalador y con agregar o quitar programas. Además, esta acción almacena el paquete de base de datos de Windows Installer en el equipo local.

La acción RegisterProduct configura los controles que se muestran en Agregar o quitar programas en el panel de control. Para obtener más información, consulte [configuración de agregar o quitar programas con Windows Installer](configuring-add-remove-programs-with-windows-installer.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

No hay restricciones de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción            |
|-------|---------------------------------------|
| \[1\] | Información sobre el producto registrado. |



 

## <a name="remarks"></a>Observaciones

La acción RegisterProduct no se realiza durante la instalación en un punto de instalación administrativa.

 

 



