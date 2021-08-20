---
title: Requisitos de preprocesador de C para MIDL
description: Esta página solo se aplica a los desarrolladores que tienen motivos específicos para reemplazar el preprocesador de Microsoft C/C++ como el preprocesador usado por MIDL, o a los desarrolladores que deben especificar modificadores de preprocesador personalizados.
ms.assetid: 1dd5eef4-5ea4-4958-8f53-9a95c0ccbf3e
keywords:
- MIDL del compilador MIDL, preprocesador C, requisitos
- MIDL del preprocesador de C, requisitos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38ed109c9febe4ead697e2c773f4e45d9af78abdf20bed99400a011ef12294b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807699"
---
# <a name="c-preprocessor-requirements-for-midl"></a>Requisitos de preprocesador de C para MIDL

Esta página solo se aplica a los desarrolladores que tienen motivos específicos para reemplazar el preprocesador de Microsoft C/C++ como el preprocesador usado por MIDL, o a los desarrolladores que deben especificar modificadores de preprocesador personalizados. Los modificadores MIDL [**/cpp \_ cmd**](-cpp-cmd.md), [**/cpp \_ opt**](-cpp-opt.md)y [**/no \_ cpp**](-no-cpp-nocpp.md) se usan para invalidar el comportamiento predeterminado del compilador. Normalmente no hay ninguna razón para reemplazar el preprocesador de Microsoft C/C++, ni para especificar modificadores de preprocesador personalizados.

El compilador MIDL usa un preprocesador de C durante el procesamiento inicial del archivo IDL. El entorno de compilación utilizado al compilar los archivos IDL está asociado a un preprocesador predeterminado de C/C++. Si se va a usar un preprocesador diferente, el modificador del compilador MIDL [**/cpp \_ cmd**](-cpp-cmd.md) habilita una invalidación del nombre predeterminado de preprocesador de C/C++:

``` syntax
midl /cpp_cmd preprocessor_name filename
```

<dl> <dt>

<span id="preprocessor_name"></span><span id="PREPROCESSOR_NAME"></span>*nombre \_ del preprocesador*
</dt> <dd>

Especifica el nombre del preprocesador que va a usar MIDL. Se puede especificar con una ruta de acceso al archivo binario. La .exe es opcional.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Nombre*
</dt> <dd>

Especifica el nombre del archivo IDL.

</dd> </dl>

-   El compilador MIDL espera que cualquier preprocesador observe las convenciones siguientes:
-   El archivo de entrada se especifica como el último argumento en la línea de comandos.
-   El preprocesador debe redirigir la salida al dispositivo de salida estándar, stdout.
-   En el flujo de salida del preprocesador, las **\# directivas de** línea están presentes para habilitar mejores mensajes de diagnóstico.
-   Las directivas de línea son las únicas directivas de preprocesador del flujo de salida.

MIDL supone que el preprocesador generado ha quitado todas las directivas de preprocesador del flujo de entrada del compilador, a excepción de las apariciones de la directiva line necesarias para identificar la ubicación de origen en los mensajes del compilador. Cuando se indica un preprocesador diferente del preprocesador de Microsoft C/C++, o al especificar opciones de preprocesador con el modificador [**/cpp \_ opt,**](-cpp-opt.md) se requiere la especificación de una opción de preprocesador adecuada que ponga las directivas de línea en el flujo de entrada del compilador. Por ejemplo, para el preprocesador de Microsoft C/C++ se tendría que usar la opción **/E:**

``` syntax
midl /cpp_cmd cl.exe /cpp_opt "/E" file.idl
```

MIDL acepta la directiva line en una de las formas siguientes: **\#**

``` syntax
#line digit-sequence "filename" new-line
 
# digit-sequence "filename" new-line
```

Para obtener una descripción completa de la directiva line y otras directivas de preprocesador, consulte la documentación del compilador de C que se usa.

MIDL acepta solo la directiva de preprocesador de línea. Por lo tanto, si se usa el modificador [**/no \_ cpp,**](-no-cpp-nocpp.md) el archivo de entrada no debe tener otras directivas de preprocesador o el archivo de entrada debe haber sido procesado antes de invocar MIDL.

Para obtener más información, vea [Trabajar con define en archivos \# IDL](dealing-with-defines-in-idl-files-2.md).

 

 




