---
description: Indica el final de la frase final en una secuencia de frases alternativas que un separador de palabras genera durante el tiempo de índice.
ms.assetid: 50E4E208-A290-42B7-9152-9472C01B20D5
title: 'IWordSink:: EndAltPhrase (método) (Search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.EndAltPhrase
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 4056357de5e3e479124e8f9a91d9b3d906300709
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275254"
---
# <a name="iwordsinkendaltphrase-method"></a>IWordSink:: EndAltPhrase (método)

Indica el final de la frase final en una secuencia de frases alternativas que un separador de palabras genera durante el tiempo de índice.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EndAltPhrase();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                           | Descripción                                                                            |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**WBREAK \_ E \_ \_ solo consulta**</dt> </dl> | Se llama a [**EndAltPhrase**](iwordsink-endaltphrase.md) durante el tiempo de la consulta.<br/> |



 

## <a name="remarks"></a>Observaciones

Las implementaciones de [**IWordBreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) llaman a **IWordSink:: EndAltPhrase** desde el método [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) para terminar una secuencia de frases alternativas. Se llama al método [**IWordSink:: StartAltPhrase**](iwordsink-startaltphrase.md) para indicar el final de una frase y el principio de otra en una secuencia de frases. Solo la última frase de una secuencia termina con una llamada a **EndAltPhrase**.

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

 

 
