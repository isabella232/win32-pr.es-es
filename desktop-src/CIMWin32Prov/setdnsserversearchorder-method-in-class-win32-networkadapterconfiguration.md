---
description: SetDNSServerSearchOrder &\# 32; El método de clase WMI utiliza una matriz de elementos de cadena para establecer el orden de búsqueda de servidores.
ms.assetid: fce688fa-7264-4965-8e1c-138160e03a7e
ms.tgt_platform: multiple
title: Método SetDNSServerSearchOrder de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDNSServerSearchOrder
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2bfe731ea1d89e8e0ad702bfa229a61fba30dfc7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080236"
---
# <a name="setdnsserversearchorder-method-of-the-win32_networkadapterconfiguration-class"></a>Método SetDNSServerSearchOrder de la \_ clase NetworkAdapterConfiguration de Win32

El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDNSServerSearchOrder** utiliza una matriz de elementos de cadena para establecer el orden de búsqueda de servidores.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetDNSServerSearchOrder(
  [in] string DNSServerSearchOrder[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DNSServerSearchOrder* \[ de\]
</dt> <dd>

Lista de direcciones IP de servidor para consultar los servidores DNS.

Ejemplo: 130.215.24.1 o 157.54.164.1

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, y un número diferente si se produce un error. Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Finalización correcta, no es necesario reiniciar** (0)
</dt> <dt>

**Finalización correcta, se requiere un reinicio** (1)
</dt> <dt>

**Método no admitido en esta plataforma** (64)
</dt> <dt>

**Error desconocido** (65)
</dt> <dt>

**Máscara de subred no válida** (66)
</dt> <dt>

**Se produjo un error al procesar una instancia devuelta** (67)
</dt> <dt>

**Parámetro de entrada no válido** (68)
</dt> <dt>

Se **especificaron más de 5 puertas de enlace** (69)
</dt> <dt>

**Dirección IP no válida** (70)
</dt> <dt>

**Dirección IP de puerta de enlace no válida** (71)
</dt> <dt>

**Se produjo un error al obtener acceso al registro para obtener la información solicitada** (72)
</dt> <dt>

**Nombre de dominio no válido** (73)
</dt> <dt>

**Nombre de host no válido** (74)
</dt> <dt>

**No se definió ningún servidor WINS principal/secundario** (75)
</dt> <dt>

**Archivo no válido** (76)
</dt> <dt>

**Ruta de acceso del sistema no válida** (77)
</dt> <dt>

**No se pudo copiar el archivo** (78)
</dt> <dt>

**Parámetro de seguridad no válido** (79)
</dt> <dt>

**No se puede configurar el servicio TCP/IP** (80)
</dt> <dt>

**No se puede configurar el servicio DHCP** (81)
</dt> <dt>

**No se puede renovar la concesión DHCP** (82)
</dt> <dt>

**No se puede liberar la concesión DHCP** (83)
</dt> <dt>

**IP no habilitada en el adaptador** (84)
</dt> <dt>

**IPX no habilitado en el adaptador** (85)
</dt> <dt>

**Error de límite de número de trama/red** (86)
</dt> <dt>

**Tipo de marco no válido** (87)
</dt> <dt>

**Número de red no válido** (88)
</dt> <dt>

**Número de red duplicada** (89)
</dt> <dt>

**Parámetro fuera de los límites** (90)
</dt> <dt>

**Acceso denegado** (91)
</dt> <dt>

**Memoria insuficiente** (92)
</dt> <dt>

**Ya existe** (93)
</dt> <dt>

**Ruta de acceso, archivo u objeto no encontrado** (94)
</dt> <dt>

**No se puede notificar al servicio** (95)
</dt> <dt>

**No se puede notificar al servicio DNS** (96)
</dt> <dt>

**Interfaz no configurable** (97)
</dt> <dt>

**No todas las concesiones DHCP se pueden liberar o renovar** (98)
</dt> <dt>

**DHCP no está habilitado en el adaptador** (100)
</dt> <dt>

**Otro** (101 4294967295)
</dt> </dl>

## <a name="remarks"></a>Observaciones

Se trata de una llamada de método dependiente de la instancia que se aplica por cada adaptador. Una vez especificados los servidores DNS estáticos para empezar a usar el protocolo de configuración dinámica de host (DHCP) en lugar de los servidores DNS estáticos, puede llamar al método sin proporcionar parámetros "in".

## <a name="examples"></a>Ejemplos

El ejemplo [establecer el orden de búsqueda de servidores DNS para varios equipos de una unidad organizativa](https://Gallery.TechNet.Microsoft.Com/Set-DNS-Server-Search-6a3e3ede) de VBScript en la galería de TechNet recupera o establece el orden de búsqueda del servidor DNS para varios equipos que pertenecen a una unidad organizativa.

En el ejemplo de VBScript [modificar el orden de búsqueda del servidor DNS para un adaptador de red](https://Gallery.TechNet.Microsoft.Com/7824348c-5a92-42cb-b4e9-ef2187702e02) se configura un adaptador de red enlazado a TCP/IP para usar dos servidores DNS.

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

 

