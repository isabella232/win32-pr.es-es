---
description: Enumeración que se usa para indicar qué versión del protocul de comunicación remota se usa.
MS-HAID: vspixengine.REMOTINGVERSION
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: REMOTINGVERSION (enumeración)
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
ms.openlocfilehash: 121342a2c0d47b2041893459d577e09e3b4d73ba
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627241"
---
# <a name="span-idvspixengineremotingversionspanremotingversion-enumeration"></a><span id="vspixengine.remotingversion"></span>REMOTINGVERSION (enumeración)

Enumeración que se usa para indicar qué versión del protocul de comunicación remota se usa.

## <a name="syntax"></a>Sintaxis


```C++
};
```

## <a name="constants"></a>Constantes

<span id="REMOTING_DEV12"></span><span id="remoting_dev12"></span>**REMOTING \_ DEV12**  
Valor que indica que se usa Visual Studio 2013 protocolo de comunicación remota RTM.

<span id="REMOTING_DEV12_UPDATE_1"></span><span id="remoting_dev12_update_1"></span>**REMOTING \_ DEV12 \_ UPDATE \_ 1**  
Valor que indica que se usa Visual Studio 2013 protocolo de comunicación remota update 1.

<span id="REMOTING_DEV12_UPDATE_4"></span><span id="remoting_dev12_update_4"></span>**REMOTING \_ DEV12 \_ UPDATE \_ 4**  
Valor que indica que se está Visual Studio 2013 Update 4 protocolo de comunicación remota.

<span id="REMOTING_DEV14"></span><span id="remoting_dev14"></span>**REMOTING \_ DEV14**  
Valor que indica que se usa Visual Studio protocolo de comunicación remota RTM 2015.

<span id="REMOTING_WIN10"></span><span id="remoting_win10"></span>**COMUNICACIÓN REMOTA \_ WIN10**  
Valor que indica que se usa Windows 10 de comunicación remota (a partir de Windows 10, el diagnóstico de gráficos es un componente del sistema operativo).

<span id="REMOTING_WIN10_JAN_2015"></span><span id="remoting_win10_jan_2015"></span>**COMUNICACIÓN REMOTA \_ WIN10 \_ \_ ENE 2015**  
Valor que indica que se está Windows 10 protocolo de comunicación remota Windows 10 (enero de 2015).

<span id="REMOTING_WIN10_JAN_2015_1"></span><span id="remoting_win10_jan_2015_1"></span>**COMUNICACIÓN REMOTA \_ WIN10 \_ \_ ENE 2015 \_ 1**  
Valor que indica que se está Windows 10 protocolo de comunicación remota (enero de 2015, v1).

<span id="REMOTING_WIN10_JAN_2015_2"></span><span id="remoting_win10_jan_2015_2"></span>**COMUNICACIÓN REMOTA \_ WIN10 \_ \_ ENE 2015 \_ 2**  
Valor que indica que se está Windows 10 protocolo de comunicación remota (enero de 2015, v2). Esta versión del protocolo introdujo solicitudes para visualizar los recursos en mosaico.

<span id="REMOTING_WIN10_JAN_2015_3"></span><span id="remoting_win10_jan_2015_3"></span>**COMUNICACIÓN REMOTA \_ WIN10 \_ \_ ENE 2015 \_ 3**  
Valor que indica que se está Windows 10 protocolo de comunicación remota (enero de 2015, v3). Esta versión del protocolo introdujo IPixEngine7, ahora en desuso, para comprobar la compatibilidad con la versión de la interfaz.

<span id="REMOTING_IPIXENGINE7_VERSION_CHECKING"></span><span id="remoting_ipixengine7_version_checking"></span>**COMPROBACIÓN DE \_ VERSIONES DE IPIXENGINE7 \_ DE COMUNICACIÓN \_ REMOTA**  
Valor que indica que se está Windows 10 protocolo de comunicación remota (enero de 2015, v1). Esta versión del protocolo no depende de REMOTINGVERSION para mediar las funcionalidades del protocolo. El GUID de interfaz ahora cambia cuando no es público int

<span id="REMOTING_WIN10_FEB_2015_1"></span><span id="remoting_win10_feb_2015_1"></span>**COMUNICACIÓN REMOTA \_ WIN10 \_ FEB \_ 2015 \_ 1**  
Valor que indica que se está Windows 10 protocolo de comunicación remota (enero de 2015, v1). Esta versión del protocolo presenta propiedades de información de resumen con identificadores únicos y fijos.

<span id="REMOTING_WIN10_2015_03_00"></span><span id="remoting_win10_2015_03_00"></span>**COMUNICACIÓN \_ REMOTA WIN10 \_ 2015 \_ 03 \_ 00**  
Valor que indica que se está Windows 10 protocolo de comunicación remota (enero de 2015, v1). Esta versión del protocolo introdujo compatibilidad con la ventana de estado DirectX11.

<span id="REMOTING_LATES"></span><span id="remoting_lates"></span>**RETRASOS \_ DE COMUNICACIÓN REMOTA**  
Valor que indica que se usa el protocolo de comunicación remota más reciente.

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



