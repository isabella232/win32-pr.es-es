---
description: Representa información sobre un experimento (captura).
MS-HAID: vspixengine.Experiment
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estructura del experimento
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 632F1F92-3E32-4B0A-8E38-2613694C267F
api_name:
- Experiment
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e932d2f2b60a72ca167f3f6edd7f4ddae9b68710
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805983"
---
# <a name="span-idvspixengineexperimentspanexperiment-structure"></a><span id="vspixengine.experiment"></span>Estructura del experimento

Representa información sobre un experimento (captura).

## <a name="syntax"></a>Sintaxis


```C++
} Experiment;
```

## <a name="members"></a>Miembros

**processId**  
IDENTIFICADOR del proceso asociado.

**applicationName**  
Cadena COM que contiene el nombre de la aplicación en la que se va a ejecutar el experimento.

**commandLineArguments**  
Cadena COM que contiene los argumentos de la línea de comandos.

**workingDirectory**  
Cadena COM que contiene la ruta de acceso del directorio de trabajo.

**tempPixRunFile**  
Cadena COM que contiene la ruta de acceso del archivo temporal que se usa para realizar el experimento.

**startOption**  
Opción de inicio asociada al experimento.

**experimentType**  
El tipo de experimento (captura).

**uiLocale**  
IDENTIFICADOR de la configuración regional utilizada para los elementos de superposición de la interfaz de usuario durante la Experiement (captura). Esto se pasa desde el host (como Visual Studio Diagnóstico de gráficos) al motor de captura.

**registryRoot**  
Cadena COM que contiene la raíz del registro. Esto se pasa desde el host (como Visual Studio Diagnóstico de gráficos) al motor de captura.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



