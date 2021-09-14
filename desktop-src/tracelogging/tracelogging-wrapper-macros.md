---
title: Macros de contenedor tracelogging
description: Enumera las macros contenedoras para los proveedores de TraceLogging.
ms.assetid: 806F43F3-D376-4DBD-A4C5-B5F01E5D009D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dc28b3a35074089b1f5c613b041534b8b282423
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267575"
---
# <a name="tracelogging-wrapper-macros"></a>Macros de contenedor tracelogging

Enumera las macros contenedoras para los proveedores de TraceLogging.

Para registrar eventos mediante proveedores de TraceLogging, debe usar las macros de escritura [**TraceLogging TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) [**o TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity). Ambas macros requieren que se ajusten los datos de evento en una macro contenedora. Hay varias macros de contenedor diferentes para distintos tipos de datos. Para obtener una lista completa de las macros tracelogging, vea [TraceLogging Macros](trace-logging-macros.md).

Además de las macros contenedora anteriores, hay varias macros disponibles para tipos de datos individuales. Todas estas macros tienen el mismo formato que la macro [TraceLoggingValue.](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingvalue) Puede usar la macro TraceLoggingValue para detectar automáticamente la macro contenedora adecuada que se va a usar, o bien usar directamente la macro específica.

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
> **TraceLoggingOptionGroup** se usa específicamente dentro de TRACELOGGING \_ DEFINE \_ PROVIDER.
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

-   TraceLoggingBinary(void data, size of the data in bytes, optional name ) Los parámetros de esta \* \[ macro \] difieren de los anteriores. Si se *especifica* el parámetro name, debe ser un literal de cadena (no una variable) y no puede contener caracteres NULL incrustados. Si no *se proporciona* el parámetro name, se genera automáticamente un nombre.

TraceLogging API también hace que varias macros estén disponibles para las matrices. Estas matrices pueden tener una longitud fija o tener una longitud variable, dependiendo de la macro contenedora que elija usar. Todas estas macros contenedora siguen este formato.

`TraceLoggingBooleanArray(pVals, cVals, name, desc, tags)`

El parámetro *pVals* apunta a la matriz de datos y *cVals* indica el número de elementos de la matriz. *cVals debe* ser una constante y no puede ser una variable. Al igual que con las macros contenedoras  de un solo valor, las etiquetas *name*, **desc** y son parámetros opcionales y deben seguir las mismas restricciones que se explican con la macro **TraceLoggingValue.**

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

 

 




