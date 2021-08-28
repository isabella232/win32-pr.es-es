---
description: '<span id="vspixengine.remotecommandtype"></span>Enumeración RemoteCommandType: enumeración que se usa para comunicarse entre el motor de captura y un host (como Visual Studio Diagnóstico de gráficos).'
MS-HAID: vspixengine.RemoteCommandType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: RemoteCommandType (enumeración)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B517F70C-2BFB-42E7-8597-AC5915AB2DE0
api_name:
- RemoteCommandType
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 73accd6f73a7c33219c83a3285837d2e1c7c133a
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631723"
---
# <a name="span-idvspixengineremotecommandtypespanremotecommandtype-enumeration"></a><span id="vspixengine.remotecommandtype"></span>RemoteCommandType (enumeración)

Enumeración que se usa para comunicarse entre el motor de captura y un host (por ejemplo, Visual Studio Diagnóstico de gráficos).

## <a name="syntax"></a>Sintaxis


```C++
};
```

## <a name="constants"></a>Constantes

<span id="BeginCommunication"></span><span id="begincommunication"></span><span id="BEGINCOMMUNICATION"></span>**BeginCommunication**  
Inicia la comunicación.

<span id="RunExperiment"></span><span id="runexperiment"></span><span id="RUNEXPERIMENT"></span>**RunExperiment**  
Inicia una Diagnóstico de gráficos de captura de datos (un experimento).

<span id="RunAction"></span><span id="runaction"></span><span id="RUNACTION"></span>**RunAction**  
Inicia una captura (igual que al pulsar la pantalla de impresión). Enviado por un host al capturar un fotograma.

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



