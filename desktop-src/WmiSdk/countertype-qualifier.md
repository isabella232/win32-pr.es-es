---
description: El calificador CounterType contiene el valor entero del tipo de contador de propiedades para las propiedades de las clases \_ PerfRawData de Win32. El valor Dentipo contiene las constantes para los tipos de fórmulas de propiedad en las clases \_ PerfFormattedData de Win32.
ms.assetid: aa79fcdb-503f-4928-b2b7-f07baeaf9fb5
ms.tgt_platform: multiple
title: Calificador CounterType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterType
api_type:
- NA
api_location: ''
ms.openlocfilehash: 7795633355eccdc19da235a56d211f4913ac532e9df51f6d30f33635f9b2d39a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131447"
---
# <a name="countertype-qualifier"></a>Calificador CounterType

El **calificador CounterType** contiene el valor entero del tipo de contador de propiedades para las propiedades de las clases [**\_ PerfRawData de Win32.**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) **El valor Dentipo contiene** las constantes para los tipos de fórmulas de propiedad en las clases [**\_ PerfFormattedData de Win32.**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)

Para obtener más información y un desglose de los tipos de contador por función, vea [Tipos de contador](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)).



| CounterType | Método Desinserción                              |
|-------------|------------------------------------------|
| 0           | PERF \_ COUNTER \_ RAWCOUNT \_ HEX             |
| 256         | PERF \_ COUNTER \_ LARGE \_ RAWCOUNT \_ HEX      |
| 2816        | TEXTO DEL \_ CONTADOR DE \_ RENDIMIENTO                      |
| 65536       | PERF \_ COUNTER \_ RAWCOUNT                  |
| 65792       | PERF \_ COUNTER \_ LARGE \_ RAWCOUNT           |
| 73728       | PERF \_ DOUBLE \_ RAW                        |
| 4195328     | PERF \_ COUNTER \_ DELTA                     |
| 4195584     | PERF \_ COUNTER \_ LARGE \_ DELTA              |
| 4260864     | CONTADOR DE \_ EJEMPLO DE \_ PERF                    |
| 4523008     | PERF \_ COUNTER \_ QUEUELEN \_ TYPE            |
| 4523264     | TIPO \_ \_ QUEUELEN GRANDE DE \_ CONTADOR DE RENDIMIENTO \_     |
| 5571840     | PERF \_ COUNTER \_ 100NS \_ QUEUELEN \_ TYPE     |
| 6620416     | PERF \_ COUNTER \_ OBJ \_ TIME \_ QUEUELEN \_ TYPE |
| 272696320   | CONTADOR \_ DE RENDIMIENTO \_                   |
| 272696576   | RECUENTO MASIVO DE \_ \_ CONTADORES DE RENDIMIENTO \_               |
| 537003008   | PERF \_ RAW \_ FRACTION                      |
| 541132032   | TEMPORIZADOR DE CONTADOR DE RENDIMIENTO \_ \_                     |
| 541525248   | TEMPORIZADOR DEL \_ SISTEMA DE PRECISIÓN DE \_ \_ PERF           |
| 542180608   | TEMPORIZADOR DE \_ PERF 100NSEC \_                     |
| 542573824   | TEMPORIZADOR PERF \_ PRECISION \_ 100NS \_            |
| 543229184   | TEMPORIZADOR DE \_ TIEMPO DE PERF \_ \_ OBJ                   |
| 543622400   | TEMPORIZADOR DE OBJETOS \_ DE \_ PRECISIÓN PERF \_           |
| 549585920   | FRACCIÓN DE EJEMPLO DE PERF \_ \_                   |
| 557909248   | INV DEL \_ TEMPORIZADOR DE CONTADOR DE \_ \_ RENDIMIENTO                |
| 558957824   | PERF \_ 100NSEC \_ TIMER \_ INV                |
| 574686464   | TEMPORIZADOR MÚLTIPLE \_ DE CONTADOR \_ DE RENDIMIENTO \_              |
| 575735040   | TEMPORIZADOR MÚLTIPLE PERF \_ 100NSEC \_ \_              |
| 591463680   | INV DE \_ \_ VARIOS \_ TEMPORIZADORES DEL \_ CONTADOR DE RENDIMIENTO         |
| 592512256   | PERF \_ 100NSEC \_ MULTI \_ TIMER \_ INV         |
| 805438464   | TEMPORIZADOR PROMEDIO DE RENDIMIENTO \_ \_                     |
| 807666944   | PERF \_ ELAPSED \_ TIME                      |
| 1073742336  | PERF \_ COUNTER \_ NODATA                    |
| 1073874176  | PERF \_ AVERAGE \_ BULK                      |
| 1073939457  | BASE DE \_ EJEMPLO DE \_ PERF                       |
| 1073939458  | PERF \_ AVERAGE \_ BASE                      |
| 1073939459  | BASE SIN \_ PROCESAR DE \_ PERF                          |
| 1073939712  | MARCA DE TIEMPO DE PRECISIÓN DE PERF \_ \_               |
| 1073939715  | BASE SIN \_ \_ PROCESAR GRANDE DE \_ PERF                   |
| 1107494144  | PERF \_ COUNTER \_ MULTI \_ BASE               |
| 2147483648  | TIPO DE \_ HISTOGRAMA DEL CONTADOR \_ DE RENDIMIENTO \_           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Calificadores específicos de las clases de rendimiento wmi](qualifiers-specific-to-wmi-performance-classes.md)
</dt> </dl>

 

