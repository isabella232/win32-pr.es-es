---
description: El método estático de la clase WMI SetTcpUseRFC1122UrgentPointer se usa para especificar si TCP usa la especificación RFC 1122 para datos urgentes o el modo que usan los sistemas derivados de Diseño de software de Berkeley (BSD).
ms.assetid: f8d07690-2723-4bc3-b15f-a24d575456a7
ms.tgt_platform: multiple
title: Método SetTcpUseRFC1122UrgentPointer de la Win32_NetworkAdapterConfiguration clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpUseRFC1122UrgentPointer
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 928a809211288eb7f024c735ce033b819e5d49f7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174437"
---
# <a name="settcpuserfc1122urgentpointer-method-of-the-win32_networkadapterconfiguration-class"></a>Método SetTcpUseRFC1122UrgentPointer de la clase \_ NetworkAdapterConfiguration de Win32

El método estático de la clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetTcpUseRFC1122UrgentPointer** se usa para especificar si TCP usa la especificación RFC 1122 para datos urgentes o el modo que usan los sistemas derivados de Diseño de software de Berkeley (BSD).

En este tema se usa Managed Object Format sintaxis MOF . Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetTcpUseRFC1122UrgentPointer(
  [in] boolean TcpUseRFC1122UrgentPointer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TcpUseRFC1122UrgentPointer* \[ En\]
</dt> <dd>

Si **es true,** TCP usa la especificación RFC 1122. Si **es false,** los datos urgentes se envían en el modo utilizado por los sistemas derivados de BSD.

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

**Método no compatible con esta plataforma**
</dt> <dd>

64

Método no compatible con esta plataforma.

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

Acceso denegado.

</dd> <dt>

**Memoria sin memoria**
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

## <a name="remarks"></a>Observaciones

RFC 1122 y BSD interpretan el puntero urgente en el encabezado TCP y la longitud de los datos urgentes de forma diferente. No son interoperables. El valor predeterminado es el modo BSD.

## <a name="examples"></a>Ejemplos

El [ejemplo modificar el uso urgente](https://Gallery.TechNet.Microsoft.Com/0ff22a90-0be6-4914-8db7-aaf72cbea9cb) de punteros para todos los adaptadores de red de VBScript configura un equipo para que use la especificación RFC 1122 para los datos urgentes.

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

[Tareas WMI: Redes](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[Tareas wmi: cuentas y dominios](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[Compatibilidad con IPv6 e IPv4 en WMI](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

