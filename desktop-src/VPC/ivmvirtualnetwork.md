---
title: Interfaz IVMVirtualNetwork (VPCCOMInterfaces. h)
description: Define una red virtual.
ms.assetid: 1ddafc33-05d4-45fb-924d-9830288aa240
keywords:
- Interfaz IVMVirtualNetwork Virtual PC
- Interfaz IVMVirtualNetwork Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06fb7c759059034874890f1dba7f7e2d1280ea8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105696034"
---
# <a name="ivmvirtualnetwork-interface"></a>Interfaz IVMVirtualNetwork

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define una red virtual. Los objetos **IVMVirtualNetwork** se devuelven desde el método [**IVMVirtualPC**](ivmvirtualpc.md) [**FindVirtualNetwork**](ivmvirtualpc-findvirtualnetwork.md). También puede recuperar un objeto **IVMVirtualNetwork** del objeto [**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md) devuelto desde la propiedad [**IVMVirtualPC:: VirtualNetworks**](ivmvirtualpc-virtualnetworks.md) .

Una red virtual se compone de un conmutador virtual, que realiza todo el enrutamiento interno y varias conexiones que están "conectadas" al conmutador virtual. Estas conexiones pueden ser una conexión de host externo real, una "red interna" o redes compartidas (NAT).

## <a name="members"></a>Miembros

La interfaz **IVMVirtualNetwork** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMVirtualNetwork** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **IVMVirtualNetwork** tiene estos métodos.



| Método                                | Descripción                                                          |
|:--------------------------------------|:---------------------------------------------------------------------|
| [**\_id**](ivmvirtualnetwork--id.md) | Recupera el identificador interno de la red virtual.<br/> |



 

### <a name="properties"></a>Propiedades

La interfaz **IVMVirtualNetwork** tiene estas propiedades.



| Propiedad                                                                | Tipo de acceso          | Descripción                                                                    |
|:------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [**HostAdapter**](ivmvirtualnetwork-hostadapter.md)<br/>         | Solo lectura<br/> | El nombre del adaptador al que está conectada la red virtual.<br/>  |
| [**MediaType**](/previous-versions/windows/desktop/legacy/dd796707(v=vs.85))<br/>             | Solo lectura<br/> | Determina si la instancia de red virtual es inalámbrica o no.<br/> |
| [**Name**](ivmvirtualnetwork-name.md)<br/>                       | Solo lectura<br/> | Nombre único de la instancia de la red virtual.<br/>                    |
| [**Adaptadores**](ivmvirtualnetwork-networkadapters.md)<br/> | Solo lectura<br/> | Colección enumerable de NIC conectadas a la red virtual.<br/>   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualNetwork se define como 431cb7a1-2469-4563-b94e-38b987adca63<br/>          |



 

