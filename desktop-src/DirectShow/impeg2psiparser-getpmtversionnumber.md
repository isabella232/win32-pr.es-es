---
description: La implementación de este método se proporciona como código de ejemplo con el SDK de DirectShow. No es una API de DirectShow compatible.
ms.assetid: 50113d6b-4e10-4dc9-aaef-f67c6918a2de
title: 'IMpeg2PsiParser:: GetPmtVersionNumber (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetPmtVersionNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3af4b20067af52216181848f4cc63ac5a7784ba9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677069"
---
# <a name="impeg2psiparsergetpmtversionnumber-method"></a>IMpeg2PsiParser:: GetPmtVersionNumber (método)

La implementación de este método se proporciona como código de ejemplo con el SDK de DirectShow. No es una API de DirectShow compatible.

El `GetPmtVersionNumber` método recupera el \_ campo de número de versión de un valor de PMT especificado. El número de versión se incrementa siempre que cambia la definición del programa.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetPmtVersionNumber(
  [in]  WORD wProgramNumber,
  [out] BYTE *pPmtVersion
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wProgramNumber* \[ de\]
</dt> <dd>

Especifica el \_ campo de número de programa del programa, tal como se indica en el valor de Pat.

</dd> <dt>

*pPmtVersion* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe el campo de número de versión \_ .

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

 

 




