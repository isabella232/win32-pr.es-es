---
description: Establece los pares de número de red y trama de Exchange (IPX) de Internetworking Packet Exchange (IPX) para este adaptador de red.
ms.assetid: 8190564f-7d9f-4b05-9949-2e732ce36dba
ms.tgt_platform: multiple
title: Método SetIPXFrameTypeNetworkPairs de la Win32_NetworkAdapterConfiguration clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPXFrameTypeNetworkPairs
api_type:
- COM
api_location:
- cimwin32.dll
ms.openlocfilehash: e4d53ec7b5600a767505e517a02fbf87b5a43d13
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974464"
---
# <a name="setipxframetypenetworkpairs-method-of-the-win32_networkadapterconfiguration-class"></a>Método SetIPXFrameTypeNetworkPairs de la clase \_ NetworkAdapterConfiguration de Win32

Establece los pares de número de red y trama de Exchange (IPX) de Internetworking Packet Exchange (IPX) para este adaptador de red.

Windows 2000 y Windows NT 3.51 y posteriores usan un número de red IPX con fines de enrutamiento. Se asigna a cada combinación de adaptador de red o tipo de marco configurado en el sistema del equipo. Este número se conoce a veces como "número de red externa". Debe ser único para cada segmento de red. Si el tipo de fotograma se establece en AUTO, el número de red debe ser cero.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetIPXFrameTypeNetworkPairs(
  [in] string IPXNetworkNumber[],
  [in] uint32 IPXFrameType[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*IPXNetworkNumber* \[ En\]
</dt> <dd>

Matriz de caracteres que identifica de forma única un adaptador en el sistema informático. El transporte compatible con NETWare Link (NWLink) IPX/SPX en Windows 2000 y Windows NT 3.51 o posterior usa dos tipos diferentes de números de red. Este número se conoce a veces como número de red externa. Debe ser único para cada segmento de red. Los valores de esta lista de cadenas deben tener un valor correspondiente en el parámetro IPXFrameType que identifique el tipo de marco de paquete usado para esta red.

</dd> <dt>

*IPXFrameType* \[ En\]
</dt> <dd>

Matriz de enteros de identificadores de tipo de marco. Los valores de esta matriz corresponden a los elementos del *parámetro IPXNetworkNumber.*

<dt>

<span id="Ethernet_II"></span><span id="ethernet_ii"></span><span id="ETHERNET_II"></span>

**Ethernet II** (0)


</dt> <dd></dd> <dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

**Ethernet 802.3** (1)


</dt> <dd></dd> <dt>

<span id="Ethernet_802.2"></span><span id="ethernet_802.2"></span><span id="ETHERNET_802.2"></span>

**Ethernet 802.2** (2)


</dt> <dd></dd> <dt>

<span id="Ethernet_SNAP"></span><span id="ethernet_snap"></span><span id="ETHERNET_SNAP"></span>

**Ethernet SNAP** (3)


</dt> <dd></dd> <dt>

<span id="AUTO"></span><span id="auto"></span>

**AUTO** (255)


</dt> <dd></dd> </dl> </dd> </dl>

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



| Requisito | Value |
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

 

 




