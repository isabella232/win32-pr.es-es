---
description: Enumeración que se usa para indicar qué versión del protocul remoto se está usando.
MS-HAID: vspixengine.REMOTINGVERSION
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumeración REMOTINGVERSION
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 598E9586-05FF-4889-BBAF-44814EEF203A
api_name:
- REMOTINGVERSION
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a813453f9b5d1a89525e5b67cc22659281d04cb5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104359917"
---
# <a name="span-idvspixengineremotingversionspanremotingversion-enumeration"></a><span id="vspixengine.remotingversion"></span>Enumeración REMOTINGVERSION

Enumeración que se usa para indicar qué versión del protocul remoto se está usando.

## <a name="syntax"></a>Sintaxis


```C++
};
```

## <a name="constants"></a>Constantes

<span id="REMOTING_DEV12"></span><span id="remoting_dev12"></span>**\_De remoto**  
Un valor que indica que se está usando el protocolo de comunicación remota de Visual Studio 2013 RTM.

<span id="REMOTING_DEV12_UPDATE_1"></span><span id="remoting_dev12_update_1"></span>**Comunicación remota \_ de \_ Update \_ 1**  
Un valor que indica que se está usando el protocolo de comunicación remota de Visual Studio 2013 Update 1.

<span id="REMOTING_DEV12_UPDATE_4"></span><span id="remoting_dev12_update_4"></span>**Comunicación remota \_ de \_ Update \_ 4**  
Valor que indica que se está usando el protocolo de comunicación remota de Visual Studio 2013 Update 4.

<span id="REMOTING_DEV14"></span><span id="remoting_dev14"></span>**\_DEV14 remoto**  
Un valor que indica que se está usando el protocolo de comunicación remota de Visual Studio 2015 RTM.

<span id="REMOTING_WIN10"></span><span id="remoting_win10"></span>**\_WIN10 remoto**  
Un valor que indica que se está usando el protocolo de comunicación remota de Windows 10 (a partir de Windows 10, el diagnóstico de gráficos es un componente del sistema operativo)

<span id="REMOTING_WIN10_JAN_2015"></span><span id="remoting_win10_jan_2015"></span>**REMOting \_ WIN10 \_ Jan \_ 2015**  
Un valor que indica que se está usando el protocolo de comunicación remota de Windows 10 (enero de 2015).

<span id="REMOTING_WIN10_JAN_2015_1"></span><span id="remoting_win10_jan_2015_1"></span>**REMOting \_ WIN10 \_ Jan \_ 2015 \_ 1**  
Un valor que indica que se está usando el protocolo de comunicación remota de Windows 10 (enero de 2015, V1).

<span id="REMOTING_WIN10_JAN_2015_2"></span><span id="remoting_win10_jan_2015_2"></span>**REMOting \_ WIN10 \_ Jan \_ 2015 \_ 2**  
Un valor que indica que se está usando el protocolo de comunicación remota de Windows 10 (enero de 2015, V2). Esta versión del protocolo presentó solicitudes para visualizar los recursos en mosaico.

<span id="REMOTING_WIN10_JAN_2015_3"></span><span id="remoting_win10_jan_2015_3"></span>**Comunicación remota \_ WIN10 \_ Jan \_ 2015 \_ 3**  
Un valor que indica que se está usando el protocolo de comunicación remota de Windows 10 (enero de 2015, V3). Esta versión del protocolo presentó IPixEngine7, ahora en desuso, para comprobar la compatibilidad de la versión de la interfaz.

<span id="REMOTING_IPIXENGINE7_VERSION_CHECKING"></span><span id="remoting_ipixengine7_version_checking"></span>**Comprobación de la versión de REMOting \_ IPIXENGINE7 \_ \_**  
Un valor que indica que se está usando el protocolo de comunicación remota de Windows 10 (enero de 2015, V1). Esta versión del Protocolo se aparta de confiar en REMOTINGVERSION a las capacidades del Protocolo de mediación. El GUID de la interfaz se cambia ahora cuando no es público.

<span id="REMOTING_WIN10_FEB_2015_1"></span><span id="remoting_win10_feb_2015_1"></span>**Comunicación remota de \_ WIN10 de \_ febrero de \_ 2015 \_ 1**  
Un valor que indica que se está usando el protocolo de comunicación remota de Windows 10 (enero de 2015, V1). Esta versión del Protocolo introduce propiedades de información de resumen con identificadores únicos y fijos.

<span id="REMOTING_WIN10_2015_03_00"></span><span id="remoting_win10_2015_03_00"></span>**REMOting \_ WIN10 \_ 2015 \_ 03 \_ 00**  
Un valor que indica que se está usando el protocolo de comunicación remota de Windows 10 (enero de 2015, V1). Esta versión del protocolo incorporó la compatibilidad con la ventana de estado DirectX11.

<span id="REMOTING_LATES"></span><span id="remoting_lates"></span>**comunicación remota \_ tardía**  
Valor que indica que se está usando el protocolo de comunicación remota más reciente.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



