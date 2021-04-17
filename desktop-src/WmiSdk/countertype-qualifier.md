---
description: El calificador de contratipo contiene el valor entero para el tipo de contador de propiedad para las propiedades de \_ las clases PerfRawData de Win32. CookingType contiene las constantes para los tipos de fórmula de propiedad de \_ las clases PerfFormattedData de Win32.
ms.assetid: aa79fcdb-503f-4928-b2b7-f07baeaf9fb5
ms.tgt_platform: multiple
title: Calificador de tipo
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
ms.openlocfilehash: 883ee7aa2f230756d62294d46e6402fe7f962d4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677627"
---
# <a name="countertype-qualifier"></a>Calificador de tipo

El calificador de **contratipo** contiene el valor entero para el tipo de contador de propiedad para las propiedades de las clases [**\_ PerfRawData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) . **CookingType** contiene las constantes para los tipos de fórmula de propiedad de las clases [**\_ PerfFormattedData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) .

Para obtener más información y un desglose de los tipos de contador por función, vea [tipos de contadores](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)).



| Tipo | CookingType                              |
|-------------|------------------------------------------|
| 0           | contador de rendimiento \_ \_ RAWCOUNT \_ Hex             |
| 256         | contador de rendimiento de \_ \_ \_ RAWCOUNT grande \_ Hex      |
| 2816        | \_texto del contador de rendimiento \_                      |
| 65536       | contador de rendimiento \_ \_ RAWCOUNT                  |
| 65792       | contador de rendimiento \_ \_ grande \_ RAWCOUNT           |
| 73728       | RENDIMIENTO \_ doble \_ sin formato                        |
| 4195328     | \_Delta de contador de rendimiento \_                     |
| 4195584     | \_ \_ diferencia grande de contador de rendimiento \_              |
| 4260864     | \_contador de ejemplo de rendimiento \_                    |
| 4523008     | tipo de contador de rendimiento \_ \_ QUEUELEN \_            |
| 4523264     | \_tipo de \_ \_ QUEUELEN grande de contador \_ de rendimiento     |
| 5571840     | Contador de rendimiento de \_ \_ \_ tipo QUEUELEN de 100 NS \_     |
| 6620416     | \_tipo de \_ \_ QUEUELEN de \_ tiempo \_ del contador de rendimiento |
| 272696320   | contador \_ de rendimiento \_                   |
| 272696576   | \_recuento masivo de contadores de rendimiento \_ \_               |
| 537003008   | fracción de rendimiento \_ sin procesar \_                      |
| 541132032   | \_temporizador de contadores de rendimiento \_                     |
| 541525248   | \_ \_ temporizador del sistema de precisión de rendimiento \_           |
| 542180608   | \_Temporizador de 100NSEC de rendimiento \_                     |
| 542573824   | \_Temporizador de \_ 100 de precisión de rendimiento \_            |
| 543229184   | \_temporizador de \_ tiempo de Perf \_                   |
| 543622400   | \_temporizador de \_ objeto de precisión de rendimiento \_           |
| 549585920   | \_fracción de ejemplo de rendimiento \_                   |
| 557909248   | \_ \_ INV del contador de rendimiento \_                |
| 558957824   | \_INV 100NSEC \_ del temporizador \_ de rendimiento                |
| 574686464   | contador de rendimiento de \_ \_ varios \_ temporizadores              |
| 575735040   | \_ \_ Temporizador múltiple de rendimiento 100NSEC \_              |
| 591463680   | contador de rendimiento de \_ \_ varios \_ temporizadores \_         |
| 592512256   | \_Inv de \_ \_ temporizador múltiple \_ de rendimiento 100NSEC         |
| 805438464   | \_temporizador de promedio de rendimiento \_                     |
| 807666944   | \_tiempo transcurrido de rendimiento \_                      |
| 1073742336  | contador de rendimiento \_ \_ NoData                    |
| 1073874176  | media de rendimiento en \_ \_ masa                      |
| 1073939457  | \_base de ejemplo de rendimiento \_                       |
| 1073939458  | \_base de promedio de rendimiento \_                      |
| 1073939459  | \_base sin procesar de rendimiento \_                          |
| 1073939712  | marca de tiempo de precisión de rendimiento \_ \_               |
| 1073939715  | \_ \_ base sin formato de alto rendimiento \_                   |
| 1107494144  | contador de rendimiento de \_ \_ varias \_ bases               |
| 2147483648  | \_tipo de \_ histograma del contador de rendimiento \_           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Calificadores específicos de las clases de rendimiento de WMI](qualifiers-specific-to-wmi-performance-classes.md)
</dt> </dl>

 

