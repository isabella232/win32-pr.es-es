---
description: EnableWINS &\# 32; El método estático de clase WMI Windows configuración Naming Service Internet (WINS) específica de TCP/IP, pero independiente del adaptador de red.
ms.assetid: ce0fb170-978f-4d70-bced-e530e43da719
ms.tgt_platform: multiple
title: Método EnableWINS de la Win32_NetworkAdapterConfiguration clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableWINS
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ce820e515bb72cbd2521521726f2b6962c49ee1b453781b5d17993c45e0d22d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118676508"
---
# <a name="enablewins-method-of-the-win32_networkadapterconfiguration-class"></a>Método EnableWINS de la clase \_ NetworkAdapterConfiguration de Win32

El método estático de la clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **EnableWINS** Windows configuración de Naming Service Internet (WINS) específica de TCP/IP, pero independiente del adaptador de red.

En este tema se Managed Object Format sintaxis de MOF . Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 EnableWINS(
  [in]           boolean DNSEnabledForWINSResolution,
  [in]           boolean WINSEnableLMHostsLookup,
  [in, optional] string  WINSHostLookupFile,
  [in, optional] string  WINSScopeID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DNSEnabledForWINSResolution* \[ En\]
</dt> <dd>

Si **es true,** el Sistema de nombres de dominio (DNS) está habilitado para la resolución de nombres sobre la resolución WINS.

</dd> <dt>

*WINSEnableLMHostsLookup* \[ En\]
</dt> <dd>

Si **es true,** se usan archivos de búsqueda local. Los archivos de búsqueda contendrán asignaciones de direcciones IP a nombres de host.

</dd> <dt>

*WINSHostLookupFile* \[ in, opcional\]
</dt> <dd>

Archivos de búsqueda que contienen asignaciones de direcciones IP a nombres de host. Si está disponible, los archivos se encontrarán en %SystemRoot% \\ system32 \\ drivers \\ .

</dd> <dt>

*WINSScopeID* \[ in, opcional\]
</dt> <dd>

Valor de identificador de ámbito que se anexará al final del nombre NetBIOS del equipo. Los sistemas que usan el mismo identificador de ámbito pueden comunicarse con este equipo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere ningún reinicio; 1 (uno) para una finalización correcta cuando se requiere un reinicio; un número diferente si se produce un error. Para obtener más información sobre los códigos de error, vea [**Wmi Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

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

## <a name="examples"></a>Ejemplos

El ejemplo de código [Enable WINS for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/64cae6dd-4155-4825-ab25-5727503edf5a) VBScript (Habilitar WINS para todos los adaptadores de red de VBScript), en la Galería de TechNet, usa **EnableWINS** para habilitar WINS en todos los adaptadores de red instalados en un equipo.

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

 

