---
description: SetGateways &\# 32; El método de clase WMI especifica una lista de puertas de enlace para enrutar paquetes a una subred diferente de la subred a la que está conectado el adaptador de red.
ms.assetid: 240f7aff-7a07-4e0d-af30-7bcabb68c736
ms.tgt_platform: multiple
title: Método SetGateways de la Win32_NetworkAdapterConfiguration clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetGateways
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 190076822a181d7b0731cb1e7b42eb0cd9d35e37c64aa0736245d1e58994763b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759725"
---
# <a name="setgateways-method-of-the-win32_networkadapterconfiguration-class"></a>Método SetGateways de la clase \_ NetworkAdapterConfiguration de Win32

El método de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetGateways** especifica una lista de puertas de enlace para enrutar paquetes a una subred diferente de la subred a la que está conectado el adaptador de red.

En este tema se usa Managed Object Format sintaxis de MOF. Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetGateways(
  [in]           string DefaultIPGateway[],
  [in, optional] uint16 GatewayCostMetric[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DefaultIPGateway* \[ En\]
</dt> <dd>

Lista de direcciones IP a puertas de enlace en las que se enrutados los paquetes de red.

</dd> <dt>

*GatewayCostMetric* \[ in, opcional\]
</dt> <dd>

Asigna un valor que oscila entre 1 y 9999, que se usa para calcular las rutas más rápidas y confiables. Los valores de este parámetro se corresponden con los valores del *parámetro DefaultIPGateway.* El valor predeterminado de una puerta de enlace es 1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere un reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio y cualquier otro valor si se produce un error. Para obtener más información sobre los códigos de error, vea [**Wmi Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Finalización correcta, no se requiere reinicio**
</dt> <dd>

0

</dd> <dt>

**Finalización correcta, reinicio necesario**
</dt> <dd>

1

</dd> <dt>

**Método no admitido en esta plataforma**
</dt> <dd>

64

Método no admitido cuando la NIC está en modo DHCP.

</dd> <dt>

**Error desconocido**
</dt> <dd>

65

</dd> <dt>

**Máscara de subred no válida**
</dt> <dd>

66

</dd> <dt>

**Error al procesar una instancia que se devolvió**
</dt> <dd>

67

</dd> <dt>

**Parámetro de entrada no válido**
</dt> <dd>

68

</dd> <dt>

**Más de 5 puertas de enlace especificadas**
</dt> <dd>

69

</dd> <dt>

**Dirección IP no válida**
</dt> <dd>

70

</dd> <dt>

**Dirección IP de puerta de enlace no válida**
</dt> <dd>

71

</dd> <dt>

**Error al acceder al Registro para obtener la información solicitada**
</dt> <dd>

72

</dd> <dt>

**Nombre de dominio no válido**
</dt> <dd>

73

</dd> <dt>

**Nombre de host no válido**
</dt> <dd>

74

</dd> <dt>

**No se ha definido ningún servidor WINS principal o secundario**
</dt> <dd>

75

</dd> <dt>

**Archivo no válido**
</dt> <dd>

76

</dd> <dt>

**Ruta de acceso del sistema no válida**
</dt> <dd>

77

</dd> <dt>

**Error de copia de archivos**
</dt> <dd>

78

</dd> <dt>

**Parámetro de seguridad no válido**
</dt> <dd>

79

</dd> <dt>

**No se puede configurar el servicio TCP/IP**
</dt> <dd>

80

</dd> <dt>

**No se puede configurar el servicio DHCP**
</dt> <dd>

81

</dd> <dt>

**No se puede renovar la concesión dhcp**
</dt> <dd>

82

</dd> <dt>

**No se puede liberar la concesión dhcp**
</dt> <dd>

83

</dd> <dt>

**IP no habilitada en el adaptador**
</dt> <dd>

84

</dd> <dt>

**IPX no habilitado en el adaptador**
</dt> <dd>

85

</dd> <dt>

**Error de límites de número de marco/red**
</dt> <dd>

86

</dd> <dt>

**Tipo de fotograma no válido**
</dt> <dd>

87

</dd> <dt>

**Número de red no válido**
</dt> <dd>

88

</dd> <dt>

**Número de red duplicado**
</dt> <dd>

89

</dd> <dt>

**Parámetro fuera de límites**
</dt> <dd>

90

</dd> <dt>

**Acceso denegado**
</dt> <dd>

91

</dd> <dt>

**No hay memoria suficiente**
</dt> <dd>

92

</dd> <dt>

**Ya existe**
</dt> <dd>

93

</dd> <dt>

**Ruta de acceso, archivo u objeto no encontrado**
</dt> <dd>

94

</dd> <dt>

**No se puede notificar al servicio**
</dt> <dd>

95

</dd> <dt>

**No se puede notificar al servicio DNS**
</dt> <dd>

96

</dd> <dt>

**Interfaz no configurable**
</dt> <dd>

97

</dd> <dt>

**No todas las concesiones DHCP se podrían liberar o renovar**
</dt> <dd>

98

</dd> <dt>

**DHCP no habilitado en el adaptador**
</dt> <dd>

100

</dd> <dt>

**Otros**
</dt> <dd>

101 4294967295

</dd> </dl>

## <a name="remarks"></a>Comentarios

Este método solo funciona cuando la tarjeta de interfaz de red (NIC) está en modo IP estático.

Para borrar la puerta de enlace, establezca la puerta de enlace en la misma dirección IP que usa en [**EnableStatic.**](enablestatic-method-in-class-win32-networkadapterconfiguration.md)

## <a name="examples"></a>Ejemplos

El [ejemplo modificar las puertas de enlace de](https://Gallery.TechNet.Microsoft.Com/9ea7670b-f68f-4efb-9cd2-7c299a8f657f) un adaptador de red de VBScript configura dos puertas de enlace para un adaptador de red.

El [ejemplo de VBScript](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) Asignar una dirección IP estática establece la dirección IP y la puerta de enlace de un equipo.

La [dirección IP estática y, a continuación, unirse a un dominio de](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) ejemplo de PowerShell ayudan a recompilar las máquinas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases de hardware del sistema de equipo](computer-system-hardware-classes.md)
</dt> <dt>

[**NetworkAdapterConfiguration de Win32 \_**](win32-networkadapterconfiguration.md)
</dt> <dt>

[Tareas wmi: redes](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[Tareas wmi: cuentas y dominios](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[Compatibilidad con IPv6 e IPv4 en WMI](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

