---
description: Recupera información de análisis del objeto InkDivider.
ms.assetid: 1b073da4-80f4-48f4-8ff6-b21793c173a8
title: CallDivide función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivide
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 0084811ee471bee8fe67653dace49fa83642a7fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539454"
---
# <a name="calldivide-function"></a>CallDivide función)

Recupera información de análisis del objeto [**InkDivider**](inkdivider-class.md) .

Esta función no está pensada para ser utilizada por el código de la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI CallDivide(
  _In_  INT_PTR hDivider,
  _In_  int     *pWordSize,
  _In_  int     *pLineSize,
  _In_  int     *pParagraphSize,
  _In_  int     *pDrawingSize,
  _Out_ int     *pWordCount,
  _Out_ int     *pLineCount,
  _Out_ int     *pParagraphCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDivider* \[ de\]
</dt> <dd>

Identificador del objeto [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*pWordSize* \[ de\]
</dt> <dd>

Tamaño de la palabra devuelta por el objeto [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*pLineSize* \[ de\]
</dt> <dd>

Tamaño de la línea devuelta por el objeto [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*pParagraphSize* \[ de\]
</dt> <dd>

Tamaño del párrafo devuelto por el objeto [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*pDrawingSize* \[ de\]
</dt> <dd>

Tamaño del dibujo devuelto por el objeto [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*pWordCount* \[ enuncia\]
</dt> <dd>

Número de palabras que devuelve el análisis de tinta.

</dd> <dt>

*pLineCount* \[ enuncia\]
</dt> <dd>

Número de líneas devueltas por el análisis de tinta.

</dd> <dt>

*pParagraphCount* \[ enuncia\]
</dt> <dd>

El número de párrafos devueltos por el análisis de tinta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función puede devolver uno de estos valores.



| Código devuelto                                                                                  | Descripción                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | La función correcta.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Uno o más parámetros no son válidos.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                         |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Biblioteca<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




