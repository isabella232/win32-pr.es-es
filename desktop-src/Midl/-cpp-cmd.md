---
title: Modificador /cpp_cmd
description: El modificador /cpp cmd especifica el preprocesador que el compilador \_ MIDL usa para preprocesar los archivos de entrada.
ms.assetid: d6261fdd-155d-4327-b254-d0267f0dec69
keywords:
- /cpp_cmd switch MIDL
topic_type:
- apiref
api_name:
- /cpp_cmd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ad693f8dbf3ddc7acda6539b89930972ca81a87
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159767"
---
# <a name="cpp_cmd-switch"></a>Modificador /cpp \_ cmd

El **modificador /cpp \_ cmd** especifica el preprocesador que el compilador MIDL usa para preprocesar los archivos de entrada.

``` syntax
midl /cpp_cmd "C_preprocessor_binary"
```

## <a name="switch-options"></a>Opciones de cambio

<dl> <dt>

*Binario \_ de preprocesador de C \_* 
</dt> <dd>

Especifica el comando que invoca el preprocesador. Este comando permite a los desarrolladores invalidar el preprocesador predeterminado. De forma predeterminada, MIDL invoca el compilador de Microsoft C/C++ desde el entorno de compilación de la máquina de compilación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El *argumento binario del \_ preprocesador \_* de C para el modificador puede especificar la ruta de acceso completa; el sufijo exe y las comillas son opcionales. Normalmente, los desarrolladores usan el modificador para elegir una versión determinada del preprocesador de Microsoft C/C++ o equivalente en el entorno de compilación. En este caso, no es necesario usar el modificador [**/cpp \_ opt**](-cpp-opt.md) con **/cpp \_ cmd**.

Cuando se usa un preprocesador que no es de Microsoft, especialmente cuando el preprocesador especificado no dirige su salida a stdout, se debe especificar el modificador del compilador de C que redirige la salida a stdout como parte del modificador [**/cpp \_ opt**](-cpp-opt.md) del compilador MIDL. Consulte [C-Preprocessor Requirements for MIDL (Requisitos del preprocesador de C para MIDL)](c-preprocessor-requirements-for-midl.md) para obtener más información.

El preprocesador se invoca mediante una cadena de comandos formada a partir de la información proporcionada al compilador MIDL por los modificadores **/cpp \_ cmd**, [**/cpp \_ opt**](-cpp-opt.md), [**/D**](-d.md), [**/I**](-i.md)y [**/U.**](-u.md) En la tabla siguiente se resume cómo se construye la cadena de comando para cada combinación de **modificadores /cpp \_ cmd** **y /cpp \_ opt.**

Cuando no se especifica el modificador **/cpp \_ cmd,** el compilador MIDL invoca al compilador de Microsoft C/C++. MIDL usa un Cl.exe binario que se encuentra en el entorno de compilación.

Cuando el modificador [**/cpp \_ opt**](-cpp-opt.md) no está presente, el compilador MIDL concatena la cadena especificada por el modificador **/cpp \_ cmd** con la información especificada por las opciones MIDL [**/I**](-i.md), [**/D**](-d.md) y [**/U.**](-u.md) La cadena /E también se concatena con la cadena de invocación del compilador de C para indicar que el compilador de C/C++ solo debe realizar el preprocesamiento. El [**modificador /nologo**](-nologo.md) se agrega para suprimir el banner del compilador de C/C++. El compilador MIDL usa la cadena concatenada para invocar el preprocesador de C para IDL de nivel superior, así como archivos IDL importados, y también para los archivos ACF correspondientes presentes.

Cuando el modificador [**/cpp \_ opt**](-cpp-opt.md) está presente, que debería ser un caso poco frecuente para las plataformas actuales de 32 y 64 bits, el compilador MIDL concatena la cadena especificada por el modificador **/cpp \_ cmd** con la cadena especificada por el modificador **/cpp \_ opt.** El compilador MIDL usa la cadena concatenada para invocar el binario de preprocesador indicado en lugar del preprocesador predeterminado. Cuando el modificador **/cpp \_ opt** está presente, ni las opciones del compilador MIDL especificadas por los modificadores [**/I**](-i.md), [**/D**](-d.md)y [**/U**](-u.md) ni el modificador del compilador de C /E se concatenan con la cadena. Debe proporcionar la opción /E, o equivalente, como parte de la cadena.



| /cpp \_ cmd present? | /cpp \_ opt present? | Descripción                                                                                                                                                                                                       |
|--------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| No (valor predeterminado)       | No (valor predeterminado)       | Invoca el compilador predeterminado de Microsoft C/C++ con la configuración obtenida de los modificadores MIDL [**/I,**](-i.md) [**/D**](-d.md) [**y /U.**](-u.md) Agrega los modificadores de preprocesador /E y [**/nologo.**](-nologo.md) |
| Sí                | No                 | Invoca el binario de preprocesador indicado con los mismos modificadores anteriores.                                                                                                                                        |
| No                 | Sí                | Invoca al compilador de Microsoft C con las opciones especificadas. No usa las opciones MIDL [**/I**](-i.md), [**/D,**](-d.md) [**/U.**](-u.md) Debe proporcionar /E como parte de [**/cpp \_ opt**](-cpp-opt.md).             |
| Sí                | Sí                | Invoca el binario de preprocesador especificado solo con las opciones especificadas. Debe usar comillas.                                                                                                                       |



 

## <a name="examples"></a>Ejemplos

**midl /cpp \_ cmd d: \\ nt tools \\ \\ ia64 \\cl.exe /DFLAG=TRUE /Ic: \\ inc filename.idl**

**midl /cpp \_ cmd "mycpp" /DFLAG=TRUE /Ic: \\ inc filename.idl**

**midl /cpp \_ opt "/E /DFLAG=TRUE /Ic: \\ inc" filename.idl**

**midl /cpp \_ cmd "cl" /cpp \_ opt "/E /DFLAG=TRUE /Ic: \\ inc" filename.idl**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**/savePP**](-savepp.md)
</dt> <dt>

[**/cpp \_ opt**](-cpp-opt.md)
</dt> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/no \_ cpp**](-no-cpp-nocpp.md)
</dt> <dt>

[Requisitos de preprocesador de C para MIDL](c-preprocessor-requirements-for-midl.md)
</dt> </dl>

 

 




