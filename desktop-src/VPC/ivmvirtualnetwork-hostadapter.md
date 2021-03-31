---
title: Propiedad IVMVirtualNetwork HostAdapter (VPCCOMInterfaces. h)
description: Nombre del adaptador al que está conectada la red virtual.
ms.assetid: 7ee074d2-13ba-42db-84db-ecfd22576a9a
keywords:
- Propiedad HostAdapter Virtual PC
- Propiedad HostAdapter Virtual PC, interfaz IVMVirtualNetwork
- Interfaz IVMVirtualNetwork Virtual PC, propiedad HostAdapter
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
ms.openlocfilehash: 0485303c2328a85c70779f16652121729546f3ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079629"
---
# <a name="ivmvirtualnetworkhostadapter-property"></a>IVMVirtualNetwork:: HostAdapter (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera el nombre del adaptador al que está conectada la red virtual.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_HostAdapter(
  [out, retval] BSTR *hostAdapter
);
```



## <a name="property-value"></a>Valor de propiedad

El nombre del adaptador de host al que está conectada la red virtual.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                            | Significado                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                               | La operación se realizó correctamente.<br/>                                                                                                                              |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>                 | El parámetro es **null**.<br/>                                                                                                                                 |
| <dl> <dt>Máquina virtual \_ \_ \_ No \_ se encontró el adaptador E</dt> <dt>0xA0040700</dt> </dl> | El adaptador Ethernet del host al que estaba conectada esta red virtual ya no está disponible. Es posible que se haya quitado o deshabilitado el adaptador Ethernet del host.<br/> |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl>         | Se produjo un error inesperado.<br/>                                                                                                                          |



## <a name="remarks"></a>Observaciones

El adaptador de red virtual permite que una red virtual se comunique con redes externas. Normalmente, hay un adaptador por cada adaptador Ethernet instalado en el equipo host. Por ejemplo, supongamos que un equipo host tenía un adaptador con la etiqueta "10/100 ENET". Para conectar una NIC virtual a la red conectada a "10/100 ENET", establezca la propiedad **HostAdapter** de red de la red virtual en "10/100 ENET" y conecte la NIC virtual a esta red virtual.

Si la propiedad **HostAdapter** se establece en una cadena vacía (""), el adaptador de NIC virtual se conecta a la red "red interna" o "redes compartidas (NAT)". Las NIC virtuales conectadas a la red "red interna" no tendrán acceso a las redes externas en el host del sistema. Sin embargo, las NIC virtuales conectadas a esta red virtual siguen pudiendo comunicarse entre sí.

Se puede tener acceso a la lista completa de adaptadores a través de la propiedad [**IVMHostInfo:: adaptadores**](ivmhostinfo-networkadapters.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualNetwork se define como 431cb7a1-2469-4563-b94e-38b987adca63<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualNetwork**](ivmvirtualnetwork.md)
</dt> </dl>

 

