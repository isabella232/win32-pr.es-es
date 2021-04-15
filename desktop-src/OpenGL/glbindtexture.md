---
title: función glBindTexture (GL. h)
description: La función glBindTexture permite la creación de una textura con nombre que está enlazada a un destino de textura.
ms.assetid: 800f2360-b40e-4911-9a45-6f310aeeefeb
keywords:
- glBindTexture (función) OpenGL
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
ms.openlocfilehash: e76009a486e3903ad8230891af8b7593ab8aaa47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422398"
---
# <a name="glbindtexture-function"></a>glBindTexture función)

La función **glBindTexture** permite la creación de una textura con nombre que está enlazada a un destino de textura.

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

Destino al que está enlazada la textura. Debe tener el valor de GL \_ Texture \_ 1D o la textura de GL \_ \_ 2D.

</dd> <dt>

*degrada* 
</dt> <dd>

Nombre de una textura; el nombre de la textura no puede estar actualmente en uso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | El *destino* del parámetro no era un valor aceptado.<br/>                                                                                                                                                       |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | La *textura* del parámetro no tenía la misma dimensionalidad que el *destino* o se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glBindTexture** permite crear una textura con nombre. La llamada a **glBindTexture** con el *destino* establecido en GL \_ Texture \_ 1D o la textura GL \_ \_ 2D y la *textura* establecida en el nombre de la nueva textura que ha creado enlaza el nombre de textura al destino de textura adecuado. Cuando una textura se enlaza a un destino, el enlace anterior para ese destino deja de estar en vigor.

Los nombres de textura son enteros sin signo con el valor cero reservado para representar la textura predeterminada para cada destino de textura. Los nombres de textura y el contenido de textura correspondiente son locales para el espacio de lista de presentación compartido del contexto de representación de OpenGL actual. dos contextos de representación comparten nombres de textura solo si también comparten listas de visualización. Puede generar un conjunto de nuevos nombres de textura mediante [**glGenTextures**](glgentextures.md).

Cuando una textura se enlaza por primera vez, se asume la dimensionalidad de su destino de textura. una textura enlazada a una textura de GL \_ \_ 1D se convierte en unidimensional y una textura enlazada a la textura de GL \_ \_ 2D se convierte en bidimensional. Las operaciones que se realizan en un destino de textura también afectan a una textura enlazada al destino. Cuando se consulta un destino de textura, el valor devuelto es el estado de la textura enlazada a él. Los destinos de texturas se convierten en alias para las texturas actualmente enlazadas a ellos.

Al enlazar una textura con **glBindTexture**, el enlace permanece activo hasta que se enlaza una textura diferente al mismo destino o se elimina la textura enlazada con la función [**glDeleteTextures**](gldeletetextures.md) . Una vez que cree una textura con nombre, puede enlazarla a un destino de textura que tenga la misma dimensionalidad que la frecuencia que necesite.

Normalmente, es mucho más rápido usar **glBindTexture** para enlazar una textura con nombre existente a uno de los destinos de textura que para volver a cargar la imagen de textura mediante [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md). Para obtener más control sobre el rendimiento de la texturización, use [**glPrioritizeTextures**](glprioritizetextures.md).

Puede incluir llamadas a **glBindTexture** en las listas de visualización.

> [!Note]  
> La función **glBindTexture** solo está disponible en la versión 1,1 o posterior de OpenGL.

 

Las siguientes funciones recuperan información relacionada con **glBindTexture**:

-   [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con enlace de la \_ textura \_ 1D de \_ argumento

**glGet** con el argumento \_ de \_ bidimensional textura 2D \_ enlace

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

 

 





