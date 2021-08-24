---
description: El método SetIPConnectionMetric se usa para establecer la métrica de enrutamiento asociada a este adaptador enlazado a IP.
ms.assetid: d7f7c0df-51e3-4dc8-8a53-977ecde075df
ms.tgt_platform: multiple
title: Método SetIPConnectionMetric de la Win32_NetworkAdapterConfiguration clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPConnectionMetric
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 08e27a392ac4b6b31849f0863fa8149730bbfcec5fc4c1fec0e15a4919509f70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759735"
---
# <a name="setipconnectionmetric-method-of-the-win32_networkadapterconfiguration-class"></a>Método SetIPConnectionMetric de la clase \_ NetworkAdapterConfiguration de Win32

El **método SetIPConnectionMetric** se usa para establecer la métrica de enrutamiento asociada a este adaptador enlazado a IP.

En este tema se usa Managed Object Format sintaxis MOF (MOF). Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetIPConnectionMetric(
  [in] uint32 IPConnectionMetric
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*IPConnectionMetric* \[ En\]
</dt> <dd>

Indica el costo de usar las rutas configuradas para este adaptador enlazado a IP. El valor se pondera para esas rutas en la tabla de enrutamiento IP. Si hay varias rutas a un destino en la tabla de enrutamiento, se usa la ruta con la métrica más baja. El intervalo de valores válidos es de 1 a 9999. El valor predeterminado es 1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere ningún reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio y un número diferente si se produce un error. Para obtener más información sobre los códigos de error, vea [**Wmi Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Finalización correcta, no se requiere reinicio**
</dt> <dd>

0

Finalización correcta, no es necesario reiniciar.

</dd> <dt>

**Finalización correcta, reinicio necesario**
</dt> <dd>

1

Finalización correcta, reinicio necesario.

</dd> <dt>

**Método no admitido en esta plataforma**
</dt> <dd>

64

Método no admitido en esta plataforma.

</dd> <dt>

**Error desconocido**
</dt> <dd>

65

Error desconocido.

</dd> <dt>

**Máscara de subred no válida**
</dt> <dd>

66

Máscara de subred no válida.

</dd> <dt>

**Error al procesar una instancia que se devolvió**
</dt> <dd>

67

Error al procesar una instancia que se devolvió.

</dd> <dt>

**Parámetro de entrada no válido**
</dt> <dd>

68

Parámetro de entrada no válido.

</dd> <dt>

**Más de 5 puertas de enlace especificadas**
</dt> <dd>

69

Se han especificado más de cinco puertas de enlace.

</dd> <dt>

**Dirección IP no válida**
</dt> <dd>

70

Dirección IP no válida.

</dd> <dt>

**Dirección IP de puerta de enlace no válida**
</dt> <dd>

71

Dirección IP de puerta de enlace no válida.

</dd> <dt>

**Error al acceder al Registro para obtener la información solicitada**
</dt> <dd>

72

Error al acceder al Registro para obtener la información solicitada.

</dd> <dt>

**Nombre de dominio no válido**
</dt> <dd>

73

Nombre de dominio no válido.

</dd> <dt>

**Nombre de host no válido**
</dt> <dd>

74

Nombre de host no válido.

</dd> <dt>

**No se ha definido ningún servidor WINS principal o secundario**
</dt> <dd>

75

No se ha definido ningún servidor WINS principal o secundario.

</dd> <dt>

**Archivo no válido**
</dt> <dd>

76

Archivo no válido.

</dd> <dt>

**Ruta de acceso del sistema no válida**
</dt> <dd>

77

Ruta de acceso del sistema no válida.

</dd> <dt>

**Error de copia de archivos**
</dt> <dd>

78

Error de copia de archivos.

</dd> <dt>

**Parámetro de seguridad no válido**
</dt> <dd>

79

Parámetro de seguridad no válido.

</dd> <dt>

**No se puede configurar el servicio TCP/IP**
</dt> <dd>

80

No se puede configurar el servicio TCP/IP.

</dd> <dt>

**No se puede configurar el servicio DHCP**
</dt> <dd>

81

No se puede configurar el servicio DHCP.

</dd> <dt>

**No se puede renovar la concesión dhcp**
</dt> <dd>

82

No se puede renovar la concesión DHCP.

</dd> <dt>

**No se puede liberar la concesión dhcp**
</dt> <dd>

83

No se puede liberar la concesión DHCP.

</dd> <dt>

**IP no habilitada en el adaptador**
</dt> <dd>

84

IP no habilitada en el adaptador.

</dd> <dt>

**IPX no habilitado en el adaptador**
</dt> <dd>

85

IPX no habilitado en el adaptador.

</dd> <dt>

**Error de límites de número de marco o red**
</dt> <dd>

86

Error de límites de número de red o marco.

</dd> <dt>

**Tipo de marco no válido**
</dt> <dd>

87

Tipo de marco no válido.

</dd> <dt>

**Número de red no válido**
</dt> <dd>

88

Número de red no válido.

</dd> <dt>

**Número de red duplicado**
</dt> <dd>

89

Número de red duplicado.

</dd> <dt>

**Parámetro fuera de límites**
</dt> <dd>

90

Parámetro fuera de los límites.

</dd> <dt>

**Acceso denegado**
</dt> <dd>

91

Acceso denegado:

</dd> <dt>

**No hay memoria suficiente**
</dt> <dd>

92

Memoria insuficiente

</dd> <dt>

**Ya existe**
</dt> <dd>

93

Ya existe.

</dd> <dt>

**Ruta de acceso, archivo u objeto no encontrado**
</dt> <dd>

94

Ruta de acceso, archivo u objeto no encontrado.

</dd> <dt>

**No se puede notificar al servicio**
</dt> <dd>

95

No se puede notificar al servicio.

</dd> <dt>

**No se puede notificar al servicio DNS**
</dt> <dd>

96

No se puede notificar al servicio DNS.

</dd> <dt>

**Interfaz no configurable**
</dt> <dd>

97

Interfaz no configurable.

</dd> <dt>

**No todas las concesiones DHCP se pueden liberar o renovar**
</dt> <dd>

98

No todas las concesiones DHCP se podrían liberar o renovar.

</dd> <dt>

**DHCP no habilitado en el adaptador**
</dt> <dd>

100

DHCP no habilitado en el adaptador.

</dd> <dt>

**Otros**
</dt> <dd>

101 4294967295

</dd> </dl>

## <a name="examples"></a>Ejemplos

El [ejemplo Modify the IP Connection Metric for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/73367c75-7a39-44dc-a8d7-eb2359030969) VBScript (Modificar la métrica de conexión IP para un adaptador de red de VBScript) establece la métrica de conexión IP de un adaptador de red en 100.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows Vista<br/>                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008, Windows Server 2008<br/>                                     |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases de hardware del sistema de equipo](computer-system-hardware-classes.md)
</dt> <dt>

[**NetworkAdapterConfiguration de Win32 \_**](win32-networkadapterconfiguration.md)
</dt> <dt>

[Tareas WMI: Redes](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[Tareas wmi: cuentas y dominios](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[Compatibilidad con IPv6 e IPv4 en WMI](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

