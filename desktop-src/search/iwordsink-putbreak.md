---
description: Coloca un salto después de la palabra anterior.
ms.assetid: C8622067-D8CE-4099-8B9F-941720F4706B
title: Método IWordSink::P utBreak (Search.h)
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
ms.openlocfilehash: d254e6e03ef9fe8af1ec65e519e4c873aea5b8a8887172329d3997424920c4e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117680442"
---
# <a name="iwordsinkputbreak-method"></a>IWordSink::P utBreak (método)

Coloca un salto después de la palabra anterior.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PutBreak(
  [in] WORDREP_BREAK_TYPE breakType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*breakType* \[ En\]
</dt> <dd>

Valor de [**WORDREP \_ BREAK \_ TYPE**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) que indica el tipo de interrupción que WordSink inserta después de la palabra anterior. Cada interrupción ocupa una posición única en el índice. Por lo tanto, la inserción de saltos entre palabras cambia la distancia relativa entre las palabras.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                          | Descripción                                          |
|--------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | La operación se completó correctamente.<br/> |



 

## <a name="remarks"></a>Comentarios

Los métodos [**IWordSinkPutWord**](iwordsink-putword.md) e [**IWordSink::P utAltWord**](iwordsink-putaltword.md) insertan automáticamente un salto de fin de palabra (EOW, indicado por el elemento EOW WORDREP BREAK del tipo enumerado \_ \_ [**WORDREP \_ BREAK \_ TYPE)**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) después de cada palabra. Llame al **método PutBreak** para insertar un tipo de interrupción distinto del final de la palabra. Este método no cambia el búfer de texto de origen (*pSourceText*) ni incrementa el recuento de caracteres (*cwc*). Sin embargo, incrementa la posición actual en el índice y afecta a los resultados de la consulta.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Search.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWordSink**](iwordsink.md)
</dt> </dl>

 

 
