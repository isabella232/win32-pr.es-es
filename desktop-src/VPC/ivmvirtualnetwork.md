---
title: Interfaz IVMVirtualNetwork (VPCCOMInterfaces.h)
description: Define una red virtual.
ms.assetid: 1ddafc33-05d4-45fb-924d-9830288aa240
keywords:
- IVMVirtualNetwork interface Virtual PC
- IVMVirtualNetwork interface Virtual PC , descrito
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
ms.openlocfilehash: a9caf5accb0add3354953d09e74a0893e2392deee7720b7a2cba0136b3f4b7c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118592590"
---
# <a name="ivmvirtualnetwork-interface"></a>IVMVirtualNetwork (interfaz)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Define una red virtual. **Los objetos IVMVirtualNetwork se** devuelven desde el método [**FindVirtualNetwork de IVMVirtualPC.**](ivmvirtualpc.md) [](ivmvirtualpc-findvirtualnetwork.md) También puede recuperar un **objeto IVMVirtualNetwork** del objeto [**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md) devuelto desde la [**propiedad IVMVirtualPC::VirtualNetworks.**](ivmvirtualpc-virtualnetworks.md)

Una red virtual consta de un conmutador virtual, que realiza todo el enrutamiento interno y varias conexiones que están "conectadas" al conmutador virtual. Estas conexiones pueden ser una conexión de host externo real, una "red interna" o redes compartidas (NAT).

## <a name="members"></a>Miembros

La **interfaz IVMVirtualNetwork** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMVirtualNetwork** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz IVMVirtualNetwork** tiene estos métodos.



| Método                                | Descripción                                                          |
|:--------------------------------------|:---------------------------------------------------------------------|
| [**\_Id**](ivmvirtualnetwork--id.md) | Recupera el identificador interno de la red virtual.<br/> |



 

### <a name="properties"></a>Propiedades

La **interfaz IVMVirtualNetwork** tiene estas propiedades.



| Propiedad                                                                | Tipo de acceso          | Descripción                                                                    |
|:------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [**HostAdapter**](ivmvirtualnetwork-hostadapter.md)<br/>         | Solo lectura<br/> | Nombre del adaptador al que está conectada la red virtual.<br/>  |
| [**MediaType**](/previous-versions/windows/desktop/legacy/dd796707(v=vs.85))<br/>             | Solo lectura<br/> | Determina si la instancia de red virtual es inalámbrica o no.<br/> |
| [**Nombre**](ivmvirtualnetwork-name.md)<br/>                       | Solo lectura<br/> | Nombre único de la instancia de red virtual.<br/>                    |
| [**NetworkAdapters**](ivmvirtualnetwork-networkadapters.md)<br/> | Solo lectura<br/> | Colección enumerable de NIC conectadas a la red virtual.<br/>   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualNetwork se define como \_ 431cb7a1-2469-4563-b94e-38b987adca63<br/>          |



 

