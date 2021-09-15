---
description: Coloca una palabra y su posición en el objeto IWordSink.
ms.assetid: 3D645BF6-895E-46E2-92A3-3E301CD228D8
title: Método IWordSink::P utWord (Search.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468326"
---
# <a name="iwordsinkputword-method"></a>IWordSink::P utWord (método)

Coloca una palabra y su posición en el [**objeto IWordSink.**](iwordsink.md)

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

*cwc* \[ En\]
</dt> <dd>

Número de caracteres de *pwcInBuf*.

</dd> <dt>

*pwcInBuf* \[ En\]
</dt> <dd>

Puntero a un búfer que contiene una forma alternativa de una palabra del texto de origen. PutWord no modifica este **parámetro.** Puede pasar el *parámetro pTextSource* desde [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) según corresponda.

</dd> <dt>

*cwcSrcLen* \[ En\]
</dt> <dd>

Número de caracteres del búfer de texto de origen (indicado por el parámetro *pTextSource* a [**IWordBreaker::BreakText)**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)que corresponden a la palabra contenida en *pwcInBuf*.

</dd> <dt>

*cwcSrcPos* \[ En\]
</dt> <dd>

Posición inicial de la palabra en *pwcInBuf* en el búfer de texto de origen (indicado por el parámetro *pTextSource* a [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                              | Descripción                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | La operación se completó correctamente. También indica que no hay más texto disponible para rellenar el búfer.<br/>                                  |
| <dl> <dt>**LANGUAGE \_ PALABRA \_ \_ GRANDE**</dt> </dl> | El valor *de cwc* es mayor que el valor de *ulMaxTokenSize* que se especifica en [**IWordBreaker::Init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init). <br/> |



 

## <a name="remarks"></a>Observaciones

Se recomienda que el **método IWordSink::P utWord** siempre contenga la palabra original tal como se encuentra *en pTextSource*. Las formas alternativas de la palabra se pasan a WordSink mediante [**IWordSink::P utAltWord**](iwordsink-putaltword.md). También se recomienda que las palabras de *pwcInBuf* coincidan lo más estrechamente posible con el texto de origen. Por ejemplo, conservar mayúsculas y acentos siempre que sea posible.

Esta llamada debe realizarse para todas las palabras recuperadas de *pTextSource,* excepto aquellas para las que se realizó la llamada [**IWordSink::P utAltWord.**](iwordsink-putaltword.md) La palabra finaliza con un carácter EOW cuando se guarda en WordSink.

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

 

 
