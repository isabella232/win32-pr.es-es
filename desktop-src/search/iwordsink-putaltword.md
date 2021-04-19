---
description: Coloca una palabra alternativa y su posición en el objeto IWordSink.
ms.assetid: 5C8A9B30-F9B5-42E9-ADAC-A11230F0C2FA
title: IWordSink::P método utAltWord (Search. h)
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
ms.openlocfilehash: 21fd9eb9ac5a1bf0f52d6574595dc495432d7ec9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696276"
---
# <a name="iwordsinkputaltword-method"></a>IWordSink::P método utAltWord

Coloca una palabra alternativa y su posición en el objeto [**IWordSink**](iwordsink.md) .

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

*CWC* \[ de\]
</dt> <dd>

Número de caracteres de *pwcInBuf*.

</dd> <dt>

*pwcInBuf* \[ de\]
</dt> <dd>

Un puntero a un búfer que contiene una forma alternativa de una palabra del texto de origen. **PutAltWord** no modifica este parámetro. Puede pasar el parámetro *pTextSource* de [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) según corresponda.

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
| <dl> <dt>**S \_ correcto**</dt> </dl>                     | La operación se completó correctamente. También indica que no queda más texto para procesarse.<br/>                                            |
| <dl> <dt>**Idioma \_ de \_ \_ palabra S grande**</dt> </dl> | El valor de *CWC* es mayor que el valor de *ulMaxTokenSize* que se especifica en [**IWordBreaker:: init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init). <br/> |



 

## <a name="remarks"></a>Observaciones

**PutAltWord** coloca una forma alternativa de una palabra en el [**IWordSink**](iwordsink.md). La palabra se coloca en la misma posición que la palabra original en el origen del texto (*pTextSource* en [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)). De forma predeterminada, **PutAltWord** finaliza las palabras con un tipo de interrupción **WORDREP \_ break \_ EOW** en el tipo enumerado [**\_ \_ tipo de interrupción WORDREP**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) .

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

 

 
