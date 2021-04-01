---
title: Propiedad DriveLetterIndex de IMsRdpDriveV2
description: Contiene el índice de la letra de la unidad.
ms.assetid: 9091d1c4-b97e-4e4c-9563-5a0b881ec250
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad DriveLetterIndex
- Propiedad DriveLetterIndex Servicios de Escritorio remoto, interfaz IMsRdpDriveV2
- Servicios de Escritorio remoto de la interfaz IMsRdpDriveV2, propiedad DriveLetterIndex
topic_type:
- apiref
api_name:
- IMsRdpDriveV2.DriveLetterIndex
- IMsRdpDriveV2.get_DriveLetterIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39284a94950935e2d273483db871a9b08f7daf36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997146"
---
# <a name="imsrdpdrivev2driveletterindex-property"></a>IMsRdpDriveV2::D propiedad riveLetterIndex

Contiene el índice de la letra de la unidad.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_DriveLetterIndex(
  [out, retval] ULONG *pDriveLetterIndex
);
```



## <a name="property-value"></a>Valor de propiedad

Índice de la letra de la unidad. 0 = "A", 1 = "B", etc.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 con SP1<br/>                                                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                      |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpDriveV2**](imsrdpdrivev2.md)
</dt> </dl>

 

 





