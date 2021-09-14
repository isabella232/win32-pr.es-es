---
description: 'Método IMpeg2PsiParser::GetPatVersionNumber: la implementación de este método se proporciona como código de ejemplo con DirectShow SDK. No es una API de DirectShow compatible.'
ms.assetid: 2f5ad9bf-3d70-491a-ab45-15cd922a02d4
title: IMpeg2PsiParser::GetPatVersionNumber (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetPatVersionNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 978da4c7076bcf8ffe91bc2b9a4b2077d9d3d48a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126886777"
---
# <a name="impeg2psiparsergetpatversionnumber-method"></a>IMpeg2PsiParser::GetPatVersionNumber (método)

La implementación de este método se proporciona como código de ejemplo con DirectShow SDK. No es una API de DirectShow compatible.

El `GetPatVersionNumber` método recupera el campo de número de versión del \_ PAT. Una secuencia de transporte contiene como máximo un PAT. El número de versión se incrementa cada vez que cambia la información de la tabla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetPatVersionNumber(
  [out] BYTE *pPatVersion
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pPatVersion* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el campo de \_ número de versión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT.** Los valores posibles incluyen, entre otros, los valores que se muestran en la tabla siguiente.



| Código devuelto                                                                          | Descripción         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Correcto.<br/> |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IMpeg2PsiParser (interfaz)**](impeg2psiparser.md)
</dt> <dt>

[Ejemplo de filtro del analizador de PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 




