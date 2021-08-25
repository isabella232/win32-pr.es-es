---
title: Propiedad IVMSerialPortCollection Item (VPCCOMInterfaces.h)
description: Recupera el objeto de puerto serie que corresponde al índice especificado.
ms.assetid: 24ce1404-d7aa-4125-b1f9-9c54418ea205
keywords:
- Propiedad de elemento Virtual PC
- Propiedad de elemento Virtual PC , interfaz IVMSerialPortCollection
- IVMSerialPortCollection interface Virtual PC , Propiedad Item
topic_type:
- apiref
api_name:
- IVMSerialPortCollection.Item
- IVMSerialPortCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48ebe4e8775abdb9bec3206cd4fd908caad0a35d503c12c528123a005e726f5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973805"
---
# <a name="ivmserialportcollectionitem-property"></a>IVMSerialPortCollection::Item, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera el objeto de puerto serie que corresponde al índice especificado.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Item(
  [in]          long          index,
  [out, retval] IVMSerialPort **serialPort
);
```



## <a name="property-value"></a>Valor de propiedad

Objeto [**IVMSerialPort.**](ivmserialport.md)

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente. <br/>                                                      |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>         | El *parámetro serialPort* es NULL. <br/>                                                |
| <dl> <dt>DISP \_ E \_ BADINDEX</dt> <dt>0x8002000B</dt> </dl>  | El índice del elemento solicitado no corresponde a un elemento de esta colección. <br/> |
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
| IID<br/>                      | IID IVMSerialPortCollection se define como \_ dd3c6175-1f04-4341-9f85-104074880289<br/>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMSerialPort**](ivmserialport.md)
</dt> <dt>

[**IVMSerialPortCollection**](ivmserialportcollection.md)
</dt> </dl>

 

