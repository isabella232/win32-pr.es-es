---
description: Inicia una operación de apagado del sistema operativo en la máquina virtual secundaria asociada. Si se devuelve cero (0), el cierre se inició correctamente. Cualquier otro código de retorno indica una condición de error.
ms.assetid: 946BBC62-5479-4AE0-8870-D0A07827B902
title: Método InitiateShutdown de la Msvm_ShutdownComponent (Winreg.h)
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
ms.openlocfilehash: f128eb2babfed0c70aca063832e579ad254ca1b02d6beaefb451c64598faa8d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950404"
---
# <a name="initiateshutdown-method-of-the-msvm_shutdowncomponent-class"></a>Método InitiateShutdown de la clase ShutdownComponent de Msvm \_

Inicia una operación de apagado del sistema operativo en la máquina virtual secundaria asociada. Si se devuelve cero (0), el cierre se inició correctamente. Cualquier otro código de retorno indica una condición de error.

## <a name="syntax"></a>Sintaxis


```mof
uint32 InitiateShutdown(
  [in] boolean Force,
  [in] string  Reason
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Forzar* \[ En\]
</dt> <dd>

Tipo: **booleano**

Marca que, si es **True,** obliga a cerrar las aplicaciones a pesar de tener datos no guardados.

</dd> <dt>

*Motivo* \[ En\]
</dt> <dd>

Tipo: **cadena**

El motivo de la operación de apagado. Se trata de una cadena definida por el usuario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

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

**La máquina está bloqueada y no se puede apagar sin la opción force** (32781)
</dt> <dt>

**Hay un apagado del sistema en curso** (32782)
</dt> </dl>

## <a name="remarks"></a>Comentarios

El acceso a [**la clase \_ ShutdownComponent de Msvm**](msvm-shutdowncomponent.md) podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| Header<br/>                   | <dl> <dt>Winreg.h</dt> </dl>                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ShutdownComponent de Msvm \_**](msvm-shutdowncomponent.md)
</dt> </dl>

 

