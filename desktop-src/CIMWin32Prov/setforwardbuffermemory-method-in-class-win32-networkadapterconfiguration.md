---
description: El método estático de la clase WMI SetForwardBufferMemory se usa para especificar cuánta memoria IP asigna para almacenar los datos del paquete en la cola de paquetes del enrutador.
ms.assetid: e76452e8-2ee8-4d39-9405-33b0aeeac74d
ms.tgt_platform: multiple
title: Método SetForwardBufferMemory de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetForwardBufferMemory
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 30179610e6eee121a86119fa347067b40ef04c2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907325"
---
# <a name="setforwardbuffermemory-method-of-the-win32_networkadapterconfiguration-class"></a>Método SetForwardBufferMemory de la \_ clase NetworkAdapterConfiguration de Win32

El método estático de la [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetForwardBufferMemory** se usa para especificar cuánta memoria IP asigna para almacenar los datos del paquete en la cola de paquetes del enrutador.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetForwardBufferMemory(
  [in] uint32 ForwardBufferMemory
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ForwardBufferMemory* \[ de\]
</dt> <dd>

Tamaño, en bytes, de la cola de paquetes del enrutador usada para almacenar los datos del paquete. El valor predeterminado es 74240 (paquetes de 50 1480 bytes, redondeado a un múltiplo de 256).

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

Cuando se rellena este espacio de búfer, el enrutador comienza a descartar los paquetes de forma aleatoria de su cola.

Los búferes de datos de cola de paquetes tienen una longitud de 256 bytes, por lo que el valor del parámetro *ForwardBufferMemory* debe ser un múltiplo de 256. Varios búferes están encadenados juntos para paquetes más grandes. El encabezado IP de un paquete se almacena por separado. Este parámetro se omite y no se asigna ningún búfer si el enrutador IP no está habilitado. El tamaño del búfer puede oscilar entre la unidad de transmisión máxima (MTU) de la red y un valor menor que 0xFFFFFFFF.

## <a name="examples"></a>Ejemplos

En el ejemplo de VBScript [modificar la memoria del búfer de reenvío para todos los adaptadores de red](https://Gallery.TechNet.Microsoft.Com/da5712dc-f854-4099-98a9-59c0ff20a524) se configura la memoria del búfer de reenvío para todos los adaptadores de red de un equipo.

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

 

