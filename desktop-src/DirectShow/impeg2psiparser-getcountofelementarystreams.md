---
description: 'Método IMpeg2PsiParser::GetCountOfElementaryStreams: la implementación de este método se proporciona como código de ejemplo con el SDK DirectShow. No es una API de DirectShow compatible.'
ms.assetid: 19ef96a8-3d5b-4da1-8cff-d6a271ad4915
title: IMpeg2PsiParser::GetCountOfElementaryStreams (método)
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
ms.openlocfilehash: fc81c0a66751751a73a3895fd31fe8651aee8caf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126886785"
---
# <a name="impeg2psiparsergetcountofelementarystreams-method"></a>IMpeg2PsiParser::GetCountOfElementaryStreams (método)

La implementación de este método se proporciona como código de ejemplo con DirectShow SDK. No es una API de DirectShow compatible.

El `GetCountOfElementaryStreams` método recupera el número de secuencias elementales en un programa especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCountOfElementaryStreams(
  [in]  WORD wProgramNumber,
  [out] WORD *pwVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wProgramNumber* \[ En\]
</dt> <dd>

Especifica el campo de \_ número de programa para el programa, como se indica en el PAT.

</dd> <dt>

*pwVal* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el número de secuencias elementales del programa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT.** Los valores posibles incluyen, entre otros, los valores que se muestran en la tabla siguiente.



| Código devuelto                                                                          | Descripción         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Correcto.<br/> |



 

## <a name="remarks"></a>Observaciones

Use el **método GetRecordProgramNumber** para obtener el número de programa.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IMpeg2PsiParser (interfaz)**](impeg2psiparser.md)
</dt> <dt>

[**IMpeg2PsiParser::GetRecordProgramNumber**](impeg2psiparser-getrecordprogramnumber.md)
</dt> <dt>

[Ejemplo de filtro del analizador de PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 




