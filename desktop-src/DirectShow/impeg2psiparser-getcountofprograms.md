---
description: La implementación de este método se proporciona como código de ejemplo con el SDK de DirectShow. No es una API de DirectShow compatible.
ms.assetid: 282dd779-9aca-46e3-a791-cb9ea86f637d
title: 'IMpeg2PsiParser:: GetCountOfPrograms (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetCountOfPrograms
api_type:
- COM
api_location: ''
ms.openlocfilehash: e4f01b2a360465b9670b52547cff1ff4c312a705
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906708"
---
# <a name="impeg2psiparsergetcountofprograms-method"></a>IMpeg2PsiParser:: GetCountOfPrograms (método)

La implementación de este método se proporciona como código de ejemplo con el SDK de DirectShow. No es una API de DirectShow compatible.

El `GetCountOfPrograms` método recupera el número de programas en el flujo de transporte.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCountOfPrograms(
  [out] int *pNumOfPrograms
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pNumOfPrograms* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe el número de programas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor HRESULT. Entre los valores posibles se incluyen, entre otros, los valores que se muestran en la tabla siguiente.



| Código devuelto                                                                          | Descripción         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | Correcto.<br/> |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IMpeg2PsiParser**](impeg2psiparser.md)
</dt> <dt>

[Ejemplo de filtro de analizador de PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 




