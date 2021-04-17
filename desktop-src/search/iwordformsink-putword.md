---
description: Coloca el formulario de Word original en el objeto IWordFormSink.
ms.assetid: 333A3109-6C0A-42AE-9E10-87F53C7F737C
title: IWordFormSink::P método utWord (Search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordFormSink.PutWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 438cb41e50f264bd373ae2ef8e84598b651b0352
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696279"
---
# <a name="iwordformsinkputword-method"></a>IWordFormSink::P método utWord

Coloca el formulario de Word original en el objeto [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PutWord(
  [in] const WCHAR *pwcInBuf ,
  [in]       ULONG cwc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pwcInBuf* \[ de\]
</dt> <dd>

Puntero a un búfer que contiene la forma alternativa final de una palabra, que siempre es la palabra original.

</dd> <dt>

*CWC* \[ de\]
</dt> <dd>

Número de caracteres de *pwcInBuf*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                          | Descripción                                           |
|--------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | La operación se completó correctamente. <br/> |



 

## <a name="remarks"></a>Observaciones

Se llama a **PutWord** desde el método [**GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) de la implementación de [**IStemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) . Este método controla el formato original de una palabra y se llama último. Todas las formas alternativas anteriores de una palabra se colocan en el objeto [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) mediante una llamada a [**IWordFormSink::P utaltword**](iwordformsink-putphrase.md).

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

 

 
