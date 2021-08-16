---
description: Net.exe se puede usar para detener e iniciar el protocolo IPv6.
ms.assetid: faa555d9-eb20-4b7a-94eb-b67a48ee630e
title: Net.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29ab08a69590d6cf53a42096bf12d2e8657c571fd27b637feca4c51c61354225
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741082"
---
# <a name="netexe"></a>Net.exe

Net.exe se puede usar para detener e iniciar el protocolo IPv6. Al reiniciar IPv6, se reinicializa el protocolo como si el equipo se estuviera reiniciando, lo que puede cambiar los números de interfaz. Net.exe tiene muchos subcomandos. Los siguientes comandos son relevantes para IPv6:

<dl> <dt>

<span id="net_stop_tcpip6"></span><span id="NET_STOP_TCPIP6"></span>**net stop tcpip6**
</dt> <dd>

Detiene el protocolo IPv6 y lo descarga de la memoria. Este comando produce un error si hay algún socket IPv6 abierto.

</dd> <dt>

<span id="net_start_tcpip6"></span><span id="NET_START_TCPIP6"></span>**net start tcpip6**
</dt> <dd>

Inicia el protocolo IPv6 si se ha detenido. Si hay un nuevo Tcpip6.sys de controlador en el directorio %systemroot% \\ System32 Drivers, se carga \\ ese archivo de controlador.

</dd> </dl>

 

 



