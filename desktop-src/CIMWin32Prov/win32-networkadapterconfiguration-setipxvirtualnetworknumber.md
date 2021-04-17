---
description: Establece el número de red virtual de intercambio de paquetes de interredes (IPX) en el sistema del equipo de destino.
ms.assetid: 52064250-b94f-4dc0-bf1a-8601cd135a90
ms.tgt_platform: multiple
title: Método SetIPXVirtualNetworkNumber de la clase Win32_NetworkAdapterConfiguration
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
ms.openlocfilehash: ed6e6802a17ef6ec4393d2ae0c5ec43f0e21d247
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659706"
---
# <a name="setipxvirtualnetworknumber-method-of-the-win32_networkadapterconfiguration-class"></a>Método SetIPXVirtualNetworkNumber de la \_ clase NetworkAdapterConfiguration de Win32

Establece el número de red virtual de intercambio de paquetes de interredes (IPX) en el sistema del equipo de destino. Windows 2000 y Windows NT 3,51 o superior usan un número de red interno para el enrutamiento interno. El número de red interna también se conoce como un número de red virtual. Identifica de forma única el sistema del equipo en la red. El método devuelve un valor entero que se puede interpretar de la siguiente manera:

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetIPXVirtualNetworkNumber(
  [in] string IPXVirtualNetNumber
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*IPXVirtualNetNumber* \[ de\]
</dt> <dd>

Número de red virtual para este sistema.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

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

**Otro** (101 – 4294967295)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CimWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Cimwin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md)
</dt> </dl>

 

 




