---
description: Mueve un contexto de tableta al principio o al final de la cola de entrada.
ms.assetid: ef4521b5-776b-46dc-864a-625bc221054a
title: 'ITabletContextP:: superposición (método)'
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
ms.openlocfilehash: b009bc08dddb15bc7aa5b12c8846ea66c4a52e56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716718"
---
# <a name="itabletcontextpoverlap-method"></a>ITabletContextP:: superposición (método)

Mueve un contexto de tableta al principio o al final de la cola de entrada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Overlap(
  [in]  BOOL  bTop,
  [out] DWORD *pdwtcid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bTop* \[ de\]
</dt> <dd>

Indica si el contexto de Tablet PC debe moverse a la parte superior o inferior de la cola de entrada.

</dd> <dt>

*pdwtcid* \[ enuncia\]
</dt> <dd>

Identificador de contexto de Tablet PC.

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

[**Interfaz ITabletContextP**](itabletcontextp.md)
</dt> </dl>

 

 




