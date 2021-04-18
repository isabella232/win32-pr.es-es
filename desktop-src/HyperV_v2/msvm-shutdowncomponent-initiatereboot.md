---
description: Inicia una operación de reinicio del sistema operativo en la máquina virtual secundaria asociada.
ms.assetid: 9f3ebbaf-ee0f-4c01-8f73-1f37c08a0feb
title: Método InitiateReboot de la clase Msvm_ShutdownComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponent.InitiateReboot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 527569e8a5d6c2bb0a54294637ae19c13f5e3af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652471"
---
# <a name="initiatereboot-method-of-the-msvm_shutdowncomponent-class"></a>Método InitiateReboot de la \_ clase ShutdownComponent de MSVM

Inicia una operación de reinicio del sistema operativo en la máquina virtual secundaria asociada.

Si se devuelve cero (0), el reinicio se ha iniciado correctamente. Cualquier otro código de retorno indica una condición de error.

## <a name="syntax"></a>Sintaxis


```mof
uint32 InitiateReboot(
  [in] boolean Force,
  [in] string  Reason
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Forzar* \[ de\]
</dt> <dd>

Marca que, si es TRUE, obliga a que se cierren las aplicaciones a pesar de tener datos no guardados.

</dd> <dt>

*Motivo* \[ de\]
</dt> <dd>

Motivo de la operación de reinicio. Esta es una cadena definida por el usuario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los siguientes valores:

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**Parámetros de método comprobados: trabajo iniciado** (4096)
</dt> <dt>

**Error** (32768)
</dt> <dt>

**Acceso denegado** (32769)
</dt> <dt>

**No compatible** (32770)
</dt> <dt>

**Estado desconocido** (32771)
</dt> <dt>

**Tiempo de espera** (32772)
</dt> <dt>

**Parámetro no válido** (32773)
</dt> <dt>

El **sistema está en uso** (32774)
</dt> <dt>

**Estado no válido para esta operación** (32775)
</dt> <dt>

**Tipo de datos incorrecto** (32776)
</dt> <dt>

El **sistema no está disponible** (32777)
</dt> <dt>

**Memoria insuficiente** (32778)
</dt> <dt>

**No se encontró el archivo** (32779)
</dt> <dt>

**El sistema no está listo** (32780)
</dt> <dt>

**El equipo está bloqueado y no se puede apagar sin la opción Force** (32781)
</dt> <dt>

**Un apagado del sistema está en curso** (32782)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ ShutdownComponent**](msvm-shutdowncomponent.md)
</dt> </dl>

 

 




