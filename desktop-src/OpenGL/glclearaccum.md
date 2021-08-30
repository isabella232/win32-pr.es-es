---
title: Función glClearAccum (Gl.h)
description: La función glClearAccum especifica los valores sin borrar para el búfer de acumulación.
ms.assetid: 77d8f340-be47-43f4-96fc-31025a4c8b4e
keywords:
- Función glClearAccum OpenGL
topic_type:
- apiref
api_name:
- glClearAccum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e4e5b02b52ac72e5694b1c5f912dd8dd98fb8dda5b623b28addd20fccbb7dd1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082075"
---
# <a name="glclearaccum-function"></a>Función glClearAccum

La **función glClearAccum** especifica los valores sin borrar para el búfer de acumulación.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glClearAccum(
   GLfloat red,
   GLfloat green,
   GLfloat blue,
   GLfloat alpha
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Rojo* 
</dt> <dd>

Valor rojo que se usa cuando se borra el búfer de acumulación. El valor predeterminado es cero.

</dd> <dt>

*Verde* 
</dt> <dd>

Valor verde que se usa cuando se borra el búfer de acumulación. El valor predeterminado es cero.

</dd> <dt>

*Azul* 
</dt> <dd>

Valor azul que se usa cuando se borra el búfer de acumulación. El valor predeterminado es cero.

</dd> <dt>

*alpha* 
</dt> <dd>

Valor alfa utilizado cuando se borra el búfer de acumulación. El valor predeterminado es cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el código de error siguiente.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glClearAccum** especifica los valores rojo, verde, azul y alfa que [**usa glClear**](glclear.md) para borrar el búfer de acumulación.

Los valores especificados **por glClearAccum** se fijan en el intervalo \[ 1,1. \]

La función siguiente recupera información relacionada con **glClearAccum**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento \_ GL ACCUM CLEAR \_ \_ VALUE

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glClear**](glclear.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





