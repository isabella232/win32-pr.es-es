---
title: Propiedad IMsRdpDriveV2 DriveLetterIndex
description: Contiene el índice de la letra de la unidad.
ms.assetid: 9091d1c4-b97e-4e4c-9563-5a0b881ec250
ms.tgt_platform: multiple
keywords:
- Propiedad DriveLetterIndex Servicios de Escritorio remoto
- Propiedad DriveLetterIndex Servicios de Escritorio remoto interfaz , IMsRdpDriveV2
- Interfaz IMsRdpDriveV2 Servicios de Escritorio remoto , propiedad DriveLetterIndex
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
ms.openlocfilehash: 10dc107eba84b0b0559ce711add4596040cf23423e0723855e2c0c9ef0de652a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119399665"
---
# <a name="imsrdpdrivev2driveletterindex-property"></a>IMsRdpDriveV2::D riveLetterIndex

Contiene el índice de la letra de la unidad.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_DriveLetterIndex(
  [out, retval] ULONG *pDriveLetterIndex
);
```



## <a name="property-value"></a>Valor de propiedad

Índice de la letra de la unidad. 0 = "A", 1 = "B", y así sucesivamente.

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

 

 





