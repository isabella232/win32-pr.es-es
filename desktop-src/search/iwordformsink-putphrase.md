---
description: Coloca una forma alternativa de una palabra en el objeto IWordFormSink.
ms.assetid: 4F6A3E88-A17C-4CA3-849D-FF0DC06D5DC3
title: IWordFormSink::P método utAltWord (Search. h)
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
ms.openlocfilehash: 43539bbf67e23bc37ca92f6a961b945ae581e746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808918"
---
# <a name="iwordformsinkputaltword-method"></a>IWordFormSink::P método utAltWord

Coloca una forma alternativa de una palabra en el objeto [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PutAltWord(
  [in] const WCHAR *pwcInBuf ,
  [in]       ULONG cwc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pwcInBuf* \[ de\]
</dt> <dd>

Un puntero a un búfer que contiene una forma alternativa de una palabra.

</dd> <dt>

*CWC* \[ de\]
</dt> <dd>

Número de caracteres de *pwcInBuf*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                              | Descripción                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                     | La operación se completó correctamente. <br/>                                                                                             |
| <dl> <dt>**Idioma \_ de \_ \_ palabra S grande**</dt> </dl> | El valor de *CWC* es mayor que el valor de *ulMaxTokenSize* que se especifica en [**IStemmer:: init**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-init). <br/> |



 

## <a name="remarks"></a>Observaciones

Se llama a este método desde el método [**GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) de la implementación de [**IStemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) . Todas las formas alternativas para una palabra, a excepción de la última, se colocan en el objeto [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) mediante una llamada a **IWordFormSink::P utaltword**. La forma alternativa final de una palabra, que siempre es el formato original de la palabra, se controla mediante una llamada a [**IWordFormSink::P utword**](iwordformsink-putword.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Search. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink)
</dt> </dl>

 

 
