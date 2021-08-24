---
description: Establece el número de red virtual Exchange paquetes de Internetworking (IPX) en el sistema de equipo de destino.
ms.assetid: 52064250-b94f-4dc0-bf1a-8601cd135a90
ms.tgt_platform: multiple
title: Método SetIPXVirtualNetworkNumber de la Win32_NetworkAdapterConfiguration clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPXVirtualNetworkNumber
api_type:
- COM
api_location:
- cimwin32.dll
ms.openlocfilehash: 37af763450eab2fdba373fe21bfde5c0b4e1e38fda1f42aff59c425ba6b10000
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079779"
---
# <a name="setipxvirtualnetworknumber-method-of-the-win32_networkadapterconfiguration-class"></a>Método SetIPXVirtualNetworkNumber de la clase \_ NetworkAdapterConfiguration de Win32

Establece el número de red virtual Exchange paquetes de Internetworking (IPX) en el sistema de equipo de destino. Windows 2000 y Windows NT 3.51 o superior usa un número de red interno para el enrutamiento interno. El número de red interno también se conoce como número de red virtual. Identifica de forma única el sistema informático de la red. El método devuelve un valor entero que se puede interpretar de la siguiente manera:

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetIPXVirtualNetworkNumber(
  [in] string IPXVirtualNetNumber
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*IPXVirtualNetNumber* \[ En\]
</dt> <dd>

Número de red virtual para este sistema.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

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

**Otros** (101–4294967295)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CimWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Cimwin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**NetworkAdapterConfiguration de Win32 \_**](win32-networkadapterconfiguration.md)
</dt> </dl>

 

 




