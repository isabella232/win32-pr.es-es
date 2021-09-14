---
description: 'Método IMpeg2PsiParser::GetPmtVersionNumber: la implementación de este método se proporciona como código de ejemplo con el SDK DirectShow. No se admite DirectShow API.'
ms.assetid: 50113d6b-4e10-4dc9-aaef-f67c6918a2de
title: IMpeg2PsiParser::GetPmtVersionNumber (Método)
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
ms.openlocfilehash: 6f4fd8d0eba88ba1df54a1cc058bc0a2951b9a19
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126886780"
---
# <a name="impeg2psiparsergetpmtversionnumber-method"></a>IMpeg2PsiParser::GetPmtVersionNumber (Método)

La implementación de este método se proporciona como código de ejemplo con DirectShow SDK. No se admite DirectShow API.

El `GetPmtVersionNumber` método recupera el campo de número de versión de un \_ PMT especificado. El número de versión se incrementa cada vez que cambia la definición del programa.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetPmtVersionNumber(
  [in]  WORD wProgramNumber,
  [out] BYTE *pPmtVersion
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wProgramNumber* \[ En\]
</dt> <dd>

Especifica el campo de \_ número de programa del programa, como se indica en el PAT.

</dd> <dt>

*pPmtVersion* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el campo de \_ número de versión.

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

 

 




