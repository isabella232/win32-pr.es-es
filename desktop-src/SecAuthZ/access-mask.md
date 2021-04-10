---
description: Define derechos estándar, específicos y genéricos. Estos derechos se usan en entradas de control de acceso (ACE) y son el medio principal para especificar el acceso solicitado o concedido a un objeto.
ms.assetid: f115ee54-3333-4109-8004-d71904a7a943
title: ACCESS_MASK (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d10d9e8db246c2705911cc57221400f40da014d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156296"
---
# <a name="access_mask"></a>máscara de acceso \_

El tipo de datos de la **\_ máscara de acceso** es un valor **DWORD** que define derechos estándar, específicos y genéricos. Estos derechos se usan en [*entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) y son el medio principal para especificar el acceso solicitado o concedido a un objeto.


```C++
typedef DWORD ACCESS_MASK;
typedef ACCESS_MASK* PACCESS_MASK;
```



## <a name="remarks"></a>Observaciones

Los bits de este valor se asignan como se indica a continuación.



| Bits             | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 15<br/>  | Derechos específicos. Contiene la máscara de acceso específica del tipo de objeto asociado a la máscara.<br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| 16 23<br/> | Derechos estándar. Contiene los derechos de acceso estándar del objeto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| 24<br/>    | Obtener acceso a la seguridad del sistema (**\_ \_ seguridad del sistema de acceso**). Se utiliza para indicar el acceso a una [*lista de control de acceso*](/windows/desktop/SecGloss/s-gly) (SACL) del sistema. Este tipo de acceso requiere que el proceso de llamada tenga el privilegio de **\_ \_ nombre de seguridad se** (Administrar registro de auditoría y seguridad). Si esta marca se establece en la máscara de acceso de una ACE de acceso de auditoría (acceso correcto o incorrecto), se auditará el acceso a la SACL.<br/> |
| 25<br/>    | Máximo permitido (**máximo \_ permitido**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 26 27<br/> | Reservado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| 28<br/>    | Genérico All (**genérico \_ All**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 29<br/>    | Ejecución genérica (**\_ ejecución genérica**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 30<br/>    | Escritura genérica (**\_ escritura genérica**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 31<br/>    | Lectura genérica (**\_ lectura genérica**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

Los bits de derechos estándar, de 16 a 23, contienen los derechos de acceso estándar del objeto y pueden ser una combinación de las siguientes marcas predefinidas.



| bit           | Marca                         | Significado                                                                                                                                                                                                                                  |
|---------------|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 16<br/> | **DELETE**<br/>        | Elimine el acceso.<br/>                                                                                                                                                                                                                |
| 17<br/> | **CONTROL de lectura \_**<br/> | Acceso de lectura al propietario, grupo y [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) del descriptor de seguridad.<br/> |
| 18<br/> | **ESCRIBIR \_ DAC**<br/>    | Acceso de escritura a la DACL.<br/>                                                                                                                                                                                                     |
| 19<br/> | **propietario de escritura \_**<br/>  | Acceso de escritura al propietario.<br/>                                                                                                                                                                                                        |
| 20<br/> | **SYNCHRONIZE**<br/>   | Sincronizar el acceso.<br/>                                                                                                                                                                                                           |



 

Las siguientes constantes definidas en Winnt. h representan los derechos de acceso específicos y estándar.


```C++
#define DELETE                           (0x00010000L)
#define READ_CONTROL                     (0x00020000L)
#define WRITE_DAC                        (0x00040000L)
#define WRITE_OWNER                      (0x00080000L)
#define SYNCHRONIZE                      (0x00100000L)

#define STANDARD_RIGHTS_REQUIRED         (0x000F0000L)

#define STANDARD_RIGHTS_READ             (READ_CONTROL)
#define STANDARD_RIGHTS_WRITE            (READ_CONTROL)
#define STANDARD_RIGHTS_EXECUTE          (READ_CONTROL)

#define STANDARD_RIGHTS_ALL              (0x001F0000L)

#define SPECIFIC_RIGHTS_ALL              (0x0000FFFFL)
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>Winnt. h (incluye Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Control de acceso](access-control.md)
</dt> <dt>

[Estructuras de Access Control básicas](authorization-structures.md)
</dt> <dt>

[Derechos de acceso y máscaras de acceso](access-rights-and-access-masks.md)
</dt> <dt>

[**\_asignación genérica**](/windows/desktop/api/Winnt/ns-winnt-generic_mapping)
</dt> </dl>

 

