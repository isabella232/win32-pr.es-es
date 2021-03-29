---
description: El método estático de la clase WMI SetPMTUDiscovery se usa para habilitar la detección de la unidad de transmisión máxima (MTU) a través de la ruta de acceso a un host remoto.
ms.assetid: 43c640bb-c4e7-4b4b-9c18-6cc426229954
ms.tgt_platform: multiple
title: Método SetPMTUDiscovery de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetPMTUDiscovery
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ef3bc9ad5d6203077275f3665c4b0efc98265fbe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807573"
---
# <a name="setpmtudiscovery-method-of-the-win32_networkadapterconfiguration-class"></a>Método SetPMTUDiscovery de la \_ clase NetworkAdapterConfiguration de Win32

El método estático de la [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetPMTUDiscovery** se usa para habilitar la detección de la unidad de transmisión máxima (MTU) a través de la ruta de acceso a un host remoto.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetPMTUDiscovery(
  [in] boolean PMTUDiscoveryEnabled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PMTUDiscoveryEnabled* \[ de\]
</dt> <dd>

Si es **true**, TCP está habilitado para intentar detectar la unidad de transmisión máxima (MTU) o el tamaño de paquete más grande a través de la ruta de acceso a un host remoto. El valor predeterminado es **true**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, y un número diferente si se produce un error. Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Finalización correcta, no se requiere ningún reinicio**
</dt> <dd>

0

Finalización correcta, no es necesario reiniciar.

</dd> <dt>

**Finalización correcta, se requiere un reinicio**
</dt> <dd>

1

Finalización correcta, se requiere un reinicio.

</dd> <dt>

**Método no admitido en esta plataforma**
</dt> <dd>

64

El método no se admite en esta plataforma.

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

**Se produjo un error al procesar una instancia devuelta**
</dt> <dd>

67

Se produjo un error al procesar una instancia devuelta.

</dd> <dt>

**Parámetro de entrada no válido**
</dt> <dd>

68

Parámetro de entrada no válido.

</dd> <dt>

**Se especificaron más de 5 puertas de enlace**
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

**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**
</dt> <dd>

72

Error al obtener acceso al registro para obtener la información solicitada.

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

**No hay definido ningún servidor WINS principal/secundario**
</dt> <dd>

75

No hay definido ningún servidor WINS principal ni secundario.

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

**No se pudo copiar el archivo**
</dt> <dd>

78

No se pudo copiar el archivo.

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

**No se puede renovar la concesión DHCP**
</dt> <dd>

82

No se puede renovar la concesión DHCP.

</dd> <dt>

**No se puede liberar la concesión DHCP**
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

IPX no está habilitado en el adaptador.

</dd> <dt>

**Error de límite de número de trama/red**
</dt> <dd>

86

Error de límite de número de trama o de red.

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

**Parámetro fuera de los límites**
</dt> <dd>

90

Parámetro fuera de los límites.

</dd> <dt>

**Acceso denegado**
</dt> <dd>

91

Acceso denegado.

</dd> <dt>

**Memoria agotada**
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

No se encuentra la ruta de acceso, el archivo o el objeto.

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

**No se pudieron liberar o renovar todas las concesiones DHCP**
</dt> <dd>

98

No todas las concesiones DHCP se pueden liberar o renovar.

</dd> <dt>

**DHCP no está habilitado en el adaptador**
</dt> <dd>

100

DHCP no está habilitado en el adaptador.

</dd> <dt>

**Otros**
</dt> <dd>

101 4294967295

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al detectar la MTU de la ruta de acceso y limitar los segmentos TCP a este tamaño, TCP puede eliminar la fragmentación en los enrutadores a lo largo de la ruta de acceso que conecta las redes con diferentes MTU. La fragmentación afecta negativamente al rendimiento TCP y a la congestión de la red. Si se establece este parámetro en **false** , se usará una MTU de 576 bytes para todas las conexiones que no sean equipos de la subred local.

## <a name="examples"></a>Ejemplos

El ejemplo de la [habilitación de la detección de PMTU en todos los adaptadores de red](https://Gallery.TechNet.Microsoft.Com/dd68dc8d-d452-484c-add7-2da5c87c3568) de VBScript permite que un equipo detecte automáticamente la unidad de transmisión máxima en una red.

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

 

