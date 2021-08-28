---
description: Coloca una forma alternativa de una palabra en el objeto IWordFormSink.
ms.assetid: 4F6A3E88-A17C-4CA3-849D-FF0DC06D5DC3
title: IWordFormSink::P utAltWord (Search.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordFormSink.PutAltWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 874428ed435d2336398f6e72c58b70de275565cce2e606f1fdddea54f0684742
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944415"
---
# <a name="iwordformsinkputaltword-method"></a>IWordFormSink::P utAltWord (método)

Coloca una forma alternativa de una palabra en el [**objeto IWordFormSink.**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PutAltWord(
  [in] const WCHAR *pwcInBuf ,
  [in]       ULONG cwc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pwcInBuf* \[ En\]
</dt> <dd>

Puntero a un búfer que contiene una forma alternativa de una palabra.

</dd> <dt>

*cwc* \[ En\]
</dt> <dd>

Número de caracteres de *pwcInBuf*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                              | Descripción                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | La operación se completó correctamente. <br/>                                                                                             |
| <dl> <dt>**LANGUAGE \_ S \_ LARGE \_ WORD**</dt> </dl> | El valor *de cwc* es mayor que el valor de *ulMaxTokenSize* que se especifica en [**IStemmer::Init**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-init). <br/> |



 

## <a name="remarks"></a>Comentarios

Se llama a este método desde [**el método GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) de la [**implementación de IStemmer.**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) Todas las formas alternativas de una palabra, excepto la última, se ponen en el objeto [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) llamando a **IWordFormSink::P utAltWord**. La forma alternativa final de una palabra, que siempre es la forma original de la palabra, se controla mediante una llamada a [**IWordFormSink::P utWord**](iwordformsink-putword.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Search.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink)
</dt> </dl>

 

 
