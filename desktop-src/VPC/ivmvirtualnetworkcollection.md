---
title: Interfaz IVMVirtualNetworkCollection (VPCCOMInterfaces. h)
description: Define una colección de objetos IVMVirtualNetwork. Para obtener un objeto IVMVirtualNetworkCollection, use la propiedad VirtualNetworks de IVMVirtualPC.
ms.assetid: 3d595bc3-1a8d-4e09-a809-944d4dcdc675
keywords:
- Interfaz IVMVirtualNetworkCollection Virtual PC
- Interfaz IVMVirtualNetworkCollection Virtual PC, descripción
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
ms.openlocfilehash: 76935fd4a67983847e211d8aa53f4a616bed9d4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803463"
---
# <a name="ivmvirtualnetworkcollection-interface"></a>Interfaz IVMVirtualNetworkCollection

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define una colección de objetos [**IVMVirtualNetwork**](ivmvirtualnetwork.md) . Para obtener un objeto **IVMVirtualNetworkCollection** , use la propiedad [**IVMVirtualPC:: VirtualNetworks**](ivmvirtualpc-virtualnetworks.md) .

## <a name="members"></a>Miembros

La interfaz **IVMVirtualNetworkCollection** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMVirtualNetworkCollection** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La interfaz **IVMVirtualNetworkCollection** tiene estas propiedades.



| Propiedad                                                             | Tipo de acceso          | Descripción                                                                                                   |
|:---------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmvirtualnetworkcollection--newenum.md)<br/> | Solo lectura<br/> | Un enumerador de la colección.<br/>                                                                  |
| [**Contabiliza**](ivmvirtualnetworkcollection-count.md)<br/>        | Solo lectura<br/> | El número de redes virtuales de esta colección.<br/>                                                 |
| [**Elemento**](ivmvirtualnetworkcollection-item.md)<br/>          | Solo lectura<br/> | El objeto [**IVMVirtualNetwork**](ivmvirtualnetwork.md) que corresponde al índice especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                     |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                      |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                           |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                  |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl>  |
| IID<br/>                      | IID \_ IVMVirtualNetworkCollection se define como 8ed680be-4242-4B2A-a21c-1982d8b0f675<br/> |



 

