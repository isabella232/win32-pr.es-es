---
description: 'Método IMpeg2PsiParser::GetCountOfPrograms: la implementación de este método se proporciona como código de ejemplo con el SDK DirectShow. No se admite DirectShow API.'
ms.assetid: 282dd779-9aca-46e3-a791-cb9ea86f637d
title: IMpeg2PsiParser::GetCountOfPrograms (método)
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
ms.openlocfilehash: d6bfe698a45ea1cfe0a4bac6e65b839292bc1996
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126886772"
---
# <a name="impeg2psiparsergetcountofprograms-method"></a>IMpeg2PsiParser::GetCountOfPrograms (método)

La implementación de este método se proporciona como código de ejemplo con DirectShow SDK. No se admite DirectShow API.

El `GetCountOfPrograms` método recupera el número de programas de la secuencia de transporte.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCountOfPrograms(
  [out] int *pNumOfPrograms
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pNumOfPrograms* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el número de programas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor HRESULT. Los valores posibles incluyen, entre otros, los valores que se muestran en la tabla siguiente.



| Código devuelto                                                                          | Descripción         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Correcto.<br/> |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IMpeg2PsiParser (interfaz)**](impeg2psiparser.md)
</dt> <dt>

[Ejemplo de filtro del analizador de PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 




