---
title: Tipos de datos de IMAPi (Imapi2. h)
description: Las especificaciones de los medios ópticos y los dispositivos asociados definen valores de intervalo para elementos como la descripción de la estructura de DVD, la descripción de la información de disco y el tamaño de página de características.
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
ms.openlocfilehash: 7793bab123e2939bdc2f5a68bb705d7468da5666
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714623"
---
# <a name="imapi-data-types"></a>Tipos de datos de IMAPi

Las especificaciones de los medios ópticos y los dispositivos asociados definen valores de intervalo para elementos como la descripción de la estructura de DVD, la descripción de la información de disco y el tamaño de página de características. IMAPi define los siguientes tipos de entero largo sin signo (ULONG) que aplican límites de valor de intervalo. Estos tipos se definen estrictamente para la validación de IDL óptima de los parámetros y como ayuda de documentación a los autores de llamadas con respecto a los límites superiores de ciertas operaciones de transferencia de datos disponibles.


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
| <span id="ULONG_IMAPI2_DVD_STRUCTURE"></span><span id="ulong_imapi2_dvd_structure"></span>**ULONG \_ IMAPI2 \_ estructura de DVD \_**                | Intervalo: 0, 65535 (0, 0x0000FFFF)<br/> La estructura de DVD está limitada a 64 KB debido a un campo de asignación de dos bytes.<br/>                                                                                                                                                                                     |
| <span id="ULONG_IMAPI2_ADAPTER_DESCRIPTOR"></span><span id="ulong_imapi2_adapter_descriptor"></span>**Descriptor de adaptador ULONG \_ IMAPI2 \_ \_** | Intervalo: 0, 268435455 (0, 0x0FFFFFFF)<br/> El descriptor de adaptador no tiene un tamaño limitado implícitamente.<br/>                                                                                                                                                                                                |
| <span id="ULONG_IMAPI2_DEVICE_DESCRIPTOR"></span><span id="ulong_imapi2_device_descriptor"></span>**\_IMAPI2 ( \_ \_ descriptor de dispositivo de ulong)**    | Intervalo: 0, 268435455 (0, 0x0FFFFFFF)<br/> El descriptor de dispositivo no tiene un tamaño limitado implícitamente.<br/>                                                                                                                                                                                                 |
| <span id="ULONG_IMAPI2_DISC_INFORMATION"></span><span id="ulong_imapi2_disc_information"></span>**ULONG \_ IMAPI2 \_ información del disco \_**       | Intervalo: 0, 65538 (0, 0x00010002)<br/> La información del disco está limitada a 64 KB más 2 bytes para el campo tamaño.<br/>                                                                                                                                                                                         |
| <span id="ULONG_IMAPI2_TRACK_INFORMATION"></span><span id="ulong_imapi2_track_information"></span>**Información de seguimiento de ULONG \_ IMAPI2 \_ \_**    | Intervalo: 0, 65538 (0, 0x00010002)<br/> La información de seguimiento está limitada a 64 KB más 2 bytes para el campo tamaño.<br/>                                                                                                                                                                                        |
| <span id="ULONG_IMAPI2_FEATURE_PAGE"></span><span id="ulong_imapi2_feature_page"></span>**Página de características de ULONG \_ IMAPI2 \_ \_**                   | Intervalo: 0256 (0, 0x00000100)<br/> Una sola página de características está limitada a 256 bytes.<br/>                                                                                                                                                                                                                 |
| <span id="ULONG_IMAPI2_MODE_PAGE"></span><span id="ulong_imapi2_mode_page"></span>**\_IMAPI2 ( \_ página del modo) \_**                            | Intervalo: 0257 (0, 0x00000101)<br/> Una página de modo único está limitada a 257 bytes.<br/>                                                                                                                                                                                                                    |
| <span id="ULONG_IMAPI2_ALL_FEATURE_PAGES"></span><span id="ulong_imapi2_all_feature_pages"></span>**ULONG \_ IMAPI2 \_ todas \_ \_ las páginas de características**   | Intervalo: 0, 65536 (0, 0x00010000)<br/> El número de características se limita a un campo de dos bytes.<br/>                                                                                                                                                                                                       |
| <span id="ULONG_IMAPI2_ALL_PROFILES"></span><span id="ulong_imapi2_all_profiles"></span>**ULONG \_ IMAPI2 \_ todos los \_ perfiles**                   | Intervalo: 0, 63 (0, 0x0000003F)<br/> El número de perfiles de un dispositivo es el número de perfiles que caben en una sola característica. Cada perfil ocupa cuatro bytes. Una sola característica puede contener 252 bytes de datos adicionales, lo suficiente para almacenar un máximo de 63 perfiles.<br/>                                 |
| <span id="ULONG_IMAPI2_ALL_MODE_PAGES"></span><span id="ulong_imapi2_all_mode_pages"></span>**\_Páginas de modo ulong IMAPI2 \_ All \_ \_**            | Intervalo: 0, 32763 (0, 0x00007FFB)<br/> Recuento de las páginas de modo para un dispositivo. El recuento, mediante el modo \_ SENSE10, está limitado a un campo de dos bytes.<br/> El encabezado del parámetro de modo es de 8 bytes. Cada página tiene al menos dos bytes. El número máximo de páginas de modo es 32763: (65535-8)/2 redondeado hacia abajo.<br/> |
| <span id="ULONG_IMAPI2_NONZERO"></span><span id="ulong_imapi2_nonzero"></span>**ULONG \_ IMAPI2 \_ distinto de cero**                                   | Intervalo: 1, 2147483647 (1, 0x7FFFFFFF)<br/> Valor distinto de cero genérico que se puede utilizar para comprobar que un valor no es cero.<br/>                                                                                                                                                                              |
| <span id="ULONG_IMAPI2_NOT_NEGATIVE"></span><span id="ulong_imapi2_not_negative"></span>**ULONG \_ IMAPI2 \_ no es \_ negativo**                   | Intervalo: 0, 2147483647 (0, 0x7FFFFFFF)<br/> Entero de 32 bits con un valor no negativo.<br/>                                                                                                                                                                                                              |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Imapi2. h</dt> </dl> |



 

 





