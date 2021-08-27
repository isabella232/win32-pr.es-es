---
title: Función glBindTexture (Gl.h)
description: La función glBindTexture permite la creación de una textura con nombre enlazada a un destino de textura.
ms.assetid: 800f2360-b40e-4911-9a45-6f310aeeefeb
keywords:
- Función glBindTexture OpenGL
topic_type:
- apiref
api_name:
- glBindTexture
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f7f108a0ce4fbc60aba6dc0430227eab15218fe17f80800678fc16b54bbc39f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082225"
---
# <a name="glbindtexture-function"></a>Función glBindTexture

La **función glBindTexture** permite la creación de una textura con nombre enlazada a un destino de textura.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glBindTexture(
   GLenum target,
   GLuint texture
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Destino* 
</dt> <dd>

Destino al que está enlazada la textura. Debe tener el valor GL \_ TEXTURE \_ 1D o GL \_ TEXTURE \_ 2D.

</dd> <dt>

*Textura* 
</dt> <dd>

Nombre de una textura; el nombre de textura no puede estar actualmente en uso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | El destino *del parámetro* no era un valor aceptado.<br/>                                                                                                                                                       |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | La textura *del parámetro* no tenía la misma dimensionalidad que el destino *o* se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glBindTexture** permite crear una textura con nombre. Al llamar **a glBindTexture** con destino establecido en GL TEXTURE 1D o GL TEXTURE  \_ \_ \_ \_  2D, y la textura establecida en el nombre de la nueva textura que ha creado enlaza el nombre de textura al destino de textura adecuado. Cuando una textura está enlazada a un destino, el enlace anterior para ese destino ya no está en vigor.

Los nombres de textura son enteros sin signo con el valor cero reservado para representar la textura predeterminada para cada destino de textura. Los nombres de textura y el contenido de textura correspondiente son locales en el espacio compartido de la lista de visualización del contexto de representación de OpenGL actual; dos contextos de representación comparten nombres de textura solo si también comparten listas para mostrar. Puede generar un conjunto de nuevos nombres de textura mediante [**glGenTextures**](glgentextures.md).

Cuando una textura se enlaza por primera vez, asume la dimensionalidad de su destino de textura; una textura enlazada a GL TEXTURE 1D se convierte en unidimensional y una textura enlazada \_ \_ a GL TEXTURE \_ \_ 2D se convierte en bidimensional. Las operaciones que se realizan en un destino de textura también afectan a una textura enlazada al destino. Cuando se consulta un destino de textura, el valor devuelto es el estado de la textura enlazada a él. Los destinos de textura se convierten en alias para las texturas enlazadas actualmente a ellos.

Al enlazar una textura con **glBindTexture,** el enlace permanece activo hasta que se enlaza una textura diferente al mismo destino o se elimina la textura enlazada con la función [**glDeleteTextures.**](gldeletetextures.md) Una vez que cree una textura con nombre, puede enlazarla a un destino de textura que tenga la misma dimensionalidad con la frecuencia que sea necesario.

Normalmente es mucho más rápido usar **glBindTexture** para enlazar una textura con nombre existente a uno de los destinos de textura que volver a cargar la imagen de textura mediante [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D.**](glteximage2d.md) Para un control adicional del rendimiento de texturing, use [**glPrioritizeTextures**](glprioritizetextures.md).

Puede incluir llamadas a **glBindTexture en** listas para mostrar.

> [!Note]  
> La **función glBindTexture** solo está disponible en OpenGL versión 1.1 o posterior.

 

Las siguientes funciones recuperan información relacionada **con glBindTexture**:

-   [**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ TEXTURE \_ 1D \_ BINDING

**glGet con** el argumento GL \_ TEXTURE \_ 2D \_ BINDING

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

[**glAreTexturesResident**](glaretexturesresident.md)
</dt> <dt>

[**glDeleteTextures**](gldeletetextures.md)
</dt> <dt>

[**glGenTextures**](glgentextures.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glIsTexture**](glistexture.md)
</dt> <dt>

[**glPrioritizeTextures**](glprioritizetextures.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





