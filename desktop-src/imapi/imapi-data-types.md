---
title: Tipos de datos IMAPI (Imapi2.h)
description: Las especificaciones de medios ópticos y dispositivos asociados definen valores de intervalo para elementos como la descripción de la estructura de DVD, la descripción de la información del disco y el tamaño de página de características.
ms.assetid: 8797a8d0-5ce5-4b16-9d41-c22fa0d67dcf
keywords:
- ULONG_IMAPI2_DVD_STRUCTURE
- ULONG_IMAPI2_ADAPTER_DESCRIPTOR
- ULONG_IMAPI2_DEVICE_DESCRIPTOR
- ULONG_IMAPI2_DISC_INFORMATION
- ULONG_IMAPI2_TRACK_INFORMATION
- ULONG_IMAPI2_FEATURE_PAGE
- ULONG_IMAPI2_MODE_PAGE
- ULONG_IMAPI2_ALL_FEATURE_PAGES
- ULONG_IMAPI2_ALL_PROFILES
- ULONG_IMAPI2_ALL_MODE_PAGES
- ULONG_IMAPI2_NONZERO
- ULONG_IMAPI2_NOT_NEGATIVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f003c2e03ff3d21623111d3d43a83cddf43e31c64557cfce18b5a401cdcd5d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612015"
---
# <a name="imapi-data-types"></a>Tipos de datos IMAPI

Las especificaciones de medios ópticos y dispositivos asociados definen valores de intervalo para elementos como la descripción de la estructura de DVD, la descripción de la información del disco y el tamaño de página de características. IMAPI define los siguientes tipos de entero largo sin signo (ULONG) que aplican límites de valor de intervalo. Estos tipos se definen estrictamente para la validación óptima de IDL de parámetros y como una ayuda de documentación a los llamadores con respecto a los límites superiores para ciertas operaciones de transferencia de datos disponibles.


```C++
typedef ULONG ULONG_IMAPI2_DVD_STRUCTURE;
typedef ULONG ULONG_IMAPI2_ADAPTER_DESCRIPTOR;
typedef ULONG ULONG_IMAPI2_DEVICE_DESCRIPTOR;
typedef ULONG ULONG_IMAPI2_DISC_INFORMATION;
typedef ULONG ULONG_IMAPI2_TRACK_INFORMATION;
typedef ULONG ULONG_IMAPI2_FEATURE_PAGE;
typedef ULONG ULONG_IMAPI2_MODE_PAGE;
typedef ULONG ULONG_IMAPI2_ALL_FEATURE_PAGES;
typedef ULONG ULONG_IMAPI2_ALL_PROFILES;
typedef ULONG ULONG_IMAPI2_ALL_MODE_PAGES;
typedef ULONG ULONG_IMAPI2_NONZERO;
typedef ULONG ULONG_IMAPI2_NOT_NEGATIVE;
```





