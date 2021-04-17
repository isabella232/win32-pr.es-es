---
description: La implementación de este método se proporciona como código de ejemplo con el SDK de DirectShow. No es una API de DirectShow compatible.
ms.assetid: 19ef96a8-3d5b-4da1-8cff-d6a271ad4915
title: 'IMpeg2PsiParser:: GetCountOfElementaryStreams (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetCountOfElementaryStreams
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6593b699592c913940b14c2c26aea42057acfa40
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677071"
---
# <a name="impeg2psiparsergetcountofelementarystreams-method"></a>IMpeg2PsiParser:: GetCountOfElementaryStreams (método)

La implementación de este método se proporciona como código de ejemplo con el SDK de DirectShow. No es una API de DirectShow compatible.

El `GetCountOfElementaryStreams` método recupera el número de flujos elementales en un programa especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCountOfElementaryStreams(
  [in]  WORD wProgramNumber,
  [out] WORD *pwVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wProgramNumber* \[ de\]
</dt> <dd>

Especifica el \_ campo de número de programa para el programa, como se indica en el valor de Pat.

</dd> <dt>

*pwVal* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe el número de flujos elementales del programa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT** . Entre los valores posibles se incluyen, entre otros, los valores que se muestran en la tabla siguiente.



| Código devuelto                                                                          | Descripción         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | Correcto.<br/> |



 

## <a name="remarks"></a>Observaciones

Use el método **GetRecordProgramNumber** para obtener el número de programa.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IMpeg2PsiParser**](impeg2psiparser.md)
</dt> <dt>

[**IMpeg2PsiParser::GetRecordProgramNumber**](impeg2psiparser-getrecordprogramnumber.md)
</dt> <dt>

[Ejemplo de filtro de analizador de PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 




