---
description: Coloca una palabra alternativa y su posición en el objeto IWordSink.
ms.assetid: 5C8A9B30-F9B5-42E9-ADAC-A11230F0C2FA
title: Método IWordSink::P utAltWord (Search.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutAltWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 8282a1b28fa901727930f57e459c6e751b19a74669967c8d3d3d81910278943d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117862593"
---
# <a name="iwordsinkputaltword-method"></a>IWordSink::P utAltWord (método)

Coloca una palabra alternativa y su posición en el [**objeto IWordSink.**](iwordsink.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PutAltWord(
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

Puntero a un búfer que contiene una forma alternativa de una palabra del texto de origen. **PutAltWord** no modifica este parámetro. Puede pasar el *parámetro pTextSource* desde [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) según corresponda.

</dd> <dt>

*cwcSrcLen* \[ En\]
</dt> <dd>

Número de caracteres del búfer de texto de origen (indicado por el parámetro *pTextSource* a [**IWordBreaker::BreakText)**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)que corresponden a la palabra contenida en *pwcInBuf*.

</dd> <dt>

*cwcSrcPos* \[ En\]
</dt> <dd>

Posición inicial de la palabra en *pwcInBuf* en el búfer de texto de origen (indicado por el *parámetro pTextSource* a [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                              | Descripción                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | La operación se completó correctamente. También indica que no queda más texto para procesar.<br/>                                            |
| <dl> <dt>**LANGUAGE \_ S \_ LARGE \_ WORD**</dt> </dl> | El valor *de cwc* es mayor que el valor de *ulMaxTokenSize* que se especifica en [**IWordBreaker::Init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init). <br/> |



 

## <a name="remarks"></a>Comentarios

**PutAltWord coloca** una forma alternativa de palabra en [**IWordSink.**](iwordsink.md) La palabra se coloca en la misma posición que la palabra original en el origen de texto (*pTextSource* en [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)). De forma predeterminada, **PutAltWord** finaliza las palabras con un tipo de interrupción **\_ \_ EOW BREAK de WORDREP** del tipo enumerado [**\_ WORDREP BREAK \_ TYPE.**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85))

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

 

 
