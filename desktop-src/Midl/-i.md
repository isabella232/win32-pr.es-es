---
title: Modificador /I
description: El modificador /I especifica los directorios en los que se buscarán los archivos IDL importados, los archivos de encabezado incluidos y los archivos ACF.
ms.assetid: cdb0a1c2-ff99-4060-be72-a54dd20dbf93
keywords:
- /I switch MIDL
topic_type:
- apiref
api_name:
- /I
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ee48ad1e66caf5ed8facbf09ebf2c517c8c895
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159751"
---
# <a name="i-switch"></a>Modificador /I

El **modificador /I** especifica los directorios en los que se buscarán los archivos IDL importados, los archivos de encabezado incluidos y los archivos ACF.

``` syntax
midl /I include_path
```

## <a name="switch-options"></a>Cambiar opciones

<dl> <dt>

*ruta de \_ acceso de include* 
</dt> <dd>

Especifica uno o varios directorios que contienen archivos ACF, include y import. El espacio en blanco entre el **modificador /I** y *la ruta de acceso de \_ include* es opcional. Separe varios directorios con un carácter de punto y coma (;).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Puede aparecer más de un directorio con cada modificador **/I** y puede aparecer más de un modificador **/I** con cada invocación del compilador MIDL. Los directorios se buscan en el orden en que se especifican.

El **compilador de MIDL** también pasa la configuración del modificador /I al preprocesador de C del compilador de C. Cuando el modificador [**/cpp \_ cmd**](-cpp-cmd.md) está presente y el modificador [**/cpp \_ opt**](-cpp-opt.md) no lo está, el compilador MIDL concatena la cadena especificada por el modificador **/cpp \_ cmd** con las opciones **/I,** [**/D**](-d.md)y [**/U**](-u.md) y usa esta cadena concatenada para invocar el preprocesador de C para cada archivo de origen IDL y ACF. El modificador del compilador **MIDL /I** no se pasa al preprocesador cuando se especifica el modificador del compilador MIDL **/no \_ cpp** o **/cpp \_ opt.**

En entornos de sistema operativo de Microsoft (Windows de 64 bits, Windows de 32 bits, Windows de 16 bits y MS-DOS), los directorios se buscan en la secuencia siguiente:

1.  Directorio actual
2.  Directorios especificados por el modificador **/I** (en el orden en que siguen al modificador)
3.  Directorios especificados por la variable de entorno INCLUDE

Cuando se especifican directorios con el modificador **/I,** el modificador [**/no \_ def \_ idir**](-no-def-idir.md) indica al compilador MIDL que ignore el directorio actual, ignore los directorios especificados por la variable de entorno INCLUDE y busque solo los directorios especificados.

Cuando no se especifica ningún directorio con el modificador **/I,** el modificador [**/no \_ def \_ idir**](-no-def-idir.md) indica al compilador MIDL que busque solo el directorio actual.

## <a name="examples"></a>Ejemplos

**midl /I c: \\ include;c: \\ include \\ h /I \\ include2 filename.idl**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/acf**](-acf.md)
</dt> <dt>

[**/cpp \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/cpp \_ opt**](-cpp-opt.md)
</dt> <dt>

[**/no \_ def \_ idir**](-no-def-idir.md)
</dt> </dl>

 

 




