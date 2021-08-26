---
title: Configuración del servicio de nombres para Windows 3.x o MS-DOS
description: Llamada a procedimiento remoto (RPC) y configuración del servicio de nombres para Windows 3.x o MS-DOS.
ms.assetid: 7b22a12e-43d0-4e32-a191-d63a56559143
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24884c782913c47806c702ff129594c6524fe7c0e731561de405f3b6a360c7c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022435"
---
# <a name="configuring-the-name-service-for-windows-3x-or-ms-dos"></a>Configuración del servicio de nombres para Windows 3.x o MS-DOS

Al ejecutar Setup.exe para instalar la biblioteca en tiempo de ejecución rpc de 16 bits, se le pide que seleccione un proveedor de servicios de nombres:

-   Si elige Instalar **proveedor de servicios de nombre predeterminado**, se instalará el NSP predeterminado, Microsoft Locator.
-   Si elige Instalar proveedor de servicios  de nombres **personalizados,** complete el cuadro de diálogo Definir dirección de red para instalar el Servicio de directorio de celdas DCE como el NSP. El Servicio de directorio de celdas DCE es el NSP que se usa con los servidores DCE.

La dirección de red es el nombre del equipo host que ejecuta el demonio NSI (nsid). Este equipo actúa como puerta de enlace a la Servicio de directorio de celdas DCE, pasando llamadas de función NSI entre equipos que ejecutan sistemas operativos de Microsoft y equipos DCE. La dirección de red puede tener 80 caracteres o menos; por ejemplo, 11.1.9.169 es una dirección válida.

 

 




