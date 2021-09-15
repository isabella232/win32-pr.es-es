---
description: Recupera información de análisis del objeto InkDivider.
ms.assetid: 1b073da4-80f4-48f4-8ff6-b21793c173a8
title: Función CallDivide
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571437"
---
# <a name="calldivide-function"></a>Función CallDivide

Recupera información de análisis del [**objeto InkDivider.**](inkdivider-class.md)

Esta función no está pensada para que la utilice el código de la aplicación.

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

*hDivider* \[ En\]
</dt> <dd>

Identificador del objeto [**InkDivider.**](inkdivider-class.md)

</dd> <dt>

*pWordSize* \[ En\]
</dt> <dd>

Tamaño de la palabra devuelta por el [**objeto InkDivider.**](inkdivider-class.md)

</dd> <dt>

*pLineSize* \[ En\]
</dt> <dd>

Tamaño de la línea devuelta por el [**objeto InkDivider.**](inkdivider-class.md)

</dd> <dt>

*pParagraphSize* \[ En\]
</dt> <dd>

Tamaño del párrafo devuelto por el [**objeto InkDivider.**](inkdivider-class.md)

</dd> <dt>

*pDrawingSize* \[ En\]
</dt> <dd>

Tamaño del dibujo devuelto por el [**objeto InkDivider.**](inkdivider-class.md)

</dd> <dt>

*pWordCount* \[ out\]
</dt> <dd>

Número de palabras devueltas por el análisis de entrada de lápiz.

</dd> <dt>

*pLineCount* \[ out\]
</dt> <dd>

Número de líneas devueltas por el análisis de entrada de lápiz.

</dd> <dt>

*pParagraphCount* \[ out\]
</dt> <dd>

Número de párrafos devueltos por el análisis de entrada de lápiz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función puede devolver uno de estos valores.



| Código devuelto                                                                                  | Descripción                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Función suceeded.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Uno o varios parámetros no son válidos.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                         |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Biblioteca<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




