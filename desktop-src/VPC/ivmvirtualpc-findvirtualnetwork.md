---
title: Método IVMVirtualPC FindVirtualNetwork (VPCCOMInterfaces.h)
description: Recupera un objeto de red virtual que coincide con el nombre solicitado.
ms.assetid: 84526fa4-fe88-4466-866d-c432ed3125aa
keywords:
- FindVirtualNetwork, método Virtual PC
- FindVirtualNetwork method Virtual PC , IVMVirtualPC interface
- IVMVirtualPC interface Virtual PC , Método FindVirtualNetwork
topic_type:
- apiref
api_name:
- IVMVirtualPC.FindVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc8cfb0b8f9b7ee5be7bfb25d7d4cd7ca7b215bcf1824262c576038e75e6ce0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118592140"
---
# <a name="ivmvirtualpcfindvirtualnetwork-method"></a>IVMVirtualPC::FindVirtualNetwork (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera un objeto de red virtual que coincide con el nombre solicitado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FindVirtualNetwork(
  [in]          BSTR              virtualNetworkName,
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*virtualNetworkName* \[ En\]
</dt> <dd>

Nombre de la red virtual que se buscará.

</dd> <dt>

*virtualNetwork* \[ out, retval\]
</dt> <dd>

Puntero a un nuevo [**objeto IVMVirtualNetwork**](ivmvirtualnetwork.md) que representa esta red virtual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                            | Descripción                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                                  | La operación se realizó correctamente.<br/>                                                        |
| <dl> <dt>**S \_ FALSE**</dt> <dt>1</dt> </dl>                                               | No se encontró la red virtual especificada.<br/>                                    |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                                    | El *parámetro virtualNetwork* es **NULL** o no se encuentra la red virtual.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                 | El *parámetro virtualNetworkName* no es válido o es una cadena vacía.<br/>               |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ARCHIVO DE ERROR \_ \_ NO \_ ENCONTRADO)**</dt> <dt>0X80070002</dt> </dl> | No se encontró el archivo de red virtual.<br/>                                         |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                            | Se produjo un error inesperado.<br/>                                                    |
| <dl> <dt>**Máquina virtual \_ E \_ \_ VIRTUALIZACIÓN DE HARDWARE \_ DESHABILITADA**</dt> <dt>0xA0040951</dt> </dl>     | El procesador no admite extensiones de virtualización acelerada de hardware (HAV).<br/> |



 

## <a name="remarks"></a>Observaciones

Los nombres de red virtual no tienen en cuenta las mayúsculas y minúsculas, por ejemplo, "MyNetwork" y "mynetwork" hacen referencia a la misma red virtual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualPC se define como \_ 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

