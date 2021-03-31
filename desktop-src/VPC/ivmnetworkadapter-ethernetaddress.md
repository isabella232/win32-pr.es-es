---
title: Propiedad IVMNetworkAdapter denominaba ethernetaddress (VPCCOMInterfaces. h)
description: Dirección Ethernet (MAC) de la interfaz de red.
ms.assetid: 2d94c5b3-6b69-4fb1-bee4-081dc026dde3
keywords:
- Propiedad denominaba ethernetaddress Virtual PC
- Propiedad denominaba ethernetaddress Virtual PC, interfaz IVMNetworkAdapter
- Interfaz IVMNetworkAdapter Virtual PC, propiedad denominaba ethernetaddress
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.EthernetAddress
- IVMNetworkAdapter.get_EthernetAddress
- IVMNetworkAdapter.put_EthernetAddress
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7afb8f9035b0a663e01eeead95dc3f4f6bdec2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103800968"
---
# <a name="ivmnetworkadapterethernetaddress-property"></a>IVMNetworkAdapter:: denominaba ethernetaddress (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera y establece la dirección Ethernet (MAC) de la interfaz de red.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_EthernetAddress(
  [in]          BSTR ethernetAddress
);

HRESULT get_EthernetAddress(
  [out, retval] BSTR *ethernetAddress
);
```



## <a name="property-value"></a>Valor de propiedad

La dirección MAC de la NIC virtual. Debe tener el formato "*XX* - *XX* XX XX XX XX", -  -  -  - donde cada *X* es un dígito hexadecimal.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                         | Significado                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ correcto</dt> </dl>                                                                                                   | La operación se realizó correctamente.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>                              | El parámetro es **null**.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt> </dl>                           | El parámetro no tiene el formato correcto.<br/>                                                                                                                                                                                                                                                                                                                                      |
| <dl> <dt>Máquina virtual \_ E no se pudo \_ \_ establecer la \_ \_ \_ dirección Mac dinámica</dt> <dt>0xA004070A</dt> </dl> | La dirección Ethernet de una interfaz de red se puede generar dinámicamente, o bien el usuario puede establecerla en una dirección estática. No se puede llamar a este método cuando se establece la dirección para que se genere dinámicamente. La propiedad [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) se usa para cambiar el comportamiento de generación de la dirección Ethernet.<br/> |
| <dl> <dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt> </dl>                      | No se encontró la máquina virtual. Esto puede ocurrir si se quitó el equipo después de crear el objeto [**IVMNetworkAdapter**](ivmnetworkadapter.md) .<br/>                                                                                                                                                                                                                        |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl>                      | Se produjo un error inesperado.<br/>                                                                                                                                                                                                                                                                                                                                                |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMNetworkAdapter se define como e32e4165-22b8-4DC0-8d57-850171ae207a<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMNetworkAdapter**](ivmnetworkadapter.md)
</dt> </dl>

 

