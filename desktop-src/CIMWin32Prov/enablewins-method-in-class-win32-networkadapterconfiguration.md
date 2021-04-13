---
description: EnableWINS &\# 32; El método estático de clase WMI habilita la configuración de Windows Internet Naming Service (WINS) específica de TCP/IP, pero es independiente del adaptador de red.
ms.assetid: ce0fb170-978f-4d70-bced-e530e43da719
ms.tgt_platform: multiple
title: Método EnableWINS de la clase Win32_NetworkAdapterConfiguration
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
ms.openlocfilehash: 77f5ba32606ff228908e8b7a1559a73ae5139e9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538692"
---
# <a name="enablewins-method-of-the-win32_networkadapterconfiguration-class"></a>Método EnableWINS de la \_ clase NetworkAdapterConfiguration de Win32

El método estático de la [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **EnableWINS** habilita la configuración de Windows Internet Naming Service (WINS) específica de TCP/IP, pero es independiente del adaptador de red.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

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

*DNSEnabledForWINSResolution* \[ de\]
</dt> <dd>

Si es **true**, el sistema de nombres de dominio (DNS) está habilitado para la resolución de nombres a través de la resolución de WINS.

</dd> <dt>

*WINSEnableLMHostsLookup* \[ de\]
</dt> <dd>

Si **es true**, se usan los archivos de búsqueda local. Los archivos de búsqueda contendrán las asignaciones de direcciones IP a los nombres de host.

</dd> <dt>

*WINSHostLookupFile* \[ en, opcional\]
</dt> <dd>

Archivos de búsqueda que contienen asignaciones de direcciones IP a nombres de host. Si está disponible, los archivos se encuentran en% SystemRoot% \\ system32 \\ drivers \\ .

</dd> <dt>

*WINSScopeID* \[ en, opcional\]
</dt> <dd>

Valor del identificador de ámbito que se anexará al final del nombre NetBIOS del equipo. Los sistemas que utilizan el mismo identificador de ámbito pueden comunicarse con este equipo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere ningún reinicio; 1 (uno) para una finalización correcta cuando se requiere un reinicio; un número diferente si se produce un error. Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

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

## <a name="examples"></a>Ejemplos

En el ejemplo de código de VBScript [enable WINS for All Network adapters](https://Gallery.TechNet.Microsoft.Com/64cae6dd-4155-4825-ab25-5727503edf5a) , en la galería de TechNet, se usa **ENABLEWINS** para habilitar WINS en todos los adaptadores de red instalados en un equipo.

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

 

