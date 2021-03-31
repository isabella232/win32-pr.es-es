---
title: modificador/cpp_cmd
description: El \_ modificador cmd de/CPP especifica el preprocesador que el compilador MIDL utiliza para preprocesar los archivos de entrada.
ms.assetid: d6261fdd-155d-4327-b254-d0267f0dec69
keywords:
- /cpp_cmd modificador MIDL
topic_type:
- apiref
api_name:
- /cpp_cmd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ad693f8dbf3ddc7acda6539b89930972ca81a87
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784234"
---
# <a name="cpp_cmd-switch"></a>\_modificador cmd de/CPP

El modificador **\_ cmd de/CPP** especifica el preprocesador que el compilador MIDL utiliza para preprocesar los archivos de entrada.

``` syntax
midl /cpp_cmd "C_preprocessor_binary"
```

## <a name="switch-options"></a>Opciones de conmutador

<dl> <dt>

*\_Binario de preprocesador de C \_* 
</dt> <dd>

Especifica el comando que invoca el preprocesador. Este comando permite a los desarrolladores reemplazar el preprocesador predeterminado. De forma predeterminada, MIDL invoca el compilador de C/C++ de Microsoft desde el entorno de compilación de la máquina de compilación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El *argumento \_ \_ binario del preprocesador de C* para el modificador puede especificar la ruta de acceso completa; el sufijo y las comillas exe son opcionales. Normalmente, los desarrolladores usan el modificador para elegir una versión concreta del preprocesador de C/C++ de Microsoft o equivalente en el entorno de compilación. En este caso, no es necesario usar el modificador [**\_ OPT/CPP**](-cpp-opt.md) con **/CPP \_ cmd**.

Cuando se usa un preprocesador que no es de Microsoft, en especial cuando el preprocesador especificado no dirige su salida a stdout, se debe especificar el modificador de compilador de C que redirige la salida a stdout como parte del modificador [**/CPP \_ OPC**](-cpp-opt.md) del compilador MIDL. Vea [requisitos del preprocesador de C para MIDL](c-preprocessor-requirements-for-midl.md) para obtener más información

El preprocesador se invoca mediante una cadena de comando que se forma a partir de la información proporcionada al compilador de MIDL mediante los modificadores **/CPP \_ cmd**, [**/CPP \_ OPC**](-cpp-opt.md), [**/d**](-d.md), [**/i**](-i.md)y [**/u**](-u.md) . En la tabla siguiente se resume cómo se construye la cadena de comandos para cada combinación de modificadores **/CPP \_ cmd** y **/CPP \_ OPC** .

Cuando no se especifica el modificador **/CPP \_ cmd** , el compilador MIDL invoca el compilador de Microsoft C/C++. MIDL usa un binario Cl.exe que se encuentra en el entorno de compilación.

Cuando el modificador [**\_ OPT/CPP**](-cpp-opt.md) no está presente, el compilador MIDL concatena la cadena especificada por el modificador **\_ cmd/CPP** con la información especificada por las opciones de MIDL [**/i**](-i.md), [**/d**](-d.md) y [**/u**](-u.md) . La cadena/E también se concatena con la cadena de invocación del compilador de C para indicar que el compilador de C/C++ solo debe realizar el preprocesamiento. El modificador [**/nologo**](-nologo.md) se agrega para suprimir el banner del compilador de C/C++. El compilador MIDL usa la cadena concatenada para invocar el preprocesador de C para IDL de nivel superior, así como los archivos IDL importados, y también para los archivos ACF correspondientes presentes.

Cuando el modificador [**\_ OPT/CPP**](-cpp-opt.md) está presente, que debe ser un caso poco frecuente en las plataformas actuales de 32 bits y 64 bits, el compilador MIDL concatena la cadena especificada por el modificador **\_ cmd/CPP** con la cadena especificada por el modificador **/CPP \_ OPC** . El compilador MIDL utiliza la cadena concatenada para invocar el binario del preprocesador indicado en lugar del preprocesador predeterminado. Cuando el modificador **\_ OPT/CPP** está presente, ni las opciones del compilador de MIDL especificadas por los modificadores [**/I**](-i.md), [**/d**](-d.md)y [**/u**](-u.md) ni el modificador del compilador de C/e se concatenan con la cadena. Debe proporcionar la opción/E, o equivalente, como parte de la cadena.



| \_¿está presente/CPP cmd? | \_¿/CPP está disponible? | Descripción                                                                                                                                                                                                       |
|--------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| No (valor predeterminado)       | No (valor predeterminado)       | Invoca el compilador de Microsoft C/C++ predeterminado con la configuración obtenida de los modificadores de MIDL [**/i**](-i.md), [**/d**](-d.md) y [**/u**](-u.md) . Agrega los modificadores de preprocesador/E y [**/nologo**](-nologo.md). |
| Sí                | No                 | Invoca el binario del preprocesador indicado con los mismos modificadores anteriores.                                                                                                                                        |
| No                 | Sí                | Invoca el compilador de C de Microsoft con las opciones especificadas. No usa las opciones de MIDL [**/i**](-i.md), [**/d**](-d.md), [**/u**](-u.md) . Debe proporcionar/E como parte de [**/CPP \_ OPT**](-cpp-opt.md).             |
| Sí                | Sí                | Invoca el binario del preprocesador especificado solo con las opciones especificadas. Debe usar comillas.                                                                                                                       |



 

## <a name="examples"></a>Ejemplos

**MIDL/CPP \_ cmd d: \\ NT \\ Tools \\ ia64 \\cl.exe/DFLAG = true/IC: \\ Inc FILENAME. idl**

**MIDL/CPP \_ cmd "mycpp"/DFLAG = true/IC: \\ Inc FILENAME. idl**

**MIDL/CPP \_ OPT "/E/DFLAG = true/IC: \\ Inc" nombreDeArchivo. idl**

**MIDL/CPP \_ cmd "CL"/CPP \_ OPT "/e/DFLAG = true/IC: \\ Inc" nombreDeArchivo. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[**/savePP**](-savepp.md)
</dt> <dt>

[**/CPP \_ OPC**](-cpp-opt.md)
</dt> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**/no \_ CPP**](-no-cpp-nocpp.md)
</dt> <dt>

[Requisitos del preprocesador de C para MIDL](c-preprocessor-requirements-for-midl.md)
</dt> </dl>

 

 




