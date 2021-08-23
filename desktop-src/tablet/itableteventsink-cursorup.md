---
description: Se produce cuando el usuario ha elevado el lápiz óptico de la superficie del digitalizador de tabletas.
ms.assetid: 34dc7e6b-101a-4edd-8c3c-9aafb85cf58b
title: ITabletEventSink::CursorUp (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorUp
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 586f18750e832bad653a3df92d14efb41b39547ee532913ac52c986a9b5e137c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712135"
---
# <a name="itableteventsinkcursorup-method"></a>ITabletEventSink::CursorUp (método)

Se produce cuando el usuario ha elevado el lápiz óptico de la superficie del digitalizador de tabletas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CursorUp(
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

Los datos del lápiz óptico que indican la ubicación en la que se ha lifted el lápiz óptico de la tableta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

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

 

 




