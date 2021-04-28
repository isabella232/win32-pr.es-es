---
description: '<span id="vspixengine.callbackcommandtype"></span>Enumeración CallbackCommandType: enumeración que se usa para comunicarse entre el motor de captura y un host (como Visual Studio Diagnóstico de gráficos).'
MS-HAID: vspixengine.CallbackCommandType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumeración CallbackCommandType
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 78E0CD6C-5264-4F66-BAB9-20DC9C0C1EC1
api_name:
- CallbackCommandType
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 85e1b7d396d125add00824e9b7c94086e0da6be2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090133"
---
# <a name="span-idvspixenginecallbackcommandtypespancallbackcommandtype-enumeration"></a><span id="vspixengine.callbackcommandtype"></span>Enumeración CallbackCommandType

Enumeración que se usa para comunicarse entre el motor de captura y un host (por ejemplo, Visual Studio Diagnóstico de gráficos).

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>Constantes

<span id="BeginCommunicationCallback"></span><span id="begincommunicationcallback"></span><span id="BEGINCOMMUNICATIONCALLBACK"></span>**BeginCommunicationCallback**  
Resultados de BeginCommunication.

<span id="ErrorListCallback"></span><span id="errorlistcallback"></span><span id="ERRORLISTCALLBACK"></span>**ErrorListCallback**  
Errores.

<span id="WarningListCallback"></span><span id="warninglistcallback"></span><span id="WARNINGLISTCALLBACK"></span>**WarningListCallback**  
Advertencias.

<span id="MessagesCallback"></span><span id="messagescallback"></span><span id="MESSAGESCALLBACK"></span>**MessagesCallback**  
Mensajes.

<span id="RunExperimentCallback"></span><span id="runexperimentcallback"></span><span id="RUNEXPERIMENTCALLBACK"></span>**RunExperimentCallback**  
Resultado de RunExperiment.

<span id="RunActionCallback"></span><span id="runactioncallback"></span><span id="RUNACTIONCALLBACK"></span>**RunActionCallback**  
Resultado de RunAction.

<span id="NewFramesCallback"></span><span id="newframescallback"></span><span id="NEWFRAMESCALLBACK"></span>**NewFramesCallback**  
Valor que indica una devolución de llamada a la que se llamará cuando se hayan capturado nuevos fotogramas y estén listos para mostrarse.

<span id="BeginCommunicationCallbackLegacy"></span><span id="begincommunicationcallbacklegacy"></span><span id="BEGINCOMMUNICATIONCALLBACKLEGACY"></span>**BeginCommunicationCallbackLegacy**  
Resultados de una versión anterior de BeginCommunication usada en Windows 7 y Windows 8.

<span id="RunExperimentStatusCallback"></span><span id="runexperimentstatuscallback"></span><span id="RUNEXPERIMENTSTATUSCALLBACK"></span>**RunExperimentStatusCallback**  
Resultado de RunExpplotmentProgress.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



