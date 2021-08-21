---
description: Inicia una operación de reinicio del sistema operativo en la máquina virtual secundaria asociada.
ms.assetid: 9f3ebbaf-ee0f-4c01-8f73-1f37c08a0feb
title: Método InitiateReboot de la Msvm_ShutdownComponent clase
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
ms.openlocfilehash: 20ec6e4522f4a9060ced517b5f9944177a98dfa5455c35e15285921467ed4620
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950494"
---
# <a name="initiatereboot-method-of-the-msvm_shutdowncomponent-class"></a>Método InitiateReboot de la clase ShutdownComponent de Msvm \_

Inicia una operación de reinicio del sistema operativo en la máquina virtual secundaria asociada.

Si se devuelve cero (0), el reinicio se inició correctamente. Cualquier otro código de retorno indica una condición de error.

## <a name="syntax"></a>Sintaxis


```mof
uint32 InitiateReboot(
  [in] boolean Force,
  [in] string  Reason
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Forzar* \[ En\]
</dt> <dd>

Marca que, si es TRUE, obliga a cerrar las aplicaciones a pesar de tener datos no guardados.

</dd> <dt>

*Motivo* \[ En\]
</dt> <dd>

El motivo de la operación de reinicio. Se trata de una cadena definida por el usuario.

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

**El estado es desconocido** (32771)
</dt> <dt>

**Tiempo de** espera (32772)
</dt> <dt>

**Parámetro no** válido (32773)
</dt> <dt>

**Sistema en uso** (32774)
</dt> <dt>

**Estado no válido para esta operación** (32775)
</dt> <dt>

**Tipo de datos incorrecto** (32776)
</dt> <dt>

**El sistema no está disponible** (32777)
</dt> <dt>

**Memoria sin memoria** (32778)
</dt> <dt>

**Archivo no encontrado** (32779)
</dt> <dt>

**El sistema no está listo** (32780)
</dt> <dt>

**La máquina está bloqueada y no se puede apagar sin la opción forzar** (32781).
</dt> <dt>

**Hay un apagado del sistema en curso** (32782)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Msvm \_ ShutdownComponent**](msvm-shutdowncomponent.md)
</dt> </dl>

 

 




