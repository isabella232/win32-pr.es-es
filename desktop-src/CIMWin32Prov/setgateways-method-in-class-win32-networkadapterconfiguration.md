---
description: SetGateways &\# 32; Método de clase WMI especifica una lista de puertas de enlace para enrutar paquetes a una subred diferente de la subred a la que está conectado el adaptador de red.
ms.assetid: 240f7aff-7a07-4e0d-af30-7bcabb68c736
ms.tgt_platform: multiple
title: Método SetGateways de la clase Win32_NetworkAdapterConfiguration
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
ms.openlocfilehash: 215bfa736a0f9d67ae587ac1f0e1b4aa394b85d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907324"
---
# <a name="setgateways-method-of-the-win32_networkadapterconfiguration-class"></a>Método SetGateways de la \_ clase NetworkAdapterConfiguration de Win32

El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetGateways** especifica una lista de puertas de enlace para enrutar paquetes a una subred diferente de la subred a la que está conectado el adaptador de red.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetGateways(
  [in]           string DefaultIPGateway[],
  [in, optional] uint16 GatewayCostMetric[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DefaultIPGateway* \[ de\]
</dt> <dd>

Lista de direcciones IP a las puertas de enlace en las que se enrutan los paquetes de red.

</dd> <dt>

*GatewayCostMetric* \[ en, opcional\]
</dt> <dd>

Asigna un valor que oscila entre 1 y 9999, que se usa para calcular las rutas más rápidas y confiables. Los valores de este parámetro se corresponden con los valores del parámetro *DefaultIPGateway* . El valor predeterminado de una puerta de enlace es 1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere un reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, y cualquier otro valor si se produce un error. Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Finalización correcta, no se requiere ningún reinicio**
</dt> <dd>

0

</dd> <dt>

**Finalización correcta, se requiere un reinicio**
</dt> <dd>

1

</dd> <dt>

**Método no admitido en esta plataforma**
</dt> <dd>

64

El método no se admite cuando la NIC está en modo DHCP.

</dd> <dt>

**Error desconocido**
</dt> <dd>

65

</dd> <dt>

**Máscara de subred no válida**
</dt> <dd>

66

</dd> <dt>

**Se produjo un error al procesar una instancia devuelta**
</dt> <dd>

67

</dd> <dt>

**Parámetro de entrada no válido**
</dt> <dd>

68

</dd> <dt>

**Se especificaron más de 5 puertas de enlace**
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

**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**
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

**No hay definido ningún servidor WINS principal/secundario**
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

**No se pudo copiar el archivo**
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

**No se puede renovar la concesión DHCP**
</dt> <dd>

82

</dd> <dt>

**No se puede liberar la concesión DHCP**
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

**Error de límite de número de trama/red**
</dt> <dd>

86

</dd> <dt>

**Tipo de marco no válido**
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

**Parámetro fuera de los límites**
</dt> <dd>

90

</dd> <dt>

**Acceso denegado**
</dt> <dd>

91

</dd> <dt>

**Memoria agotada**
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

**No se pudieron liberar o renovar todas las concesiones DHCP**
</dt> <dd>

98

</dd> <dt>

**DHCP no está habilitado en el adaptador**
</dt> <dd>

100

</dd> <dt>

**Otros**
</dt> <dd>

101 4294967295

</dd> </dl>

## <a name="remarks"></a>Observaciones

Este método solo funciona cuando la tarjeta de interfaz de red (NIC) está en modo de dirección IP estática.

Para borrar la puerta de enlace, establezca la puerta de enlace en la misma dirección IP que usa en [**EnableStatic**](enablestatic-method-in-class-win32-networkadapterconfiguration.md).

## <a name="examples"></a>Ejemplos

En el ejemplo de VBScript [modificar las puertas de enlace para un adaptador de red](https://Gallery.TechNet.Microsoft.Com/9ea7670b-f68f-4efb-9cd2-7c299a8f657f) se configuran dos puertas de enlace para un adaptador de red.

En el ejemplo de la [asignación de una dirección IP estática](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) de VBScript se establece la dirección IP y la puerta de enlace de un equipo.

La [dirección IP estática y, a continuación, unirse a un dominio](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) de ejemplo de PowerShell ayuda en la reconstrucción de máquinas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases de hardware de sistema del equipo](computer-system-hardware-classes.md)
</dt> <dt>

[**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md)
</dt> <dt>

[Tareas de WMI: redes](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[Tareas de WMI: cuentas y dominios](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[Compatibilidad con IPv6 e IPv4 en WMI](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

