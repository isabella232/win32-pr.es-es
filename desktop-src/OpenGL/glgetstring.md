---
title: función glGetString (GL. h)
description: La función glGetString devuelve una cadena que describe la conexión de OpenGL actual.
ms.assetid: 768e6ec2-3f00-44e6-b3cb-de0f06d6a73d
keywords:
- glGetString (función) OpenGL
topic_type:
- apiref
api_name:
- glGetString
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e263e35802af752fa262c898d036fccaa37aff87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997003"
---
# <a name="glgetstring-function"></a>glGetString función)

La función **glGetString** devuelve una cadena que describe la conexión de OpenGL actual.

## <a name="syntax"></a>Sintaxis


```C++
const GLubyte* WINAPI glGetString(
   GLenum name
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*name* 
</dt> <dd>

Una de las constantes simbólicas siguientes.



| Value                                                                                                                                                         | Significado                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_VENDOR"></span><span id="gl_vendor"></span><dl> <dt>**proveedor de contabilidad general \_**</dt> </dl>             | Devuelve la empresa responsable de esta implementación de OpenGL. Este nombre no cambia de Release a Release.<br/>                                                  |
| <span id="GL_RENDERER"></span><span id="gl_renderer"></span><dl> <dt>**Representador de GL \_**</dt> </dl>       | Devuelve el nombre del representador. Este nombre suele ser específico de una configuración determinada de una plataforma de hardware. No cambia de Release a Release.<br/> |
| <span id="GL_VERSION"></span><span id="gl_version"></span><dl> <dt>**versión de contabilidad \_**</dt> </dl>          | Devuelve una versión o un número de versión.<br/>                                                                                                                                |
| <span id="GL_EXTENSIONS"></span><span id="gl_extensions"></span><dl> <dt>**extensiones de GL \_**</dt> </dl> | Devuelve una lista separada por espacios de las extensiones admitidas a OpenGL.<br/>                                                                                                   |



 

</dd> </dl>

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | *el nombre* no era un valor aceptado.<br/>                                                                                          |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glGetString** devuelve un puntero a una cadena estática que describe algún aspecto de la conexión de OpenGL actual.

Dado que OpenGL no incluye consultas para las características de rendimiento de una implementación, se espera que algunas aplicaciones se escriban para reconocer plataformas conocidas y modifiquen el uso de OpenGL en función de las características de rendimiento conocidas de estas plataformas. Las cadenas de \_ representador de contabilidad y de libro de contabilidad de forma \_ exclusiva especifican una plataforma y no cambiarán de Release a Release. Los algoritmos de reconocimiento de plataforma deben usarlos como tales.

El formato y el contenido de la cadena que devuelve **glGetString** dependen de la implementación, excepto en que:

-   Los nombres de extensión no incluirán caracteres de espacio y estarán separados por caracteres de espacio en la \_ cadena de extensiones GL.
-   La cadena de versión de GL \_ comienza con un número de versión. El número de versión usa una de estas formas:

    *\_ número principal*. *\_ número secundario*

    *\_ número principal*. *\_ número secundario*. *\_ número de versión*

-   La información específica del proveedor puede seguir el número de versión. Su formato depende de la implementación, pero un espacio siempre separa el número de versión y la información específica del proveedor.
-   Todas las cadenas terminan en NULL.

Si se genera un error, **glGetString** devuelve cero.

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





