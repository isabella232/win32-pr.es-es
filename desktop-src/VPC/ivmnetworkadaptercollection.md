---
title: Interfaz IVMNetworkAdapterCollection (VPCCOMInterfaces.h)
description: Define una colección de tarjetas de interfaz de red virtual. Para obtener un objeto IVMNetworkAdapterCollection, use las propiedades IVMVirtualMachine NetworkAdapters, IVMVirtualNetwork NetworkAdapters e IVMVirtualPC UnconnectedNetworkAdapters.
ms.assetid: cfb03a7c-a568-488c-9284-798b7e21027a
keywords:
- IVMNetworkAdapterCollection interface Virtual PC
- IVMNetworkAdapterCollection interface Virtual PC , descrito
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b532f96343ac0ced3598b8da9f74f1334e6a081e8217994ffce1d2314cadfc79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973963"
---
# <a name="ivmnetworkadaptercollection-interface"></a>IVMNetworkAdapterCollection (interfaz)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Define una colección de tarjetas de interfaz de red virtual. Para obtener un objeto IVMNetworkAdapterCollection, use las propiedades [**IVMVirtualMachine::NetworkAdapters**](ivmvirtualmachine-networkadapters.md), [**IVMVirtualNetwork::NetworkAdapters**](ivmvirtualnetwork-networkadapters.md)e [**IVMVirtualPC::UnconnectedNetworkAdapters.**](ivmvirtualpc-unconnectednetworkadapters.md)

## <a name="members"></a>Miembros

La **interfaz IVMNetworkAdapterCollection** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMNetworkAdapterCollection** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IVMNetworkAdapterCollection** tiene estas propiedades.



| Propiedad                                                             | Tipo de acceso          | Descripción                                                                                                   |
|:---------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmnetworkadaptercollection--newenum.md)<br/> | Solo lectura<br/> | Un enumerador de la colección.<br/>                                                                  |
| [**Count**](ivmnetworkadaptercollection-count.md)<br/>        | Solo lectura<br/> | Número de interfaces de red de esta colección.<br/>                                               |
| [**Elemento**](ivmnetworkadaptercollection-item.md)<br/>          | Solo lectura<br/> | Objeto [**IVMNetworkAdapter**](ivmnetworkadapter.md) que corresponde al índice especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                     |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                      |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                           |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                  |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl>  |
| IID<br/>                      | IID \_ IVMNetworkAdapterCollection se define como ebaeafe9-ebcd-47cf-866e-ad87d735e479<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMNetworkAdapter**](ivmnetworkadapter.md)
</dt> <dt>

[**IVMVirtualMachine::NetworkAdapters**](ivmvirtualmachine-networkadapters.md)
</dt> <dt>

[**IVMVirtualNetwork::NetworkAdapters**](ivmvirtualnetwork-networkadapters.md)
</dt> <dt>

[**IVMVirtualPC::UnconnectedNetworkAdapters**](ivmvirtualpc-unconnectednetworkadapters.md)
</dt> </dl>

 

