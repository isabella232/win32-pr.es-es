---
description: El método de clase WMI SetDNSDomain permite establecer el dominio DNS.
ms.assetid: a531133e-1b7c-4d85-979d-63bf4f7c9bed
ms.tgt_platform: multiple
title: Método SetDNSDomain de la Win32_NetworkAdapterConfiguration clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDNSDomain
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a5fd02168c19a5424ef455380bd9e1251f2e8f6c48a9dd8ea5ec4e9e1a1b1e4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759915"
---
# <a name="setdnsdomain-method-of-the-win32_networkadapterconfiguration-class"></a>Método SetDNSDomain de la clase NetworkAdapterConfiguration de Win32 \_

El método de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDNSDomain** permite establecer el dominio DNS.

En este tema se usa Managed Object Format sintaxis MOF (MOF). Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetDNSDomain(
  [in] string DNSDomain
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DNSDomain* \[ En\]
</dt> <dd>

Dominio con el que está asociado el DNS, representado por un nombre de organización seguido de un punto y una extensión que indica el tipo de organización.

Ejemplo: "microsoft.com"

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

No todas las concesiones DHCP se pueden liberar o renovar.

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

## <a name="remarks"></a>Comentarios

Se trata de una llamada al método dependiente de la instancia que se aplica por adaptador. La configuración se aplica al adaptador de destino.

## <a name="examples"></a>Ejemplos

El ejemplo de [código DE](https://Gallery.TechNet.Microsoft.Com/6044a0a4-d320-4c18-a94b-c125796d219b) VBScript Asignar el dominio DNS para un adaptador de red en la galería de TechNet usa **SetDNSDomain** para establecer el dominio DNS para un adaptador de red enlazado a TCP/IP.

El [ejemplo de código Modify the TCP/IP Configuration for a Computer](https://Gallery.TechNet.Microsoft.Com/3d5ae334-1d75-4cea-8079-78c6bd836faf) VBScript de la Galería de TechNet usa **SetDNSDomain** para modificar la configuración de TCP/IP para un adaptador de red.

El [ejemplo Habilitar dhcp Configuración](https://Gallery.TechNet.Microsoft.Com/41e6ab51-78c0-4413-b086-03fde33ea125) en un equipo VBScript en la Galería de TechNet usa **SetDNSDomain** para configurar todas las opciones que normalmente se necesitan para habilitar DHCP en un equipo.

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

 

