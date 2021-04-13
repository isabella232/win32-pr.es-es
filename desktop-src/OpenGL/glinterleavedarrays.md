---
title: función glInterleavedArrays (GL. h)
description: La función glInterleavedArrays especifica y habilita simultáneamente varias matrices intercaladas en una matriz agregada más grande.
ms.assetid: f1133949-d755-43e3-bf29-8e4c7fb17980
keywords:
- glInterleavedArrays (función) OpenGL
topic_type:
- apiref
api_name:
- glInterleavedArrays
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41403210e78d1a65dd700561243846d6e45bad67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422043"
---
# <a name="glinterleavedarrays-function"></a>glInterleavedArrays función)

La función **glInterleavedArrays** especifica y habilita simultáneamente varias matrices intercaladas en una matriz agregada más grande.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glInterleavedArrays(
         GLenum  format,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*format* 
</dt> <dd>

Tipo de matriz que se va a habilitar. El parámetro puede suponer uno de los siguientes valores simbólicos: GL \_ V2F, GL \_ V3F, GL \_ C4UB \_ V2F, GL \_ C4UB \_ V3F, GL \_ C3F \_ V3F, GL \_ N3F \_ V3F, GL \_ C4F \_ N3F V3F \_ , GL \_ T2F \_ V3F, GL \_ T4F \_ V4F, GL \_ T2F C4UB V3F \_ \_ , GL \_ T2F C3F V3F, GL \_ \_ \_ T2F \_ N3F \_ V3F, GL \_ T2F \_ C4F \_ N3F \_ V3F o \_ GL \_ T4F \_ \_ C4F N3F V4F.

</dd> <dt>

*STRI* 
</dt> <dd>

Desplazamiento en bytes entre cada elemento de la matriz agregado.

</dd> <dt>

*puntero* 
</dt> <dd>

Puntero al primer elemento de una matriz agregada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | el *formato* no era un valor aceptado.<br/>                                                                                        |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | *STRIDE* era un valor negativo.<br/>                                                                                             |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

Con la función **glInterleavedArrays** , puede especificar y habilitar simultáneamente varias matrices de color intercalado, normales, de textura y de vértices cuyos elementos formen parte de un elemento de matriz agregado mayor. En algunas arquitecturas de memoria, es más eficaz que especificar las matrices por separado.

Si el parámetro *STRIDE* es cero, los elementos de la matriz agregada se almacenan consecutivamente; de lo contrario, se producen bytes *STRIDE* entre los elementos de matriz agregados.

El parámetro *Format* sirve como una clave que describe cómo extraer matrices individuales de la matriz agregada:

-   Si *Format* contiene un T, las coordenadas de textura se extraen de la matriz intercalada.
-   Si C está presente, se extraen los valores de color.
-   Si N está presente, se extraen las coordenadas normales.
-   Las coordenadas del vértice siempre se extraen.
-   Los dígitos 2, 3 y 4 denotan el número de valores que se extraen.
-   F indica que los valores se extraen como valores de punto flotante.
-   Si 4UB sigue a la C, los colores también se pueden extraer como 4 bytes sin signo. Si un color se extrae como 4 bytes sin signo, el elemento de matriz de vértices que sigue se encuentra en la primera dirección alineada de punto flotante posible.

Si llama a **glInterleavedArrays** mientras compila una lista de visualización, no se compilará en la lista, pero se ejecutará inmediatamente.

No se pueden incluir llamadas a **glInterleavedArrays** en **glDisableClientState** entre llamadas a [**glBegin**](glbegin.md) y la llamada correspondiente a **glEnd**.

> [!Note]  
> La función **glInterleavedArrays** solo está disponible en la versión 1,1 o posterior de OpenGL.

 

La función **glInterleavedArrays** se implementa en el lado cliente sin ningún protocolo. Dado que los parámetros de la matriz de vértices son de cliente, no se guardan ni restauran en [**glPushAttrib**](glpushattrib.md) y **glPopAttrib**. En su lugar, use [**glPushClientAttrib**](glpushclientattrib.md) y **glPopClientAttrib** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**glArrayElement**](glarrayelement.md)
</dt> <dt>

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glDrawElements**](gldrawelements.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glPushClientAttrib**](glpushclientattrib.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





