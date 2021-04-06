---
title: Configurar el servicio de nombres para Windows 3. x o MS-DOS
description: Llamada a procedimiento remoto (RPC) y configurar el servicio de nombres para Windows 3. x o MS-DOS.
ms.assetid: 7b22a12e-43d0-4e32-a191-d63a56559143
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 533a0d8556f9cc51d0842768d0df1bdd0d553b5d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075878"
---
# <a name="configuring-the-name-service-for-windows-3x-or-ms-dos"></a>Configurar el servicio de nombres para Windows 3. x o MS-DOS

Al ejecutar Setup.exe para instalar la biblioteca en tiempo de ejecución de RPC de 16 bits, se le pide que seleccione un proveedor de servicios de nombres:

-   Si elige **instalar proveedor de servicios de nombres predeterminados**, se instalará el NSP predeterminado, localizador de Microsoft.
-   Si elige **instalar proveedor de servicios de nombres personalizados**, complete el cuadro de diálogo **definir dirección de red** para instalar el DCE servicio de directorio de celdas como NSP. El Servicio de directorio de celdas DCE es el NSP que se usa con servidores DCE.

La dirección de red es el nombre del equipo host que ejecuta el demonio NSI (NSID). Este equipo actúa como puerta de enlace al Servicio de directorio de celdas de DCE, pasando llamadas a la función NSI entre equipos que ejecutan sistemas operativos de Microsoft y equipos DCE. La dirección de red puede tener un máximo de 80 caracteres, por ejemplo, 11.1.9.169 es una dirección válida.

 

 




