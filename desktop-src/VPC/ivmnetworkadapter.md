---
title: Interfaz IVMNetworkAdapter (VPCCOMInterfaces.h)
description: Actúa como la interfaz de una tarjeta de interfaz de red virtual.
ms.assetid: df050706-09be-47d1-9ae1-1eb0e1836d64
keywords:
- IVMNetworkAdapter interface Virtual PC
- IVMNetworkAdapter interface Virtual PC , descrito
topic_type:
- apiref
api_name:
- IVMNetworkAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73622161629f6d3746c153fb9e2df32ee120fd748defc60d0d02ef6ea4378b14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118843902"
---
# <a name="ivmnetworkadapter-interface"></a>Interfaz IVMNetworkAdapter

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Actúa como interfaz para una tarjeta de interfaz de red virtual (NIC). Se usa para configurar cómo se redime una máquina virtual. Las tarjetas de interfaz de red se pueden agregar y quitar mediante [**IVMVirtualMachine::AddNetworkAdapter**](ivmvirtualmachine-addnetworkadapter.md) e [**IVMVirtualMachine::RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md). También puede recuperar un objeto **IVMNetworkAdapter** de la colección [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md) devuelta de las propiedades [**IVMVirtualMachine::NetworkAdapters**](ivmvirtualmachine-networkadapters.md) o [**IVMVirtualNetwork::NetworkAdapters.**](ivmvirtualnetwork-networkadapters.md)

## <a name="members"></a>Miembros

La **interfaz IVMNetworkAdapter** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMNetworkAdapter** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz IVMNetworkAdapter** tiene estos métodos.



| Método                                                                         | Descripción                                                                 |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [**\_ID**](ivmnetworkadapter--id.md)                                          | Recupera el identificador interno de esta interfaz de red.<br/>     |
| [**AttachToVirtualNetwork**](ivmnetworkadapter-attachtovirtualnetwork.md)     | Asocia la interfaz de red a la red virtual especificada.<br/> |
| [**DetachFromVirtualNetwork**](ivmnetworkadapter-detachfromvirtualnetwork.md) | Desasoja la interfaz de red de su red virtual.<br/>         |



 

### <a name="properties"></a>Propiedades

La **interfaz IVMNetworkAdapter** tiene estas propiedades.



| Propiedad                                                                                  | Tipo de acceso           | Descripción                                                                 |
|:------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------|
| [**EthernetAddress**](ivmnetworkadapter-ethernetaddress.md)<br/>                   | Lectura/escritura<br/> | Dirección Ethernet (MAC) de la interfaz de red.<br/>             |
| [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md)<br/> | Lectura/escritura<br/> | Indica si la dirección Ethernet se genera dinámicamente.<br/> |
| [**VirtualMachine**](ivmnetworkadapter-virtualmachine.md)<br/>                     | Solo lectura<br/>  | Máquina virtual asociada a esta interfaz de red.<br/>      |
| [**VirtualNetwork**](ivmnetworkadapter-virtualnetwork.md)<br/>                     | Solo lectura<br/>  | Red virtual a la que está conectada la interfaz de red.<br/>  |



 

## <a name="remarks"></a>Comentarios

La dirección Ethernet predeterminada para una interfaz de red es "00-00-00-00-00-00", que la mayoría de los sistemas operativos consideran una dirección Ethernet no válida. Si [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) está establecido en **FALSE,** [**EthernetAddress**](ivmnetworkadapter-ethernetaddress.md) debe inicializarse con una dirección de red Ethernet válida.

Los procedimientos siguientes explican cómo usar la **interfaz IVMNetworkAdapter.**

**Para asociar una NIC virtual a una NIC de host**

-   Las NIC virtuales (invitadas) no están conectadas directamente a una NIC de host. En su lugar, la NIC virtual se asocia a una red virtual que está conectada a una NIC de host. Para obtener más información sobre cómo configurar redes virtuales, vea [**IVMVirtualNetwork**](ivmvirtualnetwork.md). Para asociar la NIC virtual a una red virtual, use el [**método AttachToVirtualNetwork.**](ivmnetworkadapter-attachtovirtualnetwork.md)

**Para desconectar una NIC virtual de la red virtual**

-   El [**método DetachFromVirtualNetwork**](ivmnetworkadapter-detachfromvirtualnetwork.md) separará la NIC virtual de la red virtual. Después de llamar a esta función, la [**propiedad VirtualNetwork**](ivmnetworkadapter-virtualnetwork.md) devolverá un identificador de red virtual que no es válido.

**Para quitar una NIC virtual de una máquina virtual si tiene el objeto nic virtual**

1.  Obtenga la máquina virtual asociada a la NIC virtual mediante la [**propiedad VirtualMachine.**](ivmnetworkadapter-virtualmachine.md)
2.  Use el objeto actual como parámetro para el [**método IVMVirtualMachine::RemoveNetworkAdapter.**](ivmvirtualmachine-removenetworkadapter.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMNetworkAdapter se define como \_ e32e4165-22b8-4dc0-8d57-850171ae207a<br/>          |



 

