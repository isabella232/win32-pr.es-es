---
title: Configuración del servicio de nombres para Windows 3.x o MS-DOS
description: Llamada a procedimiento remoto (RPC) y configuración del servicio de nombres para Windows 3.x o MS-DOS.
ms.assetid: 7b22a12e-43d0-4e32-a191-d63a56559143
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 533a0d8556f9cc51d0842768d0df1bdd0d553b5d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069162"
---
# <a name="configuring-the-name-service-for-windows-3x-or-ms-dos"></a>Configuración del servicio de nombres para Windows 3.x o MS-DOS

Al ejecutar Setup.exe instalar la biblioteca en tiempo de ejecución rpc de 16 bits, se le pide que seleccione un proveedor de servicios de nombres:

-   Si elige Instalar **proveedor de servicios de nombre predeterminado**, se instala el NSP predeterminado, Microsoft Locator.
-   Si elige Instalar proveedor de servicios  de nombres **personalizados,** complete el cuadro de diálogo Definir dirección de red para instalar el Servicio de directorio de celdas DCE como NSP. El nombre Servicio de directorio de celdas DCE es el NSP que se usa con los servidores DCE.

La dirección de red es el nombre del equipo host que ejecuta el demonio NSI (nsid). Este equipo actúa como puerta de enlace a la Servicio de directorio de celdas DCE, pasando llamadas de función NSI entre equipos que ejecutan sistemas operativos de Microsoft y equipos DCE. La dirección de red puede tener 80 caracteres o menos, por ejemplo, 11.1.9.169 es una dirección válida.

 

 




