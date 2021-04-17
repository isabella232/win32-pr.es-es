---
title: Propiedad DriveByIndex de IMsRdpDriveCollection
description: Recupera la unidad en el índice especificado.
ms.assetid: 28bb2a44-00ac-4892-881d-fdd3fe6adb6b
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad DriveByIndex
- Propiedad DriveByIndex Servicios de Escritorio remoto, interfaz IMsRdpDriveCollection
- Servicios de Escritorio remoto de la interfaz IMsRdpDriveCollection, propiedad DriveByIndex
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.DriveByIndex
- IMsRdpDriveCollection.get_DriveByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2789656b328f9615787ff2cd50a1b69c712a8138
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422475"
---
# <a name="imsrdpdrivecollectiondrivebyindex-property"></a>IMsRdpDriveCollection::D propiedad riveByIndex

Recupera la unidad en el índice especificado.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_DriveByIndex(
  [in]          ULONG index,
  [out, retval] IMsRdpDrive **ppDevice
);
```



## <a name="property-value"></a>Valor de propiedad

Puntero a la interfaz [**IMsRdpDrive**](imsrdpdrive.md) .

## <a name="error-codes"></a>Códigos de error

Si el método se ejecuta correctamente, se devuelve **S \_ OK** . Cualquier otro valor **HRESULT** indica que se produjo un error en la llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IMsRdpDriveCollection se define como 7ff17599-da2c-4677-Ad35-f60c04fe1585<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpDriveCollection**](imsrdpdrivecollection.md)
</dt> </dl>

 

 





