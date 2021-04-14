---
description: Representa el control de comprobación de la máquina (CMC) corregido que se va a cambiar del controlador de interrupción al sondeo. Esta clase solo está disponible en sistemas Windows de 64 bits.
ms.assetid: c5e99e13-0f65-40bc-8863-b2ca7ea221df
title: MSMCAEvent_SwitchToCMCPolling (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SwitchToCMCPolling
- MSMCAEvent_SwitchToCMCPolling.Active
- MSMCAEvent_SwitchToCMCPolling.InstanceName
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: f7d0d543dc36054550d4ddf6cc1a77ce80cf1647
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360288"
---
# <a name="msmcaevent_switchtocmcpolling-class"></a>MSMCAEvent \_ SwitchToCMCPolling (clase)

La clase **MSMCAEvent \_ SwitchToCMCPolling** representa el control correcto de la comprobación de la máquina (CMC) que se va a cambiar del controlador de interrupción al sondeo. En algunos casos, el kernel sondea la capa de abstracción del sistema (SAL) en busca de cualquier error de plataforma CMC o corregido (CPE) que se produjera en el intervalo de sondeo anterior. Esta clase solo está disponible en sistemas Windows de 64 bits.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MSMCAEvent_SwitchToCMCPolling : WMIEvent
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a>Miembros

La clase **MSMCAEvent \_ SwitchToCMCPolling** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSMCAEvent \_ SwitchToCMCPolling** tiene estas propiedades.

<dl> <dt>

**Activo**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

**True** si esta instancia de la clase está activa; en caso contrario, **false**.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Identificador único de esta instancia de la clase.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **MSMCAEvent \_ SwitchToCMCPolling** se deriva de [**WMIEvent**](wmievent.md).

La capa de abstracción del sistema (SAL) es código grabado en el ROM que el sistema operativo llama para realizar operaciones dependientes de la plataforma. Es similar al BIOS en una plataforma x86. En los casos en los que la plataforma no admite interrupciones para sondeos CMC o CPE, el sistema operativo sondea cada minuto y comprueba si se ha producido un error anteriormente. Si la plataforma admite interrupciones y el sistema operativo recibe una cantidad definida por el usuario de sondeos CMC o CPE en un minuto, se deshabilitará la interrupción y el sondeo. Si el usuario no define el número de sondeos en un minuto, el sistema establece un valor predeterminado de 10 sondeos por minuto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2003<br/>                                                         |
| Espacio de nombres<br/>                | \\WMI raíz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Wmicore. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases MSMCA](msmca-classes.md)
</dt> <dt>

[**WMIEvent**](wmievent.md)
</dt> </dl>

 

