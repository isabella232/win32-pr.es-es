---
title: Comprobación de las opciones del preprocesador
description: El compilador MIDL invoca implícitamente el preprocesador y no muestra sus modificadores de preprocesador.
ms.assetid: 2f402af4-18d7-480c-a8d2-d16f402ef87a
keywords:
- MIDL del compilador MIDL, comprobar las opciones de preprocesador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acb9f5055623a44e88ed57b5ed0cadd0034c6962e160a081c7a55a9a51ca9e13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382778"
---
# <a name="verifying-preprocessor-options"></a>Comprobación de las opciones del preprocesador

El compilador MIDL invoca implícitamente el preprocesador y no muestra sus modificadores de preprocesador. En ausencia del modificador [**/cpp \_ opt**](-cpp-opt.md) de MIDL, la línea de comandos del preprocesador se compone de todos los modificadores [**/I,**](-i.md) [**/D**](-d.md) y [**/U**](-u.md) usados en la línea de comandos de MIDL, así como modificadores **/E** y [**/nologo.**](-nologo.md) Para ver los modificadores pasados al preprocesador, use el modificador [**/confirm del**](-confirm.md) compilador.

Por ejemplo, la siguiente línea

**midl.exe -D \_ WIN32 \_ WINNT=0x501 -robust -DNTENV=1 -Id: \\ nt public sdk inc \\ \\ \\ -confirm -Oicf -env win32 -out x86 stub.idl**

genera la siguiente salida:

``` syntax
32 bit arguments
          input file -  stub.idl
          app_config -  No
               c_ext -  Yes
              client -  stub
                char -  signed
             confirm -  Yes
             cpp_cmd -  cl.exe
             cpp_opt -  -Id:\nt\public\sdk\inc -D_WIN32_WINNT=0x501 -DNTENV=1  -
E -nologo
             msc_ver -  1100
               cstub -  i386\stub_c.c
                   D -  -D_WIN32_WINNT=0x501 -DNTENV=1
                 env -  win32
            append64 -  No
               rpcss -  No
             use_epv -  No
      no_default_epv -  No
               error -  allocation ref bounds_check enum stub_data
              header -  i386\stub.h
                   I -  -Id:\nt\public\sdk\inc
              nologo -  No
              ms_ext -  Yes
            ms_union -  No
       no_format_opt -  No
            oldnames -  No
                 out -  i386\
              server -  stub
               sstub -  i386\stub_s.c
                   O -  interpreted stubs
                   W -  1
                  Zp -  8
```

 

 




