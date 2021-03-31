---
title: Interfaz IVMNetworkAdapterCollection (VPCCOMInterfaces. h)
description: Define una colección de tarjetas de interfaz de red virtual. Para obtener un objeto IVMNetworkAdapterCollection, use las propiedades IVMVirtualMachine adaptadores, IVMVirtualNetwork adaptadores y IVMVirtualPC UnconnectedNetworkAdapters.
ms.assetid: cfb03a7c-a568-488c-9284-798b7e21027a
keywords:
- Interfaz IVMNetworkAdapterCollection Virtual PC
- Interfaz IVMNetworkAdapterCollection Virtual PC, descripción
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
ms.openlocfilehash: 8005b88cb873f00708829672cdeb6563b606d42b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079470"
---
# <a name="ivmnetworkadaptercollection-interface"></a>Interfaz IVMNetworkAdapterCollection

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define una colección de tarjetas de interfaz de red virtual. Para obtener un objeto IVMNetworkAdapterCollection, use las propiedades [**IVMVirtualMachine:: adaptadores**](ivmvirtualmachine-networkadapters.md), [**IVMVirtualNetwork:: adaptadores**](ivmvirtualnetwork-networkadapters.md)y [**IVMVirtualPC:: UnconnectedNetworkAdapters**](ivmvirtualpc-unconnectednetworkadapters.md) .

## <a name="members"></a>Miembros

La interfaz **IVMNetworkAdapterCollection** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMNetworkAdapterCollection** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La interfaz **IVMNetworkAdapterCollection** tiene estas propiedades.



| Propiedad                                                             | Tipo de acceso          | Descripción                                                                                                   |
|:---------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmnetworkadaptercollection--newenum.md)<br/> | Solo lectura<br/> | Un enumerador de la colección.<br/>                                                                  |
| [**Contabiliza**](ivmnetworkadaptercollection-count.md)<br/>        | Solo lectura<br/> | Número de interfaces de red de esta colección.<br/>                                               |
| [**Elemento**](ivmnetworkadaptercollection-item.md)<br/>          | Solo lectura<br/> | El objeto [**IVMNetworkAdapter**](ivmnetworkadapter.md) que corresponde al índice especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                     |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                      |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                           |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                  |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl>  |
| IID<br/>                      | IID \_ IVMNetworkAdapterCollection se define como ebaeafe9-eBCD-47cf-866e-ad87d735e479<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMNetworkAdapter**](ivmnetworkadapter.md)
</dt> <dt>

[**IVMVirtualMachine:: adaptadores**](ivmvirtualmachine-networkadapters.md)
</dt> <dt>

[**IVMVirtualNetwork:: adaptadores**](ivmvirtualnetwork-networkadapters.md)
</dt> <dt>

[**IVMVirtualPC::UnconnectedNetworkAdapters**](ivmvirtualpc-unconnectednetworkadapters.md)
</dt> </dl>

 

