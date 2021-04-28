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
ms.openlocfilehash: ed57b9b044613351e99096a8c8cb741b8ad7a269
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110513"
---
# <a name="span-idvspixengineremotecommandtypespanremotecommandtype-enumeration"></a><span id="vspixengine.remotecommandtype"></span>RemoteCommandType (enumeración)

Enumeración que se usa para comunicarse entre el motor de captura y un host (por ejemplo, Visual Studio Diagnóstico de gráficos).

## <a name="syntax"></a>Syntax


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

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



