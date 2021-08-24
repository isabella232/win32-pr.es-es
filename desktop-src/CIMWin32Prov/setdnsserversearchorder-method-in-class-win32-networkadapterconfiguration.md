---
description: SetDNSServerSearchOrder &\# 32; El método de clase WMI usa una matriz de elementos de cadena para establecer el orden de búsqueda del servidor.
ms.assetid: fce688fa-7264-4965-8e1c-138160e03a7e
ms.tgt_platform: multiple
title: Método SetDNSServerSearchOrder de la Win32_NetworkAdapterConfiguration clase
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
ms.openlocfilehash: 2ae53996e2f8199d552909a186ab17e6b7ec89857c9be24dc4d8d4bfe583cfea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759805"
---
# <a name="setdnsserversearchorder-method-of-the-win32_networkadapterconfiguration-class"></a>Método SetDNSServerSearchOrder de la clase \_ NetworkAdapterConfiguration de Win32

El método de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDNSServerSearchOrder** usa una matriz de elementos de cadena para establecer el orden de búsqueda del servidor.

En este tema se usa Managed Object Format sintaxis de MOF. Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetDNSServerSearchOrder(
  [in] string DNSServerSearchOrder[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DNSServerSearchOrder* \[ En\]
</dt> <dd>

Lista de direcciones IP del servidor para consultar los servidores DNS.

Ejemplo: 130.215.24.1 o 157.54.164.1

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere ningún reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio y un número diferente si se produce un error. Para obtener más información sobre los códigos de error, vea [**Wmi Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Finalización correcta, no se requiere reinicio** (0)
</dt> <dt>

**Finalización correcta, reinicio necesario** (1)
</dt> <dt>

**Método no admitido en esta plataforma** (64)
</dt> <dt>

**Error desconocido** (65)
</dt> <dt>

**Máscara de subred no válida** (66)
</dt> <dt>

**Error al procesar una instancia devuelta** (67)
</dt> <dt>

**Parámetro de entrada no** válido (68)
</dt> <dt>

**Más de 5 puertas de enlace especificadas** (69)
</dt> <dt>

**Dirección IP no válida** (70)
</dt> <dt>

**Dirección IP de puerta de enlace no** válida (71)
</dt> <dt>

**Error al acceder al Registro para obtener la información solicitada** (72)
</dt> <dt>

**Nombre de dominio no** válido (73)
</dt> <dt>

**Nombre de host no** válido (74)
</dt> <dt>

**No hay ningún servidor WINS principal** o secundario definido (75)
</dt> <dt>

**Archivo no** válido (76)
</dt> <dt>

**Ruta de acceso del sistema no** válida (77)
</dt> <dt>

**Error de copia de** archivos (78)
</dt> <dt>

**Parámetro de seguridad no** válido (79)
</dt> <dt>

**No se puede configurar el servicio TCP/IP** (80)
</dt> <dt>

**No se puede configurar el servicio DHCP** (81)
</dt> <dt>

**No se puede renovar la concesión dhcp** (82)
</dt> <dt>

**No se puede liberar la concesión dhcp** (83)
</dt> <dt>

**IP no habilitada en el adaptador** (84)
</dt> <dt>

**IPX no habilitado en el adaptador** (85)
</dt> <dt>

**Error de límites de número de red o marco** (86)
</dt> <dt>

**Tipo de fotograma no** válido (87)
</dt> <dt>

**Número de red no** válido (88)
</dt> <dt>

**Número de red duplicado** (89)
</dt> <dt>

**Parámetro fuera de límites** (90)
</dt> <dt>

**Acceso denegado** (91)
</dt> <dt>

**Memoria sin memoria** (92)
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

**No todas las concesiones DHCP se pudieron liberar o renovar** (98)
</dt> <dt>

**DHCP no habilitado en el adaptador** (100)
</dt> <dt>

**Otros** (101 4294967295)
</dt> </dl>

## <a name="remarks"></a>Comentarios

Se trata de una llamada de método dependiente de la instancia que se aplica por adaptador. Después de especificar que los servidores DNS estáticos empiecen a usar el Protocolo de configuración dinámica de host (DHCP) en lugar de los servidores DNS estáticos, puede llamar al método sin proporcionar parámetros "in".

## <a name="examples"></a>Ejemplos

El [ejemplo set DNS Server Search Order for Multiple Computers in an Organizational Unit](https://Gallery.TechNet.Microsoft.Com/Set-DNS-Server-Search-6a3e3ede) VBScript (Establecer orden de búsqueda del servidor DNS para varios equipos de una unidad organizativa de VBScript) de la Galería de TechNet recupera o establece el orden de búsqueda del servidor DNS para varios equipos que pertenecen a una unidad organizativa.

El [ejemplo modify the DNS Server Search Order for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/7824348c-5a92-42cb-b4e9-ef2187702e02) VBScript (Modificar el orden de búsqueda del servidor DNS para un adaptador de red VBScript) configura un adaptador de red enlazado a TCP/IP para usar dos servidores DNS.

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

 

