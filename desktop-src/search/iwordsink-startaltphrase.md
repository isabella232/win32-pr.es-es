---
description: Indica el límite entre las frases de una secuencia de frases alternativas que un separador de palabras genera durante el tiempo de índice.
ms.assetid: 3F3B6761-887B-426E-A44F-E636397180C7
title: Método IWordSink::StartAltPhrase (Search.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468325"
---
# <a name="iwordsinkstartaltphrase-method"></a>IWordSink::StartAltPhrase (método)

Indica el límite entre las frases de una secuencia de frases alternativas que un separador de palabras genera durante el tiempo de índice.

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
| <dl> <dt>**SOLO CONSULTA \_ WBREAK E \_ \_**</dt> </dl> | [**Se llama a StartAltPhrase**](iwordsink-startaltphrase.md) durante el tiempo de consulta.<br/> |



 

## <a name="remarks"></a>Observaciones

Cada frase alternativa comienza con una **llamada a StartAltPhrase.** La frase se coloca en el objeto [**IWordSink**](iwordsink.md) mediante llamadas posteriores al método [**IWordSink::P utWord**](iwordsink-putword.md) [**o IWordSink::P utAltWord.**](iwordsink-putaltword.md) La última frase alternativa de una secuencia de frases finaliza con una llamada al [**método IWordSink::EndAltPhrase.**](iwordsink-endaltphrase.md)

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

 

 




