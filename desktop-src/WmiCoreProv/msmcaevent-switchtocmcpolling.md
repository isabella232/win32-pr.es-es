---
description: Representa el control de comprobación de máquina (CMC) corregido que se va a cambiar del controlador de interrupción al sondeo. Esta clase solo está disponible en sistemas de 64 Windows bits.
ms.assetid: c5e99e13-0f65-40bc-8863-b2ca7ea221df
title: MSMCAEvent_SwitchToCMCPolling clase
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
ms.openlocfilehash: a8192dc83a50063b2aaabba2bf708053fadb8e094bfa1cab82b11b084f722a76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640945"
---
# <a name="msmcaevent_switchtocmcpolling-class"></a>Clase MSMCAEvent \_ SwitchToCMCPolling

La **clase \_ SwitchToCMCPolling de MSMCAEvent** representa el control de comprobación de máquina (CMC) corregido que se va a cambiar del controlador de interrupción al sondeo. En algunos casos, el kernel sondea la capa de abstracción del sistema (SAL) en busca de cualquier error de cmc o de plataforma (CPE) corregido que se produjo dentro del intervalo de sondeo anterior. Esta clase solo está disponible en sistemas de 64 Windows bits.

La sintaxis siguiente se simplifica a partir Managed Object Format (MOF) e incluye todas sus propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MSMCAEvent_SwitchToCMCPolling : WMIEvent
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a>Miembros

La **clase MSMCAEvent \_ SwitchToCMCPolling** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase MSMCAEvent \_ SwitchToCMCPolling** tiene estas propiedades.

<dl> <dt>

**Activo**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

**TRUE**, si esta instancia de la clase está activa; de lo contrario, **FALSE**.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Clave**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Identificador único de esta instancia de la clase .

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ SwitchToCMCPolling de MSMCAEvent** se deriva de [**WMIEvent**](wmievent.md).

La capa de abstracción del sistema (SAL) está codificada en la ROM a la que llama el sistema operativo para realizar operaciones dependientes de la plataforma. Es similar al BIOS en una plataforma x86. En los casos en los que la plataforma no admite interrupciones para el sondeo de CMC o CPE, el sistema operativo sondea cada minuto, comprobando si se produjo un error anteriormente. Si la plataforma admite interrupciones y el sistema operativo recibe una cantidad definida por el usuario de sondeos de CMC o CPE en un minuto, deshabilita la interrupción y el sondeo. Si el usuario no define el número de sondeos en un minuto, el sistema establece un valor predeterminado en 10 sondeos por minuto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2003<br/>                                                         |
| Espacio de nombres<br/>                | Wmi \\ raíz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Wmicore.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Clases MSMCA](msmca-classes.md)
</dt> <dt>

[**WMIEvent**](wmievent.md)
</dt> </dl>

 

