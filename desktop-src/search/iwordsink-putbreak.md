---
description: Coloca un salto después de la palabra anterior.
ms.assetid: C8622067-D8CE-4099-8B9F-941720F4706B
title: IWordSink::P método utBreak (Search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutBreak
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: c6407f1307b4860960c5202af13de736c7921139
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360185"
---
# <a name="iwordsinkputbreak-method"></a>IWordSink::P método utBreak

Coloca un salto después de la palabra anterior.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PutBreak(
  [in] WORDREP_BREAK_TYPE breakType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*breakType* \[ de\]
</dt> <dd>

Un valor del [**\_ \_ tipo de interrupción WORDREP**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) que indica el tipo de interrupción que el WordSink inserta después de la palabra anterior. Cada salto ocupa una posición única en el índice. Por lo tanto, la inserción de saltos entre palabras cambia la distancia relativa entre palabras.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                          | Descripción                                          |
|--------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | La operación se completó correctamente.<br/> |



 

## <a name="remarks"></a>Observaciones

Los métodos [**IWordSinkPutWord**](iwordsink-putword.md) y [**IWordSink::P utaltword**](iwordsink-putaltword.md) insertan automáticamente un salto de final de palabra (EOW, indicado por el \_ elemento WORDREP break \_ EOW del tipo de [**\_ interrupción \_ WORDREP**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) tipo enumerado) después de cada palabra. Llame al método **PutBreak** para insertar un tipo de interrupción que no sea el final de la palabra. Este método no cambia el búfer de texto de origen (*pSourceText*) ni incrementa el recuento de caracteres (*CWC*). Sin embargo, incrementa la posición actual en el índice y afecta a los resultados de la consulta.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Search. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWordSink**](iwordsink.md)
</dt> </dl>

 

 
