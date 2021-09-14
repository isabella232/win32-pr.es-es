---
description: Net.exe se puede usar para detener e iniciar el protocolo IPv6.
ms.assetid: faa555d9-eb20-4b7a-94eb-b67a48ee630e
title: Net.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5074696b71ce000ef330f2c88fceef0f60b0222e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249368"
---
# <a name="netexe"></a>Net.exe

Net.exe se puede usar para detener e iniciar el protocolo IPv6. Al reiniciar IPv6, se reinicializa el protocolo como si el equipo se reiniciara, lo que puede cambiar los números de interfaz. Net.exe tiene muchos subcomandos. Los siguientes comandos son relevantes para IPv6:

<dl> <dt>

<span id="net_stop_tcpip6"></span><span id="NET_STOP_TCPIP6"></span>**net stop tcpip6**
</dt> <dd>

Detiene el protocolo IPv6 y lo descarga de la memoria. Se produce un error en este comando si hay algún socket IPv6 abierto.

</dd> <dt>

<span id="net_start_tcpip6"></span><span id="NET_START_TCPIP6"></span>**net start tcpip6**
</dt> <dd>

Inicia el protocolo IPv6 si se detuvo. Si hay un nuevo Tcpip6.sys controlador en el directorio %systemroot% \\ System32 Drivers, se carga \\ ese archivo de controlador.

</dd> </dl>

 

 



