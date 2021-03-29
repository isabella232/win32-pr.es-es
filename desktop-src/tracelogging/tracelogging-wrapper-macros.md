---
title: Macros de contenedor de TraceLogging
description: Enumera las macros de contenedor para los proveedores de TraceLogging.
ms.assetid: 806F43F3-D376-4DBD-A4C5-B5F01E5D009D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dc28b3a35074089b1f5c613b041534b8b282423
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779687"
---
# <a name="tracelogging-wrapper-macros"></a>Macros de contenedor de TraceLogging

Enumera las macros de contenedor para los proveedores de TraceLogging.

Para registrar eventos mediante proveedores de TraceLogging, debe usar las macros TraceLogging Write [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) o [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity). Ambas macros requieren que se ajusten los datos de eventos en una macro contenedora. Hay varias macros de contenedor diferentes para los distintos tipos de datos. Para obtener una lista completa de las macros de TraceLogging, vea [macros de TraceLogging](trace-logging-macros.md).

Además de las macros de contenedor anteriores, hay varias macros disponibles para los tipos de datos individuales. Todas estas macros tienen el mismo formato que la macro [TraceLoggingValue](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingvalue) . Puede usar la macro TraceLoggingValue para detectar automáticamente la macro de contenedor adecuada que se va a usar o usar directamente la macro específica.

-   [**TraceLoggingBinary**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingbinary)
-   [**TraceLoggingChannel**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingchannel)
-   [**TraceLoggingCustomAttribute**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingcustomattribute)
-   [**TraceLoggingDescription**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingdescription)
-   [**TraceLoggingEventTag**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingeventtag)
-   [**TraceLoggingKeyword**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingkeyword)
-   [**TraceLoggingLevel**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogginglevel)
-   [**TraceLoggingOpcode**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingopcode)
-   [**TraceLoggingSocketAddress**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingsocketaddress)
-   [**TraceLoggingStruct**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingstruct)
-   [**TraceLoggingValue**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingvalue)

> [!Note]
>
> **TraceLoggingOptionGroup** es específicamente para su uso dentro del \_ proveedor de definición de TRACELOGGING \_ .
>
> -   [**TraceLoggingOptionGroup**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup)

 

Estas son las macros de contenedor individuales.

-   TraceLoggingInt8

-   TraceLoggingUInt8

-   TraceLoggingInt16

-   TraceLoggingUInt16

-   TraceLoggingInt32

-   TraceLoggingUInt32

-   TraceLoggingInt64

-   TraceLoggingUInt64

-   TraceLoggingFloat32

-   TraceLoggingFloat64

-   TraceLoggingBool

-   TraceLoggingFileTime

-   TraceLoggingGuid

-   TraceLoggingPointer

-   TraceLoggingSystemTime

-   TraceLoggingHexInt8

-   TraceLoggingHexUInt8

-   TraceLoggingHexInt32

-   TraceLoggingHexUInt32

-   TraceLoggingHexInt64

-   TraceLoggingHexUInt64

-   TraceLoggingWchar

-   TraceLoggingChar

-   TraceLoggingIntPtr

-   TraceLoggingUIntPtr

-   TraceLoggingBoolean

-   TraceLoggingHexInt16

-   TraceLoggingHexUInt16

-   TraceLoggingPid

-   TraceLoggingTid

-   TraceLoggingPort

-   TraceLoggingWinError

-   TraceLoggingNTStatus

-   TraceLoggingHResult

-   TraceLoggingSocketAddress

-   TraceLoggingSid

-   TraceLoggingString

-   TraceLoggingWideString

-   TraceLoggingCountedString

-   TraceLoggingCountedWideString

-   TraceLoggingAnsiString

-   TraceLoggingUnicodeString

-   TraceLoggingBinary (datos vacíos \* , tamaño de los datos en bytes \[ , \] nombre opcional) los parámetros de esta macro difieren de los anteriores. Si se especifica el parámetro *Name* , debe ser un literal de cadena (no una variable) y no puede contener caracteres nulos incrustados. Si no se proporciona el parámetro *Name* , se genera automáticamente un nombre.

La API de TraceLogging también hace que varias macros estén disponibles para las matrices. Estas matrices pueden tener una longitud fija o ser de longitud variable, en función de la macro de contenedor que elija usar. Todas estas macros de contenedor siguen este formato.

`TraceLoggingBooleanArray(pVals, cVals, name, desc, tags)`

El parámetro *pVals* apunta a la matriz de datos y *cVals* indica el número de elementos de la matriz. *cVals* debe ser una constante y no puede ser una variable. Al igual que con las macros de contenedor de valor único, *Name*, **DESC** y *Tags* son parámetros opcionales y deben seguir las mismas restricciones que se explican con la macro **TraceLoggingValue** .

-   TraceLoggingInt8FixedArray

-   TraceLoggingUInt8FixedArray

-   TraceLoggingInt16FixedArray

-   TraceLoggingUInt16FixedArray

-   TraceLoggingInt32FixedArray

-   TraceLoggingUInt32FixedArray

-   TraceLoggingInt64FixedArray

-   TraceLoggingUInt64FixedArray

-   TraceLoggingFloat32FixedArray

-   TraceLoggingFloat64FixedArray

-   TraceLoggingBoolFixedArray

-   TraceLoggingGuidFixedArray

-   TraceLoggingPointerFixedArray

-   TraceLoggingFileTimeFixedArray

-   TraceLoggingSystemTimeFixedArray

-   TraceLoggingHexInt8FixedArray

-   TraceLoggingHexUInt8FixedArray

-   TraceLoggingHexInt32FixedArray

-   TraceLoggingHexUInt32FixedArray

-   TraceLoggingHexInt64FixedArray

-   TraceLoggingHexUInt64FixedArray

-   TraceLoggingWcharFixedArray

-   TraceLoggingCharFixedArray

-   TraceLoggingIntPtrFixedArray

-   TraceLoggingUIntPtrFixedArray

-   TraceLoggingBooleanFixedArray

-   TraceLoggingHexInt16FixedArray

-   TraceLoggingHexUInt16FixedArray

-   TraceLoggingInt8Array

-   TraceLoggingUInt8Array

-   TraceLoggingInt16Array

-   TraceLoggingUInt16Array

-   TraceLoggingInt32Array

-   TraceLoggingUInt32Array

-   TraceLoggingInt64Array

-   TraceLoggingUInt64Array

-   TraceLoggingFloat32Array

-   TraceLoggingFloat64Array

-   TraceLoggingBoolArray

-   TraceLoggingGuidArray

-   TraceLoggingPointerArray

-   TraceLoggingFileTimeArray

-   TraceLoggingSystemTimeArray

-   TraceLoggingHexInt8Array

-   TraceLoggingHexUInt8Array

-   TraceLoggingHexInt32Array

-   TraceLoggingHexUInt32Array

-   TraceLoggingHexInt64Array

-   TraceLoggingHexUInt64Array

-   TraceLoggingWcharArray

-   TraceLoggingCharArray

-   TraceLoggingIntPtrArray

-   TraceLoggingUIntPtrArray

-   TraceLoggingBooleanArray

-   TraceLoggingHexInt16Array

-   TraceLoggingHexUInt16Array

 

 




