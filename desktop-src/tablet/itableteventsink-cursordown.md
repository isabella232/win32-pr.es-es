---
description: Se produce cuando la punta del lápiz óptico se pone en contacto con la superficie de la tableta de digitalización.
ms.assetid: 7f4a441d-00d2-4120-8a8d-d3496cdc7e58
title: ITabletEventSink::CursorDown (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorDown
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 242e9ebdf2999c342e6ae7f4711a9f142b38a23e977e7dc9a44b906e0062bc2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820645"
---
# <a name="itableteventsinkcursordown-method"></a>ITabletEventSink::CursorDown (método)

Se produce cuando la punta del lápiz óptico se pone en contacto con la superficie de la tableta de digitalización.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CursorDown(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] ULONG             nSerialNumber,
  [in] ULONG             cbPkt,
  [in] BYTE              *pbPkt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*tcid* \[ En\]
</dt> <dd>

Identificador de la tableta.

</dd> <dt>

*cid* \[ en\]
</dt> <dd>

Identificador del lápiz óptico.

</dd> <dt>

*nSerialNumber* \[ En\]
</dt> <dd>

Número de serie del lápiz óptico.

</dd> <dt>

*cbPkt* \[ En\]
</dt> <dd>

Número de bytes de un paquete de datos de lápiz óptico.

</dd> <dt>

*pbPkt* \[ En\]
</dt> <dd>

Datos del lápiz óptico que indican la ubicación en la que el lápiz tocó la tableta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                            | Descripción                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Correcto.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITabletEventSink (interfaz)**](itableteventsink.md)
</dt> </dl>

 

 




