---
description: Mueve un contexto de tableta al frente o al final de la cola de entrada.
ms.assetid: ef4521b5-776b-46dc-864a-625bc221054a
title: ITabletContextP::Overlap (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.Overlap
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: ec8b462f2d06e1613c32b795af1793776cafddd6a3531ac6a0b5385f3d3e5128
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712245"
---
# <a name="itabletcontextpoverlap-method"></a>ITabletContextP::Overlap (método)

Mueve un contexto de tableta al frente o al final de la cola de entrada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Overlap(
  [in]  BOOL  bTop,
  [out] DWORD *pdwtcid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bTop* \[ En\]
</dt> <dd>

Indica si el contexto de la tableta debe moverse a la parte superior o inferior de la cola de entrada.

</dd> <dt>

*pdwtcid* \[ out\]
</dt> <dd>

Identificador de contexto de tableta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                            | Descripción                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Correcto.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITabletContextP (interfaz)**](itabletcontextp.md)
</dt> </dl>

 

 




