---
title: Modificador/i
description: El modificador/I especifica los directorios en los que se van a buscar archivos IDL importados, archivos de encabezado incluidos y archivos ACF.
ms.assetid: cdb0a1c2-ff99-4060-be72-a54dd20dbf93
keywords:
- /I modificador MIDL
topic_type:
- apiref
api_name:
- /I
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ee48ad1e66caf5ed8facbf09ebf2c517c8c895
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076844"
---
# <a name="i-switch"></a>Modificador/i

El modificador **/i** especifica los directorios en los que se van a buscar archivos IDL importados, archivos de encabezado incluidos y archivos ACF.

``` syntax
midl /I include_path
```

## <a name="switch-options"></a>Opciones de conmutador

<dl> <dt>

*Ruta de inclusión \_* 
</dt> <dd>

Especifica uno o más directorios que contienen archivos de importación, inclusión y ACF. El espacio en blanco entre el modificador **/i** y la *ruta de \_ acceso de inclusión* es opcional. Separe varios directorios con un carácter de punto y coma (;).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Puede aparecer más de un directorio con cada modificador **/i** y puede aparecer más de un modificador **/i** con cada invocación del compilador de MIDL. Los directorios se buscan en el orden en que se especifican.

El compilador MIDL pasa también el valor del modificador **/i** al preprocesador de c del compilador de c. Cuando el modificador [**\_ cmd de/CPP**](-cpp-cmd.md) está presente y el modificador [**\_ OPT de/CPP**](-cpp-opt.md) no es, el compilador MIDL concatena la cadena especificada por el modificador **/CPP \_ cmd** con las opciones **/i**, [**/d**](-d.md)y [**/U**](-u.md) y usa esta cadena concatenada para invocar el preprocesador de C para cada archivo de origen IDL y ACF. El modificador de compilador de MIDL **/i** no se pasa al preprocesador cuando se especifica el modificador del compilador MIDL **/no \_ CPP** o **/CPP \_ OPC** .

En los entornos de sistema operativo de Microsoft (Windows de 64 bits, Windows de 32 bits, Windows de 16 bits y MS-DOS), los directorios se buscan en la secuencia siguiente:

1.  Directorio actual
2.  Directorios especificados por el modificador **/i** (en el orden en el que siguen el modificador)
3.  Directorios especificados por la variable de entorno INCLUDE

Cuando se especifican directorios con el modificador **/i** , el modificador [**/no \_ Def \_ Idir**](-no-def-idir.md) indica al compilador de MIDL que omita el directorio actual, omita los directorios especificados por la variable de entorno include y busque solo los directorios especificados.

Cuando no se especifica ningún directorio con el modificador **/i** , el modificador [**/no \_ Def \_ Idir**](-no-def-idir.md) indica al compilador de MIDL que busque solo el directorio actual.

## <a name="examples"></a>Ejemplos

**MIDL/I c: \\ include; c: \\ include \\ h/i \\ include2 nombrearchivo. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**/acf**](-acf.md)
</dt> <dt>

[**/CPP \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/CPP \_ OPC**](-cpp-opt.md)
</dt> <dt>

[**/no \_ Def \_ Idir**](-no-def-idir.md)
</dt> </dl>

 

 




