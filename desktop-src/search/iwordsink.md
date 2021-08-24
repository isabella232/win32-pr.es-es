---
description: Controla las palabras identificadas por los saltos de palabras durante el tiempo de índice y el tiempo de consulta.
ms.assetid: 220FCAE5-D22D-45ED-9689-E78C0D8E0BB3
title: Interfaz IWordSink (Search.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 109a852f37f3118cd1012c7385a4f9071fdd2f8867f57036e7607c20fd2dadbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822315"
---
# <a name="iwordsink-interface"></a>Interfaz IWordSink

Controla las palabras identificadas por los saltos de palabras durante el tiempo de índice y el tiempo de consulta.

## <a name="members"></a>Miembros

La **interfaz IWordSink** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWordSink** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IWordSink** tiene estos métodos.



| Método                                             | Descripción                                                                                                                             |
|:---------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**EndAltPhrase**](iwordsink-endaltphrase.md)     | Indica el final de la frase final en una secuencia de frases alternativas que un separador de palabras genera durante el tiempo de índice.<br/>  |
| [**PutAltWord**](iwordsink-putaltword.md)         | Coloca una palabra alternativa y su posición en el **objeto IWordSink.**<br/>                                                       |
| [**PutBreak**](iwordsink-putbreak.md)             | Coloca un salto después de la palabra anterior.<br/>                                                                                       |
| [**PutWord**](iwordsink-putword.md)               | Coloca una palabra y su posición en el **objeto IWordSink.**<br/>                                                                    |
| [**StartAltPhrase**](iwordsink-startaltphrase.md) | Indica el límite entre las frases de una secuencia de frases alternativas que un separador de palabras genera durante el tiempo de índice.<br/> |



 

## <a name="remarks"></a>Comentarios

Windows Search crea e inicializa instancias del **objeto IWordSink.** El **objeto IWordSink** recibe el parámetro *fQuery* durante la inicialización y usa este parámetro para determinar el contexto de separación de palabras en el que se usa el objeto.

[**Las implementaciones de IWordBreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) reciben un puntero al **objeto IWordSink** en el [**método IWordBreaker::BreakText.**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Search.h</dt> </dl> |



 

 
