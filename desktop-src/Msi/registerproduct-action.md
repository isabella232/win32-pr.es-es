---
description: La acción RegisterProduct registra la información del producto con el instalador y con Agregar o quitar programas. Además, esta acción almacena el paquete de base de Windows instalador en el equipo local.
ms.assetid: 689b09c7-9c17-42f5-ba31-cf9c6252e453
title: Acción RegisterProduct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 185b670b7a24c31e6dc5adb402cd6c557e2eba9eac3db5138744cd1e827113ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375969"
---
# <a name="registerproduct-action"></a>Acción RegisterProduct

La acción RegisterProduct registra la información del producto con el instalador y con Agregar o quitar programas. Además, esta acción almacena el paquete de base de Windows instalador en el equipo local.

La acción RegisterProduct configura los controles mostrados por el comando Agregar o quitar programas en Panel de control. Para obtener más información, [vea Configuring Add/Remove Programs with Windows Installer](configuring-add-remove-programs-with-windows-installer.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

No hay restricciones de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción            |
|-------|---------------------------------------|
| \[1\] | Información sobre el producto registrado. |



 

## <a name="remarks"></a>Comentarios

La acción RegisterProduct no se realiza durante la instalación en un punto de instalación administrativa.

 

 



