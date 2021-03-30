---
description: Indica el límite entre frases en una secuencia de frases alternativas que un separador de palabras genera durante el tiempo de índice.
ms.assetid: 3F3B6761-887B-426E-A44F-E636397180C7
title: 'IWordSink:: StartAltPhrase (método) (Search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.StartAltPhrase
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: e4e35c5ed75016292dd420e7a832c6cfb780284a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275253"
---
# <a name="iwordsinkstartaltphrase-method"></a>IWordSink:: StartAltPhrase (método)

Indica el límite entre frases en una secuencia de frases alternativas que un separador de palabras genera durante el tiempo de índice.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT StartAltPhrase();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                           | Descripción                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <dt>**WBREAK \_ E \_ \_ solo consulta**</dt> </dl> | Se llama a [**StartAltPhrase**](iwordsink-startaltphrase.md) durante el tiempo de la consulta.<br/> |



 

## <a name="remarks"></a>Observaciones

Cada frase alternativa comienza con una llamada a **StartAltPhrase** . La frase se coloca en el objeto [**IWordSink**](iwordsink.md) a través de las llamadas subsiguientes al método [**IWordSink::P utword**](iwordsink-putword.md) o [**IWordSink::P utaltword**](iwordsink-putaltword.md) . La frase alternativa final en una secuencia de frases finaliza con una llamada al método [**IWordSink:: EndAltPhrase**](iwordsink-endaltphrase.md) .

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

 

 




