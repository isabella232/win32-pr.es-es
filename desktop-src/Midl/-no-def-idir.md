---
title: modificador/no_def_idir
description: Cuando se especifican directorios con el modificador/I, \_ el \_ modificador/no Def Idir indica al compilador de MIDL que solo busque en los directorios especificados con el modificador/i.
ms.assetid: 9a396de4-332d-4832-8e8b-291690cd3a10
keywords:
- /no_def_idir modificador MIDL
topic_type:
- apiref
api_name:
- /no_def_idir
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62ed845c73c36fbbfe4ea7dea952ee4541b043a7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103904194"
---
# <a name="no_def_idir-switch"></a><span data-ttu-id="133cd-104">/no \_ Def \_ Idir modificador</span><span class="sxs-lookup"><span data-stu-id="133cd-104">/no\_def\_idir switch</span></span>

<span data-ttu-id="133cd-105">Cuando se especifican directorios con el modificador [**/i**](-i.md) , el modificador **/no \_ Def \_ Idir** indica al compilador de MIDL que busque solo los directorios especificados con el modificador **/i** , omitiendo el directorio actual, así como los directorios especificados por la variable de entorno include.</span><span class="sxs-lookup"><span data-stu-id="133cd-105">When directories are specified with the [**/I**](-i.md) switch, the **/no\_def\_idir** switch instructs the MIDL compiler to search only the directories specified with the **/I** switch, ignoring the current directory as well as the directories specified by the INCLUDE environment variable.</span></span>

``` syntax
midl /no_def_idir
```

## <a name="switch-options"></a><span data-ttu-id="133cd-106">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="133cd-106">Switch Options</span></span>

<span data-ttu-id="133cd-107">Este modificador no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="133cd-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="133cd-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="133cd-108">Remarks</span></span>

<span data-ttu-id="133cd-109">Cuando no se especifica ningún directorio con el modificador [**/i**](-i.md) , el modificador **/no \_ Def \_ Idir** indica al compilador de MIDL que busque solo el directorio actual.</span><span class="sxs-lookup"><span data-stu-id="133cd-109">When no directories are specified with the [**/I**](-i.md) switch, the **/no\_def\_idir** switch instructs the MIDL compiler to search only the current directory.</span></span>

## <a name="examples"></a><span data-ttu-id="133cd-110">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="133cd-110">Examples</span></span>

``` syntax
; search only the current directory 
midl /no_def_idir filename.idl  

; search only the specified directories 
midl /no_def_idir /I c:\c700\include filename.idl 
```

## <a name="see-also"></a><span data-ttu-id="133cd-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="133cd-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="133cd-112">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="133cd-112">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="133cd-113">**/acf**</span><span class="sxs-lookup"><span data-stu-id="133cd-113">**/acf**</span></span>](-acf.md)
</dt> <dt>

[<span data-ttu-id="133cd-114">**/I**</span><span class="sxs-lookup"><span data-stu-id="133cd-114">**/I**</span></span>](-i.md)
</dt> </dl>

 

 




