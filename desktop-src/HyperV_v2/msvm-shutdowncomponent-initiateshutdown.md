---
description: Inicia una operación de apagado del sistema operativo en la máquina virtual secundaria asociada. Si se devuelve cero (0), el cierre se ha iniciado correctamente. Cualquier otro código de retorno indica una condición de error.
ms.assetid: 946BBC62-5479-4AE0-8870-D0A07827B902
title: Método InitiateShutdown de la clase Msvm_ShutdownComponent (winreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponent.InitiateShutdown
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 266ab64bb058325ac165a2e12c2a91d442a90269
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277569"
---
# <a name="initiateshutdown-method-of-the-msvm_shutdowncomponent-class"></a>Método InitiateShutdown de la \_ clase ShutdownComponent de MSVM

Inicia una operación de apagado del sistema operativo en la máquina virtual secundaria asociada. Si se devuelve cero (0), el cierre se ha iniciado correctamente. Cualquier otro código de retorno indica una condición de error.

## <a name="syntax"></a>Sintaxis


```mof
uint32 InitiateShutdown(
  [in] boolean Force,
  [in] string  Reason
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Forzar* \[ de\]
</dt> <dd>

Tipo: **booleano**

Marca que, si **es true**, obliga a que se cierren las aplicaciones a pesar de tener datos no guardados.

</dd> <dt>

*Motivo* \[ de\]
</dt> <dd>

Tipo: **String**

Motivo de la operación de cierre. Esta es una cadena definida por el usuario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

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

## <a name="remarks"></a>Observaciones

El acceso a la clase [**MSVM \_ ShutdownComponent**](msvm-shutdowncomponent.md) puede estar restringido por el filtrado de UAC. Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| Encabezado<br/>                   | <dl> <dt>Winreg. h</dt> </dl>                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ ShutdownComponent**](msvm-shutdowncomponent.md)
</dt> </dl>

 

