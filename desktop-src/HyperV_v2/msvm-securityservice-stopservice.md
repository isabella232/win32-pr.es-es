---
description: detiene el servicio.
ms.assetid: cf100cea-b0e1-42e9-831e-6422aded47c5
title: Método StopService de la clase Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 68e88e2c88d4f75f4d7671c389bab0cd81d0deb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277575"
---
# <a name="stopservice-method-of-the-msvm_securityservice-class"></a>Método StopService de la \_ clase MSVM SecurityService

detiene el servicio.

## <a name="syntax"></a>Sintaxis


```mof
uint32 StopService();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si se ejecuta correctamente, devuelve un 0; de lo contrario, devuelve un error.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**No compatible** (1)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ SecurityService**](msvm-securityservice.md)
</dt> </dl>

 

 




