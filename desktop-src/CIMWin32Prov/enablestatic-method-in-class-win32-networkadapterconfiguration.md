---
description: El método de clase WMI EnableStatic habilita el direccionamiento TCP/IP estático para el adaptador de red de destino. Como resultado, DHCP para este adaptador de red está deshabilitado.
ms.assetid: d0076424-58c0-4cfe-b55b-44c0f2620388
ms.tgt_platform: multiple
title: Método EnableStatic de la Win32_NetworkAdapterConfiguration clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableStatic
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 74a7b9ca8c8016cca5a78f2e7fe753f00398193e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062709"
---
# <a name="enablestatic-method-of-the-win32_networkadapterconfiguration-class"></a>Método EnableStatic de la clase NetworkAdapterConfiguration de Win32 \_

El método de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **EnableStatic** habilita el direccionamiento TCP/IP estático para el adaptador de red de destino. Como resultado, DHCP para este adaptador de red está deshabilitado.

En este tema se usa Managed Object Format sintaxis MOF . Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 EnableStatic(
  [in] string IPAddress[],
  [in] string SubnetMask[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*IPAddress* \[ En\]
</dt> <dd>

Enumera todas las direcciones IP estáticas del adaptador de red actual.

Ejemplo: 155.34.22.0.

</dd> <dt>

*SubnetMask* \[ En\]
</dt> <dd>

Máscaras de subred que complementan los valores del *parámetro IPAddress.*

Ejemplo: 255.255.0.0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere un reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio y cualquier otro número si se produce un error. Para obtener más información sobre los códigos de error, vea [**Wmi Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

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

No se puede configurar el servicio DHCP. Para obtener más información, vea la sección Comentarios.

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

**2147786788**
</dt> <dd>

Bloqueo de escritura no habilitado. Para obtener más información, [**vea INetCfgLock::AcquireWriteLock**](/previous-versions/windows/hardware/network/ff547914(v=vs.85)).

</dd> <dt>

**Otros**
</dt> <dd>

101 4294967295

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al usar **EnableStatic** para cambiar la dirección IP del equipo remoto, mientras se conecta a través de ese adaptador, es probable que la conexión al equipo remoto sea flexible y reciba un mensaje de error rpc no disponible. (sin embargo, la configuración cambia). Para evitar este escenario, considere la posibilidad de cambiar la configuración de puerta de enlace o DNS antes de establecer la dirección IP del adaptador.

Cuando se **usa EnableStatic** para proporcionar a un adaptador una configuración de IP estática, la función devuelve un "81 - No se puede configurar el servicio DHCP" si el adaptador ya está configurado con una dirección estática. Sin embargo, la función sigue estableciendo correctamente con la nueva operación.

## <a name="examples"></a>Ejemplos

La [dirección IP estática y,](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) a continuación, unirse a un ejemplo de código de PowerShell de dominio, en la Galería de TechNet, usa **EnableStatic** para agregar una dirección IP estática a un equipo local.

En [el ejemplo de código](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) DE VBScript Asignar una dirección IP estática, en la Galería de TechNet, se usa **EnableStatic** para establecer la dirección IP de un equipo.

En el ejemplo de VBScript siguiente se muestra cómo deshabilitar el uso de DHCP en una instancia de [**\_ NetworkAdapterConfiguration de Win32.**](win32-networkadapterconfiguration.md) En este caso, especificamos el adaptador con un índice de 0. Se debe seleccionar el índice correcto de las instancias de NetworkAdapter de Win32 \_ para otras interfaces.

> [!Note]  
> Este script solo se aplica a los sistemas basados en NT. Cambie las variables de ipaddr y subred siguientes a los valores que desea aplicar al adaptador.

 


```VB
Set Adapter = GetObject("winmgmts:Win32_NetworkAdapterConfiguration=1")

ipaddr = Array("1.1.1.1")
subnet = Array("255.255.255.0")


RetVal = Adapter.EnableStatic(ipaddr,subnet)

if RetVal = 0 then 
 WScript.Echo "DHCP disabled, using static IP address"
else 
 WScript.Echo "DHCP disable failed"
end if
```



En el ejemplo de Perl siguiente se muestra cómo deshabilitar el uso de DHCP en una instancia de [**\_ NetworkAdapterConfiguration de Win32.**](win32-networkadapterconfiguration.md) En este caso, especificamos el adaptador con un índice de 0. Se debe seleccionar el índice correcto de las instancias de NetworkAdapter de Win32 \_ para otras interfaces.

> [!Note]  
> Este script solo se aplica a los sistemas basados en NT. Cambie las variables de ipaddr y subred siguientes a los valores que desea aplicar al adaptador.

 


```
use strict;
use Win32::OLE;

my ($Adapter, @ipaddr, @subnet, $RetVal);  
eval { $Adapter = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2:Win32_NetworkAdapterConfiguration.Index=\"0\""); };

unless ($@) 
{
 push @ipaddr, "192.168.144.107";
 push @subnet, "255.255.255.0";

 $RetVal = $Adapter->EnableStatic(\@ipaddr, \@subnet);

 if ($RetVal == 0) 
 {
  print "\nDHCP disabled, using static IP address\n";
 }
 else 
 {
  print "\nDHCP disable failed\n";
 }
}
else
{
 print STDERR "\n", Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

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

 

