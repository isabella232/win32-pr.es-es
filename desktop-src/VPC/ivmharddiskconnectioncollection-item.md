---
title: Propiedad del elemento IVMHardDiskConnectionCollection (VPCCOMInterfaces. h)
description: Recupera el objeto de conexión del disco duro correspondiente al índice especificado.
ms.assetid: 24e158fb-b026-4619-9d0d-a59cd782894f
keywords:
- Propiedad del elemento Virtual PC
- Propiedad del elemento Virtual PC, interfaz IVMHardDiskConnectionCollection
- Interfaz IVMHardDiskConnectionCollection Virtual PC, propiedad Item
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection.Item
- IVMHardDiskConnectionCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5558e70cfcf18f67c14e52160737b851fa9ea2c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676551"
---
# <a name="ivmharddiskconnectioncollectionitem-property"></a>IVMHardDiskConnectionCollection:: Item (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera el objeto de conexión del disco duro correspondiente al índice especificado.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Item(
  [in]          long                  index,
  [out, retval] IVMHardDiskConnection **hardDiskConnection
);
```



## <a name="property-value"></a>Valor de propiedad

El objeto [**IVMHardDiskConnection**](ivmharddiskconnection.md) .

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente. <br/>                                                      |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>         | El parámetro *hardDiskConnection* es **null**. <br/>                                    |
| <dl> <dt>DISP \_ . E \_ BADINDEX</dt> <dt>0x8002000B</dt> </dl>  | El índice del elemento solicitado no corresponde a un elemento de esta colección. <br/> |
| <dl> <dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt> </dl> | La configuración es desconocida.<br/>                                                       |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/>                                                   |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                         |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                          |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                               |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                      |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl>      |
| IID<br/>                      | IID \_ IVMHardDiskconnectionCollection se define como b9f2caf4-0aeb-4085-B105-ceddb90dbf62<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMHardDiskConnection**](ivmharddiskconnection.md)
</dt> <dt>

[**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md)
</dt> </dl>

 

