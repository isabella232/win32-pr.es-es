---
title: Propiedad IVMAccountant NetworkBytesSent (VPCCOMInterfaces. h)
description: Número total de bytes enviados por todos los adaptadores de red virtuales para esta máquina virtual.
ms.assetid: 3b5c3fa2-48c6-46c8-bbb6-5d1a9769308a
keywords:
- Propiedad NetworkBytesSent Virtual PC
- Propiedad NetworkBytesSent Virtual PC, interfaz IVMAccountant
- Interfaz IVMAccountant Virtual PC, propiedad NetworkBytesSent
topic_type:
- apiref
api_name:
- IVMAccountant.NetworkBytesSent
- IVMAccountant.get_NetworkBytesSent
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d25a6c0a9ee784af8bfab196fc9aaef0d1474d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996486"
---
# <a name="ivmaccountantnetworkbytessent-property"></a>IVMAccountant:: NetworkBytesSent (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera el número total de bytes enviados por todos los adaptadores de red virtual para esta máquina virtual.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_NetworkBytesSent(
  [out, retval] VARIANT *bytesSent
);
```



## <a name="property-value"></a>Valor de propiedad

El número total de bytes enviados por todas las tarjetas de interfaz de red virtual para esta máquina virtual. Se devuelve como una **variante** de tipo **VT \_ decimal**.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>       |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **null**.<br/>          |
| <dl> <dt>S \_ FALSO</dt> <dt>1</dt> </dl>                    | La máquina virtual no se está ejecutando.<br/> |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/>   |



## <a name="remarks"></a>Observaciones

Tenga en cuenta que las estadísticas de e/s de red se restablecen a cero cuando una máquina virtual se enciende, se restablece o se restaura desde el estado guardado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMAccountant se define como 6376c067-7f57-4D63-b754-06e2e4f51d73<br/>              |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMAccountant**](ivmaccountant.md)
</dt> </dl>

 

