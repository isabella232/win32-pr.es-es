---
title: Propiedad Item de IVMParallelPortCollection (VPCCOMInterfaces.h)
description: Recupera el objeto de puerto paralelo que corresponde al índice especificado.
ms.assetid: f67a4224-ca96-4d68-9f0f-4977ffff859e
keywords:
- Propiedad de elemento Virtual PC
- Propiedad item Virtual PC , IVMParallelPortCollection (interfaz)
- IVMParallelPortCollection interface Virtual PC , Propiedad Item
topic_type:
- apiref
api_name:
- IVMParallelPortCollection.Item
- IVMParallelPortCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a28aec3fbe9585185f61cc7941d5de8033b73019354ca480f72fe4b3b7be793
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007005"
---
# <a name="ivmparallelportcollectionitem-property"></a>IVMParallelPortCollection::Item, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera el objeto de puerto paralelo que corresponde al índice especificado.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Item(
  [in]          long            index,
  [out, retval] IVMParallelPort **vmParallelPort
);
```



## <a name="property-value"></a>Valor de propiedad

Objeto [**IVMParallelPort.**](ivmparallelport.md)

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente. <br/>                                                      |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>         | El *parámetro vmParallelPort* es **NULL.** <br/>                                        |
| <dl> <dt>DISP \_ E \_ BADINDEX</dt> <dt>0x8002000B</dt> </dl>  | El índice del elemento solicitado no se corresponde con un elemento de esta colección. <br/> |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl> | La configuración es desconocida.<br/>                                                       |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/>                                                   |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMParallelPortCollection se define como 27c3e036-198f-430c-8735-6e652f7203fd<br/>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMParallelPort**](ivmparallelport.md)
</dt> <dt>

[**IVMParallelPortCollection**](ivmparallelportcollection.md)
</dt> </dl>

 

