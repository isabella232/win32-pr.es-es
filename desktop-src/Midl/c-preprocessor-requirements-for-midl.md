---
title: Requisitos del preprocesador de C para MIDL
description: Esta página se aplica solo a los desarrolladores que tienen razones específicas para reemplazar el preprocesador de C/C++ de Microsoft como el preprocesador usado por MIDL, o a los desarrolladores que deben especificar modificadores de preprocesador personalizados.
ms.assetid: 1dd5eef4-5ea4-4958-8f53-9a95c0ccbf3e
keywords:
- 'MIDL del compilador MIDL, C: preprocesador, requisitos'
- 'C: preprocesador MIDL, requisitos'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b49c4e0c086a52eda2705d72cf2a2ff22c759290
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994455"
---
# <a name="c-preprocessor-requirements-for-midl"></a>Requisitos del preprocesador de C para MIDL

Esta página se aplica solo a los desarrolladores que tienen razones específicas para reemplazar el preprocesador de C/C++ de Microsoft como el preprocesador usado por MIDL, o a los desarrolladores que deben especificar modificadores de preprocesador personalizados. Los modificadores MIDL [**/CPP \_ cmd**](-cpp-cmd.md), [**/CPP \_ OPC**](-cpp-opt.md)y [**/no \_ CPP**](-no-cpp-nocpp.md) se utilizan para invalidar el comportamiento predeterminado del compilador. Normalmente, no hay ningún motivo para reemplazar el preprocesador de Microsoft C/C++ ni para especificar modificadores de preprocesador personalizados.

El compilador MIDL usa un preprocesador de C durante el procesamiento inicial del archivo IDL. El entorno de compilación usado al compilar los archivos IDL está asociado a un preprocesador de C/C++ predeterminado. Si se va a usar un preprocesador diferente, el modificador del compilador MIDL [**/CPP \_ cmd**](-cpp-cmd.md) habilita una invalidación del nombre del preprocesador de C/C++ predeterminado:

``` syntax
midl /cpp_cmd preprocessor_name filename
```

<dl> <dt>

<span id="preprocessor_name"></span><span id="PREPROCESSOR_NAME"></span>*nombre del preprocesador \_*
</dt> <dd>

Especifica el nombre del preprocesador que va a usar MIDL. Se puede especificar con una ruta de acceso al archivo binario. La extensión. exe es opcional.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*extensión*
</dt> <dd>

Especifica el nombre del archivo IDL.

</dd> </dl>

-   El compilador MIDL espera que cualquier preprocesador respete las convenciones siguientes:
-   El archivo de entrada se especifica como el último argumento de la línea de comandos.
-   El preprocesador debe redirigir la salida al dispositivo de salida estándar, stdout.
-   En el flujo de salida del preprocesador, las directivas de **\# línea** están presentes para permitir mejores mensajes de diagnóstico.
-   Las directivas de línea son las únicas directivas de preprocesador en el flujo de salida.

MIDL supone que el preprocesador generado ha quitado todas las directivas de preprocesador del flujo de entrada del compilador, con la excepción de las repeticiones de la Directiva de línea necesarias para identificar la ubicación de origen en los mensajes del compilador. Cuando se indica un preprocesador diferente del preprocesador de C/C++ de Microsoft, o cuando se especifican opciones del preprocesador con el modificador [**/CPP \_ OPC**](-cpp-opt.md) , se requiere una opción de preprocesador adecuada que coloque las directivas de línea en el flujo de entrada del compilador. Por ejemplo, para el preprocesador de C/C++ de Microsoft, debe usarse la opción **/e** :

``` syntax
midl /cpp_cmd cl.exe /cpp_opt "/E" file.idl
```

La Directiva de **\# línea** es aceptada por MIDL en una de las siguientes formas:

``` syntax
#line digit-sequence "filename" new-line
 
# digit-sequence "filename" new-line
```

Para obtener una descripción completa de la directiva line y otras directivas de preprocesador, vea la documentación del compilador de C que se está usando.

MIDL solo acepta la Directiva de preprocesador de línea. Por lo tanto, si se utiliza el modificador [**/no \_ CPP**](-no-cpp-nocpp.md) , el archivo de entrada no debe tener otras directivas de preprocesador, o el archivo de entrada se debe haber procesado antes de invocar MIDL.

Para obtener más información, vea [trabajar con las \# definiciones de los archivos IDL](dealing-with-defines-in-idl-files-2.md).

 

 




