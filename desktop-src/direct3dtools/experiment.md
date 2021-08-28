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
ms.openlocfilehash: 90e60f3f197db78a3ec399c2f8ffe7144901b097
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625371"
---
# <a name="span-idvspixengineexperimentspanexperiment-structure"></a><span id="vspixengine.experiment"></span>Estructura del experimento

Representa información sobre un experimento (captura).

## <a name="syntax"></a>Sintaxis


```C++
} Experiment;
```

## <a name="members"></a>Miembros

**processId**  
Identificador de proceso asociado.

**applicationName**  
Cadena COM que contiene el nombre de la aplicación en la que se ejecutará el experimento.

**commandLineArguments**  
Cadena COM que contiene los argumentos de la línea de comandos.

**workingDirectory**  
Cadena COM que contiene la ruta de acceso del directorio de trabajo.

**tempPixRunFile**  
Cadena COM que contiene la ruta de acceso del archivo temporal utilizado para realizar el experimento.

**startOption**  
Opción de inicio asociada al experimento.

**experimentType**  
Tipo de experimento (captura).

**uiLocale**  
Identificador de la configuración regional que se usa para los elementos de superposición de la interfaz de usuario durante la expansión (captura). Esto se pasa desde el host (por ejemplo, Visual Studio Diagnóstico de gráficos) al motor de captura.

**registryRoot**  
Cadena COM que contiene la raíz del Registro. Esto se pasa desde el host (por ejemplo, Visual Studio Diagnóstico de gráficos) al motor de captura.

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



