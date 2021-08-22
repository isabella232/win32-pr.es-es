---
title: Interfaz IVMVirtualNetworkCollection (VPCCOMInterfaces.h)
description: Define una colección de objetos IVMVirtualNetwork. Para obtener un objeto IVMVirtualNetworkCollection, use la propiedad IVMVirtualPC VirtualNetworks.
ms.assetid: 3d595bc3-1a8d-4e09-a809-944d4dcdc675
keywords:
- IVMVirtualNetworkCollection interface Virtual PC
- IVMVirtualNetworkCollection interface Virtual PC , descrito
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32694b311482e58635ca28dc005fe68ab08495c15d251e176fb78266e7624e29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118592276"
---
# <a name="ivmvirtualnetworkcollection-interface"></a>Interfaz IVMVirtualNetworkCollection

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Define una colección de [**objetos IVMVirtualNetwork.**](ivmvirtualnetwork.md) Para obtener un **objeto IVMVirtualNetworkCollection,** use la [**propiedad IVMVirtualPC::VirtualNetworks.**](ivmvirtualpc-virtualnetworks.md)

## <a name="members"></a>Miembros

La **interfaz IVMVirtualNetworkCollection** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMVirtualNetworkCollection** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IVMVirtualNetworkCollection** tiene estas propiedades.



| Propiedad                                                             | Tipo de acceso          | Descripción                                                                                                   |
|:---------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmvirtualnetworkcollection--newenum.md)<br/> | Solo lectura<br/> | Un enumerador de la colección.<br/>                                                                  |
| [**Contar**](ivmvirtualnetworkcollection-count.md)<br/>        | Solo lectura<br/> | Número de redes virtuales de esta colección.<br/>                                                 |
| [**Elemento**](ivmvirtualnetworkcollection-item.md)<br/>          | Solo lectura<br/> | Objeto [**IVMVirtualNetwork**](ivmvirtualnetwork.md) que corresponde al índice especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                     |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                      |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                           |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                  |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl>  |
| IID<br/>                      | IID \_ IVMVirtualNetworkCollection se define como 8ed680be-4242-4b2a-a21c-1982d8b0f675<br/> |



 

