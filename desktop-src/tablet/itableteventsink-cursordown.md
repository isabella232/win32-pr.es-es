---
description: Se produce cuando la punta del lápiz se pone en contacto con la superficie de la tableta de la digitalización.
ms.assetid: 7f4a441d-00d2-4120-8a8d-d3496cdc7e58
title: 'ITabletEventSink:: CursorDown (método)'
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
ms.openlocfilehash: 1f0ffbe8c300e3c227cd59d8ff391b8990873c56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814430"
---
# <a name="itableteventsinkcursordown-method"></a>ITabletEventSink:: CursorDown (método)

Se produce cuando la punta del lápiz se pone en contacto con la superficie de la tableta de la digitalización.

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

*TCID* \[ de\]
</dt> <dd>

El identificador de la tableta.

</dd> <dt>

*CID* \[ en\]
</dt> <dd>

Identificador del lápiz óptico.

</dd> <dt>

*nSerialNumber* \[ de\]
</dt> <dd>

Número de serie del lápiz óptico.

</dd> <dt>

*cbPkt* \[ de\]
</dt> <dd>

El número de bytes de un paquete de datos del lápiz óptico.

</dd> <dt>

*pbPkt* \[ de\]
</dt> <dd>

Datos del lápiz óptico que indican la ubicación donde el lápiz toca la tableta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                            | Descripción                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>   | Correcto.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz ITabletEventSink**](itableteventsink.md)
</dt> </dl>

 

 




