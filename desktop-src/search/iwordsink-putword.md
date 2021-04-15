---
description: Coloca una palabra y su posición en el objeto IWordSink.
ms.assetid: 3D645BF6-895E-46E2-92A3-3E301CD228D8
title: IWordSink::P método utWord (Search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 5f622e09c2b82bc8de986dafcc83247617caec75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696275"
---
# <a name="iwordsinkputword-method"></a>IWordSink::P método utWord

Coloca una palabra y su posición en el objeto [**IWordSink**](iwordsink.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PutWord(
  [in]       ULONG cwc,
  [in] const WCHAR *pwcInBuf,
  [in]       ULONG cwcSrcLen,
  [in]       ULONG cwcSrcPos
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CWC* \[ de\]
</dt> <dd>

Número de caracteres de *pwcInBuf*.

</dd> <dt>

*pwcInBuf* \[ de\]
</dt> <dd>

Un puntero a un búfer que contiene una forma alternativa de una palabra del texto de origen. **PutWord** no modifica este parámetro. Puede pasar el parámetro *pTextSource* de [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) según corresponda.

</dd> <dt>

*cwcSrcLen* \[ de\]
</dt> <dd>

Número de caracteres del búfer de texto de origen (indicado por el parámetro *pTextSource* en [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) que corresponden a la palabra contenida en *pwcInBuf*.

</dd> <dt>

*cwcSrcPos* \[ de\]
</dt> <dd>

Posición inicial de la palabra en *pwcInBuf* en el búfer de texto de origen (indicado por el parámetro *pTextSource* a [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                              | Descripción                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                     | La operación se completó correctamente. También indica que no hay más texto disponible para rellenar el búfer.<br/>                                  |
| <dl> <dt>**Idioma \_ de \_ \_ palabra S grande**</dt> </dl> | El valor de *CWC* es mayor que el valor de *ulMaxTokenSize* que se especifica en [**IWordBreaker:: init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init). <br/> |



 

## <a name="remarks"></a>Observaciones

Se recomienda que el método **IWordSink::P utword** contenga siempre la palabra original como se encuentra en *pTextSource*. Las formas alternativas de la palabra se pasan a WordSink mediante [**IWordSink::P utaltword**](iwordsink-putaltword.md). También se recomienda que las palabras de *pwcInBuf* coincidan con el texto de origen lo más cerca posible. Por ejemplo, conserve las mayúsculas y los acentos siempre que sea posible.

Esta llamada se debe realizar para cada palabra recuperada de *pTextSource* , excepto aquellas para las que se realizó la llamada a [**utaltword de IWordSink::P**](iwordsink-putaltword.md) . La palabra se termina con un carácter EOW cuando se guarda en WordSink.

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

 

 
