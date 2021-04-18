---
title: Interfaz IVMNetworkAdapter (VPCCOMInterfaces. h)
description: Actúa como la interfaz de una tarjeta de interfaz de red virtual.
ms.assetid: df050706-09be-47d1-9ae1-1eb0e1836d64
keywords:
- Interfaz IVMNetworkAdapter Virtual PC
- Interfaz IVMNetworkAdapter Virtual PC, descripción
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
ms.openlocfilehash: 74a0ccf722715896743129b6666609bd8a88df3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422358"
---
# <a name="ivmnetworkadapter-interface"></a>Interfaz IVMNetworkAdapter

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Actúa como la interfaz de una tarjeta de interfaz de red virtual (NIC). Se usa para configurar el modo en que una máquina virtual está en red. Las tarjetas de interfaz de red se pueden agregar y quitar mediante [**IVMVirtualMachine:: AddNetworkAdapter**](ivmvirtualmachine-addnetworkadapter.md) y [**IVMVirtualMachine:: RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md). También puede recuperar un objeto **IVMNetworkAdapter** de la colección [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md) devuelta desde las propiedades [**IVMVirtualMachine:: adaptadores**](ivmvirtualmachine-networkadapters.md) o [**IVMVirtualNetwork:: adaptadores**](ivmvirtualnetwork-networkadapters.md) .

## <a name="members"></a>Miembros

La interfaz **IVMNetworkAdapter** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMNetworkAdapter** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **IVMNetworkAdapter** tiene estos métodos.



| Método                                                                         | Descripción                                                                 |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [**\_id**](ivmnetworkadapter--id.md)                                          | Recupera el identificador interno de esta interfaz de red.<br/>     |
| [**AttachToVirtualNetwork**](ivmnetworkadapter-attachtovirtualnetwork.md)     | Conecta la interfaz de red a la red virtual especificada.<br/> |
| [**DetachFromVirtualNetwork**](ivmnetworkadapter-detachfromvirtualnetwork.md) | Desasocia la interfaz de red de su red virtual.<br/>         |



 

### <a name="properties"></a>Propiedades

La interfaz **IVMNetworkAdapter** tiene estas propiedades.



| Propiedad                                                                                  | Tipo de acceso           | Descripción                                                                 |
|:------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------|
| [**Denominaba ethernetaddress**](ivmnetworkadapter-ethernetaddress.md)<br/>                   | Lectura/escritura<br/> | Dirección Ethernet (MAC) de la interfaz de red.<br/>             |
| [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md)<br/> | Lectura/escritura<br/> | Indica si la dirección Ethernet se genera dinámicamente.<br/> |
| [**VirtualMachine**](ivmnetworkadapter-virtualmachine.md)<br/>                     | Solo lectura<br/>  | La máquina virtual asociada a esta interfaz de red.<br/>      |
| [**VirtualNetwork**](ivmnetworkadapter-virtualnetwork.md)<br/>                     | Solo lectura<br/>  | La red virtual a la que está conectada la interfaz de red.<br/>  |



 

## <a name="remarks"></a>Observaciones

La dirección Ethernet predeterminada para una interfaz de red es "00-00-00-00-00-00", que se considera una dirección Ethernet no válida en la mayoría de los sistemas operativos. Si [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) se establece en **false**, [**denominaba ethernetaddress**](ivmnetworkadapter-ethernetaddress.md) se debe inicializar con una dirección de red Ethernet válida.

En los procedimientos siguientes se explica cómo usar la interfaz **IVMNetworkAdapter** .

**Para asociar una NIC virtual a una NIC de host**

-   Las NIC virtuales (invitado) no se conectan directamente a una NIC de host. En su lugar, la NIC virtual se conecta a una red virtual que está conectada a una NIC de host. Para obtener más información sobre la configuración de redes virtuales, vea [**IVMVirtualNetwork**](ivmvirtualnetwork.md). Para asociar la NIC virtual a una red virtual, use el método [**AttachToVirtualNetwork**](ivmnetworkadapter-attachtovirtualnetwork.md) .

**Para desconectar una NIC virtual de la red virtual**

-   El método [**DetachFromVirtualNetwork**](ivmnetworkadapter-detachfromvirtualnetwork.md) desasociará la NIC virtual de la red virtual. Después de llamar a esta función, la propiedad [**VirtualNetwork**](ivmnetworkadapter-virtualnetwork.md) devolverá un identificador de red virtual que no es válido.

**Para quitar una NIC virtual de una máquina virtual si tiene el objeto NIC virtual**

1.  Obtenga la máquina virtual asociada a la NIC virtual mediante la propiedad [**VirtualMachine**](ivmnetworkadapter-virtualmachine.md) .
2.  Use el objeto actual como parámetro para el método [**IVMVirtualMachine:: RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMNetworkAdapter se define como e32e4165-22b8-4DC0-8d57-850171ae207a<br/>          |



 

