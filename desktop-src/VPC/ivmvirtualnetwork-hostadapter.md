---
title: Propiedad IVMVirtualNetwork HostAdapter (VPCCOMInterfaces.h)
description: Nombre del adaptador al que está conectada la red virtual.
ms.assetid: 7ee074d2-13ba-42db-84db-ecfd22576a9a
keywords:
- HostAdapter, propiedad Virtual PC
- Propiedad HostAdapter Virtual PC , interfaz IVMVirtualNetwork
- Interfaz IVMVirtualNetwork Pc virtual, propiedad HostAdapter
topic_type:
- apiref
api_name:
- IVMVirtualNetwork.HostAdapter
- IVMVirtualNetwork.get_HostAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72db5d8349572b2bd3549c2ee54d20e994bdfe8aed6ba0fbe31875e04f6942f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122685"
---
# <a name="ivmvirtualnetworkhostadapter-property"></a>Propiedad IVMVirtualNetwork::HostAdapter

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera el nombre del adaptador al que está conectada la red virtual.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_HostAdapter(
  [out, retval] BSTR *hostAdapter
);
```



## <a name="property-value"></a>Valor de propiedad

Nombre del adaptador de host al que está conectada la red virtual.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                            | Significado                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                               | La operación se realizó correctamente.<br/>                                                                                                                              |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>                 | El parámetro es **NULL.**<br/>                                                                                                                                 |
| <dl> <dt>Máquina virtual \_ NO \_ SE ENCONTRÓ EL \_ \_ ADAPTADOR</dt> <dt>0XA0040700</dt> </dl> | El adaptador Ethernet de host al que se conectó esta red virtual ya no está disponible. Es posible que el adaptador Ethernet del host se haya quitado o deshabilitado.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>         | Se produjo un error inesperado.<br/>                                                                                                                          |



## <a name="remarks"></a>Comentarios

El adaptador de red virtual permite que una red virtual se hable con redes externas. Normalmente hay un adaptador por adaptador Ethernet instalado en el equipo host. Por ejemplo, supongamos que una máquina host tenía un adaptador con la etiqueta "10/100 ENET". Para conectar una NIC virtual a la red conectada a "10/100 ENET", establezca la propiedad **HostAdapter** de red de la red virtual en "10/100 ENET" y conecte la NIC virtual a esta red virtual.

Si la **propiedad HostAdapter** está establecida en una cadena vacía (""), el adaptador nic virtual se conecta a la red "Red interna" o "Redes compartidas (NAT)". Las NIC virtuales conectadas a la red "Red interna" no tendrán acceso a redes externas en el host del sistema. Sin embargo, las NIC virtuales conectadas a esta red virtual todavía pueden comunicarse entre sí.

Se puede acceder a la lista completa de adaptadores a través de la [**propiedad IVMHostInfo::NetworkAdapters.**](ivmhostinfo-networkadapters.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualNetwork se define como \_ 431cb7a1-2469-4563-b94e-38b987adca63<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualNetwork**](ivmvirtualnetwork.md)
</dt> </dl>

 

