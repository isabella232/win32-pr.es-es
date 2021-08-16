---
title: Función glGetString (Gl.h)
description: La función glGetString devuelve una cadena que describe la conexión OpenGL actual.
ms.assetid: 768e6ec2-3f00-44e6-b3cb-de0f06d6a73d
keywords:
- Función glGetString OpenGL
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
ms.openlocfilehash: 9cbc5a1add320d711c92020074b3de810d134e88953a8413c0efd2e6b6fdd954
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118359914"
---
# <a name="glgetstring-function"></a>Función glGetString

La **función glGetString** devuelve una cadena que describe la conexión OpenGL actual.

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

Una de las siguientes constantes simbólicas.



| Valor                                                                                                                                                         | Significado                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_VENDOR"></span><span id="gl_vendor"></span><dl> <dt>**\_PROVEEDOR DE GL**</dt> </dl>             | Devuelve la empresa responsable de esta implementación de OpenGL. Este nombre no cambia de versión a versión.<br/>                                                  |
| <span id="GL_RENDERER"></span><span id="gl_renderer"></span><dl> <dt>**REPRESENTADOR \_ DE GL**</dt> </dl>       | Devuelve el nombre del representador. Este nombre suele ser específico de una configuración determinada de una plataforma de hardware. No cambia de versión a versión.<br/> |
| <span id="GL_VERSION"></span><span id="gl_version"></span><dl> <dt>**VERSIÓN \_ DE GL**</dt> </dl>          | Devuelve una versión o un número de versión.<br/>                                                                                                                                |
| <span id="GL_EXTENSIONS"></span><span id="gl_extensions"></span><dl> <dt>**EXTENSIONES \_ GL**</dt> </dl> | Devuelve una lista separada por espacios de extensiones admitidas a OpenGL.<br/>                                                                                                   |



 

</dd> </dl>

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ NO \_ VÁLIDA DE GL**</dt> </dl>      | *name* no era un valor aceptado.<br/>                                                                                          |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glGetString** devuelve un puntero a una cadena estática que describe algún aspecto de la conexión OpenGL actual.

Dado que OpenGL no incluye consultas para las características de rendimiento de una implementación, se espera que algunas aplicaciones se escriban para reconocer plataformas conocidas y modifiquen su uso de OpenGL en función de las características de rendimiento conocidas de estas plataformas. Las cadenas GL VENDOR y GL RENDERER juntos especifican de forma única una plataforma \_ \_ y no cambiarán de versión a versión. Deben usarse como tales mediante algoritmos de reconocimiento de plataforma.

El formato y el contenido de la cadena que **glGetString devuelve** dependen de la implementación, salvo que:

-   Los nombres de extensión no incluirán caracteres de espacio y estarán separados por caracteres de espacio en la cadena \_ GL EXTENSIONS.
-   La cadena \_ GL VERSION comienza con un número de versión. El número de versión usa uno de estos formularios:

    *número \_ principal*. *número \_ menor*

    *número \_ principal*. *número \_ menor*. *número de \_ versión*

-   La información específica del proveedor puede seguir el número de versión. Su formato depende de la implementación, pero un espacio siempre separa el número de versión y la información específica del proveedor.
-   Todas las cadenas finalizan en NULL.

Si se genera un error, **glGetString** devuelve cero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