| Tipo de datos                                                                                                                                  | Descripción                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ULONG_IMAPI2_DVD_STRUCTURE"></span><span id="ulong_imapi2_dvd_structure"></span>**ESTRUCTURA DE DVD DE ULONG \_ IMAPI2 \_ \_**                | Intervalo: 065535 (0,0x0000FFFF)<br/> La estructura de DVD está limitada a 64 KB debido a un campo de asignación de dos bytes.<br/>                                                                                                                                                                                     |
| <span id="ULONG_IMAPI2_ADAPTER_DESCRIPTOR"></span><span id="ulong_imapi2_adapter_descriptor"></span>**DESCRIPTOR DEL ADAPTADOR DE ULONG \_ IMAPI2 \_ \_** | Intervalo: 0,268435455 (0,0x0FFFFFFF)<br/> El descriptor del adaptador no tiene un tamaño limitado implícitamente.<br/>                                                                                                                                                                                                |
| <span id="ULONG_IMAPI2_DEVICE_DESCRIPTOR"></span><span id="ulong_imapi2_device_descriptor"></span>**DESCRIPTOR DE \_ DISPOSITIVO ULONG IMAPI2 \_ \_**    | Intervalo: 0,268435455 (0,0x0FFFFFFF)<br/> El descriptor de dispositivo no tiene un tamaño limitado implícitamente.<br/>                                                                                                                                                                                                 |
| <span id="ULONG_IMAPI2_DISC_INFORMATION"></span><span id="ulong_imapi2_disc_information"></span>**INFORMACIÓN DEL DISCO DE ULONG \_ IMAPI2 \_ \_**       | Intervalo: 065538 (0,0x00010002)<br/> La información del disco está limitada a 64 KB más 2 bytes para el campo de tamaño.<br/>                                                                                                                                                                                         |
| <span id="ULONG_IMAPI2_TRACK_INFORMATION"></span><span id="ulong_imapi2_track_information"></span>**INFORMACIÓN DE SEGUIMIENTO DE ULONG \_ IMAPI2 \_ \_**    | Intervalo: 065538 (0,0x00010002)<br/> La información de seguimiento está limitada a 64 KB más 2 bytes para el campo de tamaño.<br/>                                                                                                                                                                                        |
| <span id="ULONG_IMAPI2_FEATURE_PAGE"></span><span id="ulong_imapi2_feature_page"></span>**PÁGINA DE CARACTERÍSTICAS DE ULONG \_ IMAPI2 \_ \_**                   | Intervalo: 0256 (0,0x00000100)<br/> Una sola página de características está limitada a 256 bytes.<br/>                                                                                                                                                                                                                 |
| <span id="ULONG_IMAPI2_MODE_PAGE"></span><span id="ulong_imapi2_mode_page"></span>**PÁGINA DEL \_ MODO IMAPI2 \_ DE ULONG \_**                            | Intervalo: 0257 (0,0x00000101)<br/> Una página en modo único está limitada a 257 bytes.<br/>                                                                                                                                                                                                                    |
| <span id="ULONG_IMAPI2_ALL_FEATURE_PAGES"></span><span id="ulong_imapi2_all_feature_pages"></span>**PÁGINAS DE CARACTERÍSTICAS DE ULONG \_ IMAPI2 \_ \_ \_**   | Intervalo: 065536 (0,0x00010000)<br/> El número de características se limita a un campo de dos bytes.<br/>                                                                                                                                                                                                       |
| <span id="ULONG_IMAPI2_ALL_PROFILES"></span><span id="ulong_imapi2_all_profiles"></span>**TODOS LOS PERFILES DE ULONG \_ IMAPI2 \_ \_**                   | Intervalo: 0,63 (0,0x0000003F)<br/> El número de perfiles de un dispositivo es el número de perfiles que caben en una sola característica. Cada perfil ocupa cuatro bytes. Una sola característica puede contener 252 bytes de datos adicionales, suficientes para almacenar un máximo de 63 perfiles.<br/>                                 |
| <span id="ULONG_IMAPI2_ALL_MODE_PAGES"></span><span id="ulong_imapi2_all_mode_pages"></span>**PÁGINAS DE TODOS LOS MODO DE ULONG \_ IMAPI2 \_ \_ \_**            | Intervalo: 0,32763 (0,0x00007FFB)<br/> Recuento de las páginas de modo de un dispositivo. El recuento, a través de MODE \_ SENSE10, se limita a un campo de dos bytes.<br/> El encabezado del parámetro mode es de 8 bytes. Cada página tiene al menos dos bytes. El número máximo de páginas en modo es 32763: (65535 - 8)/2 redondeado hacia abajo.<br/> |
| <span id="ULONG_IMAPI2_NONZERO"></span><span id="ulong_imapi2_nonzero"></span>**ULONG \_ IMAPI2 \_ DISTINTO DE CERO**                                   | Intervalo: 1,2147483647 (1,0x7FFFFFFF)<br/> Valor genérico distinto de cero que se puede usar para comprobar que un valor no es cero.<br/>                                                                                                                                                                              |
| <span id="ULONG_IMAPI2_NOT_NEGATIVE"></span><span id="ulong_imapi2_not_negative"></span>**ULONG \_ IMAPI2 \_ NOT \_ NEGATIVE**                   | Intervalo: 0, 2147483647 (0,0x7FFFFFFF)<br/> Entero de 32 bits con valor no negativo.<br/>                                                                                                                                                                                                              |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>Imapi2.h</dt> </dl> |



 

 





