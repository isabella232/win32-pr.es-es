---
description: La implementación de este método se proporciona como código de ejemplo con el SDK de DirectShow. No es una API de DirectShow compatible.
ms.assetid: 3800a0b1-a581-40ed-81ab-3d5f77f442df
title: 'IMpeg2PsiParser:: GetRecordProgramNumber (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetRecordProgramNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2bedc5922ce90fa2fda612f30571f884e75841d6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677068"
---
# <a name="impeg2psiparsergetrecordprogramnumber-method"></a>IMpeg2PsiParser:: GetRecordProgramNumber (método)

La implementación de este método se proporciona como código de ejemplo con el SDK de DirectShow. No es una API de DirectShow compatible.

El `GetRecordProgramNumber` método recupera el número de programa para un programa especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetRecordProgramNumber(
  [in]  DWORD dwIndex,
  [out] WORD  *pwVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwIndex* \[ de\]
</dt> <dd>

Especifica la entrada de PAT que define el programa, indizada desde cero.

</dd> <dt>

*pwVal* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe el \_ campo de número de programa de la Pat.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT** . Entre los valores posibles se incluyen, entre otros, los valores que se muestran en la tabla siguiente.



| Código devuelto                                                                          | Descripción         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | Correcto.<br/> |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IMpeg2PsiParser**](impeg2psiparser.md)
</dt> <dt>

[Ejemplo de filtro de analizador de PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 




