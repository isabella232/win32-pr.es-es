---
title: Función glInterleavedArrays (Gl.h)
description: La función glInterleavedArrays especifica y habilita simultáneamente varias matrices intercaladas en una matriz de agregado mayor.
ms.assetid: f1133949-d755-43e3-bf29-8e4c7fb17980
keywords:
- Función glInterleavedArrays OpenGL
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
ms.openlocfilehash: ce3b37186614fa431585c1e5a932edab946afd6d881ba1cf8eb5c5690220f603
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938566"
---
# <a name="glinterleavedarrays-function"></a>Función glInterleavedArrays

La **función glInterleavedArrays** especifica y habilita simultáneamente varias matrices intercaladas en una matriz de agregado mayor.

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

Tipo de matriz que se habilitará. El parámetro puede asumir uno de los siguientes valores simbólicos: GL \_ V2F, GL \_ V3F, GL \_ C4UB \_ V2F, GL \_ C4UB \_ V3F, GL \_ \_ C3F V3F, GL \_ N3F \_ V3F, GL \_ C4F \_ N3F \_ V3F, GL \_ \_ T2F \_ V3F, GL T4F \_ V4F, GL \_ T2F \_ C4UB \_ V3F, GL \_ T2F \_ \_ C3F V3F, GL \_ T2F \_ N3F \_ V3F, GL \_ T2F \_ C4F \_ \_ N3F V3F o GL \_ T4F \_ C4F \_ N3F \_ V4F.

</dd> <dt>

*Paso* 
</dt> <dd>

Desplazamiento en bytes entre cada elemento de la matriz de agregados.

</dd> <dt>

*Puntero* 
</dt> <dd>

Puntero al primer elemento de una matriz de agregados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ NO \_ VÁLIDA DE GL**</dt> </dl>      | *format* no era un valor aceptado.<br/>                                                                                        |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *stride* era un valor negativo.<br/>                                                                                             |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

Con **la función glInterleavedArrays,** puede especificar y habilitar simultáneamente varias matrices de colores, normales, texturas y vértices intercaladas cuyos elementos forman parte de un elemento de matriz agregado mayor. Para algunas arquitecturas de memoria, esto es más eficaz que especificar las matrices por separado.

Si el *parámetro stride* es cero, los elementos de la matriz de agregados se almacenan de forma consecutiva; de *lo contrario, se producen* bytes de paso entre elementos de matriz agregados.

El *parámetro format* actúa como clave que describe cómo extraer matrices individuales de la matriz de agregados:

-   Si *format* contiene una T, las coordenadas de textura se extraen de la matriz intercalada.
-   Si C está presente, se extraen los valores de color.
-   Si N está presente, se extraen coordenadas normales.
-   Las coordenadas de vértice siempre se extraen.
-   Los dígitos 2, 3 y 4 indican cuántos valores se extraen.
-   F indica que los valores se extraen como valores de punto flotante.
-   Si 4UB sigue a C, los colores también se pueden extraer como 4 bytes sin signo. Si un color se extrae como 4 bytes sin signo, el elemento de matriz de vértices siguiente se encuentra en la primera dirección alineada de punto flotante posible.

Si llama a **glInterleavedArrays** al compilar una lista de visualización, no se compila en la lista, pero se ejecuta inmediatamente.

No se pueden incluir llamadas **a glInterleavedArrays** en **glDisableClientState** entre las llamadas [**a glBegin**](glbegin.md) y la llamada correspondiente **a glEnd**.

> [!Note]  
> La **función glInterleavedArrays** solo está disponible en OpenGL versión 1.1 o posterior.

 

La **función glInterleavedArrays** se implementa en el lado cliente sin protocolo. Dado que los parámetros de la matriz de vértices son de estado del lado cliente, [**glPushAttrib**](glpushattrib.md) y **glPopAttrib** no los guardan ni restauran. Use [**glPushClientAttrib**](glpushclientattrib.md) y **glPopClientAttrib en** su lugar.

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

 

 





