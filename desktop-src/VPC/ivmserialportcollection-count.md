---
title: Propiedad IVMSerialPortCollection Count (VPCCOMInterfaces.h)
description: Recupera el número de puertos serie de esta colección.
ms.assetid: 94ff6c9d-17bc-4aa5-a486-d4428c829d02
keywords:
- Count, propiedad Virtual PC
- Count, interfaz IVMSerialPortCollection de la propiedad Virtual PC
- IVMSerialPortCollection interface Virtual PC , Propiedad Count
topic_type:
- apiref
api_name:
- IVMSerialPortCollection.Count
- IVMSerialPortCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b8c7390b4637cf8e39fe83fcbb9844913a41d20fd2ed9515695ec068b33af6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118593158"
---
# <a name="ivmserialportcollectioncount-property"></a>IVMSerialPortCollection::Count, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera el número de puertos serie de esta colección.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a>Valor de propiedad

Número de puertos serie.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                            | Significado                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>               | La operación se realizó correctamente.<br/> |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl> | El parámetro es **NULL.**<br/>    |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMSerialPortCollection se define como \_ dd3c6175-1f04-4341-9f85-104074880289<br/>    |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IVMSerialPortCollection**](ivmserialportcollection.md)
</dt> </dl>

 

