---
title: /LCID (modificador)
description: La opción del compilador/LCID MIDL permite usar caracteres internacionales en los archivos de entrada, nombres de archivo y rutas de acceso de directorio.
ms.assetid: 2ab4ba67-4414-4889-8ed7-83f4888caf8b
keywords:
- /LCID (modificador) MIDL
topic_type:
- apiref
api_name:
- /lcid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 370548bb9899ce84173f2321a129aaeda1c6fe81
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358243"
---
# <a name="lcid-switch"></a><span data-ttu-id="75587-104">/LCID (modificador)</span><span class="sxs-lookup"><span data-stu-id="75587-104">/lcid switch</span></span>

<span data-ttu-id="75587-105">La opción del compilador **/LCID** MIDL permite usar caracteres internacionales en los archivos de entrada, nombres de archivo y rutas de acceso de directorio.</span><span class="sxs-lookup"><span data-stu-id="75587-105">The **/lcid** MIDL compiler option lets you use international characters in your input files, file names, and directory paths.</span></span>

``` syntax
midl /lcid localeID
```

## <a name="switch-options"></a><span data-ttu-id="75587-106">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="75587-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="75587-107">*LCID*</span><span class="sxs-lookup"><span data-stu-id="75587-107">*localeID*</span></span> 
</dt> <dd>

<span data-ttu-id="75587-108">Especifica el identificador de configuración regional de 32 bits usado en la compatibilidad con el idioma nacional de Windows.</span><span class="sxs-lookup"><span data-stu-id="75587-108">Specifies the 32-bit locale identifier used in Windows National Language Support.</span></span> <span data-ttu-id="75587-109">El identificador de configuración regional debe especificarse en formato decimal.</span><span class="sxs-lookup"><span data-stu-id="75587-109">The locale identifier should be specified in decimal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="75587-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="75587-110">Remarks</span></span>

<span data-ttu-id="75587-111">Dentro de los archivos de entrada, puede usar los comentarios, las cadenas, los helpstrings y los identificadores localizados.</span><span class="sxs-lookup"><span data-stu-id="75587-111">Within the input files, you can use localized comments, strings, helpstrings and identifiers.</span></span> <span data-ttu-id="75587-112">En concreto, el modificador **/LCID** proporciona compatibilidad completa con DBCS, para representar idiomas asiáticos como japonés, Chino y coreano.</span><span class="sxs-lookup"><span data-stu-id="75587-112">In particular, the **/lcid** switch provides full DBCS support, to represent Asian languages such as Japanese, Chinese, and Korean.</span></span>

> [!Note]  
> <span data-ttu-id="75587-113">El modificador **/LCID** está disponible con la versión 3.01.75 de MIDL y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="75587-113">The **/lcid** switch is available with MIDL version 3.01.75 and later.</span></span>

 

## <a name="examples"></a><span data-ttu-id="75587-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="75587-114">Examples</span></span>

<span data-ttu-id="75587-115">**MIDL/LCID 1041 iFace. idl**</span><span class="sxs-lookup"><span data-stu-id="75587-115">**midl /lcid 1041 iface.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="75587-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="75587-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75587-117">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="75587-117">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="75587-118">**LCID**</span><span class="sxs-lookup"><span data-stu-id="75587-118">**lcid**</span></span>](lcid.md)
</dt> </dl>

 

 




