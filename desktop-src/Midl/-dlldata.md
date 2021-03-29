---
title: modificador/dlldata
description: El modificador/dlldata se usa para especificar el nombre de archivo del archivo dlldata generado para un archivo DLL de proxy. Si no se especifica el modificador/dlldata, se usa el nombre de archivo predeterminado dlldata. c.
ms.assetid: 5211498b-c641-447f-9514-a98766e26ea9
keywords:
- /dlldata modificador MIDL
topic_type:
- apiref
api_name:
- /dlldata
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0e9c1d7f27c56f81905081fd9ef24c8c490391b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784228"
---
# <a name="dlldata-switch"></a><span data-ttu-id="f9c55-105">modificador/dlldata</span><span class="sxs-lookup"><span data-stu-id="f9c55-105">/dlldata switch</span></span>

<span data-ttu-id="f9c55-106">El modificador **/dlldata** se usa para especificar el nombre de archivo del archivo dlldata generado para un archivo dll de proxy.</span><span class="sxs-lookup"><span data-stu-id="f9c55-106">The **/dlldata** switch is used to specify the file name for the generated dlldata file for a proxy DLL.</span></span> <span data-ttu-id="f9c55-107">Si no se especifica el modificador **/dlldata** , se usa el nombre de archivo predeterminado dlldata. c.</span><span class="sxs-lookup"><span data-stu-id="f9c55-107">The default file name Dlldata.c is used if the **/dlldata** switch is not specified.</span></span>

``` syntax
midl /dlldata file-name
```

## <a name="switch-options"></a><span data-ttu-id="f9c55-108">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="f9c55-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="f9c55-109">*nombre de archivo*</span><span class="sxs-lookup"><span data-stu-id="f9c55-109">*file-name*</span></span> 
</dt> <dd>

<span data-ttu-id="f9c55-110">Nombre del archivo de código fuente de C que generará el compilador MIDL para la DLL del proxy.</span><span class="sxs-lookup"><span data-stu-id="f9c55-110">The name of the C source file the MIDL compiler will generate for the proxy DLL.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f9c55-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9c55-111">Remarks</span></span>

<span data-ttu-id="f9c55-112">El archivo especificado por *nombre-archivo* debe estar vinculado al archivo DLL del proxy.</span><span class="sxs-lookup"><span data-stu-id="f9c55-112">The file specified by *file-name* must be linked to the proxy DLL.</span></span> <span data-ttu-id="f9c55-113">El archivo dlldata contiene puntos de entrada y estructuras de datos requeridos por el generador de clases para la DLL del proxy.</span><span class="sxs-lookup"><span data-stu-id="f9c55-113">The dlldata file contains entry points and data structures required by the class factory for the proxy DLL.</span></span> <span data-ttu-id="f9c55-114">Estas estructuras de datos especifican las interfaces de objeto incluidas en el archivo DLL del proxy.</span><span class="sxs-lookup"><span data-stu-id="f9c55-114">These data structures specify the object interfaces contained in the proxy DLL.</span></span> <span data-ttu-id="f9c55-115">El archivo dlldata también especifica el identificador de clase del generador de clases para la DLL del proxy.</span><span class="sxs-lookup"><span data-stu-id="f9c55-115">The dlldata file also specifies the class identifier of the class factory for the proxy DLL.</span></span> <span data-ttu-id="f9c55-116">Siempre es el UUID (IID) de la primera interfaz del primer archivo proxy (por orden alfabético).</span><span class="sxs-lookup"><span data-stu-id="f9c55-116">This is always the UUID (IID) of the first interface of the first proxy file (by alphabetical order).</span></span>

<span data-ttu-id="f9c55-117">Se debe especificar el mismo archivo dlldata al invocar a MIDL en todos los archivos IDL que vayan a un archivo DLL de proxy determinado.</span><span class="sxs-lookup"><span data-stu-id="f9c55-117">The same dlldata file should be specified when invoking MIDL on all the IDL files that will go into a particular proxy DLL.</span></span> <span data-ttu-id="f9c55-118">El archivo dlldata se crea o se actualiza durante cada compilación de MIDL, lo que genera incrementalmente una lista de las interfaces que Irán a la DLL de proxy.</span><span class="sxs-lookup"><span data-stu-id="f9c55-118">The dlldata file is created or updated during each MIDL compilation, incrementally building a list of the interfaces that will go into the proxy DLL.</span></span>

## <a name="examples"></a><span data-ttu-id="f9c55-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f9c55-119">Examples</span></span>

<span data-ttu-id="f9c55-120">**datos/dlldata de MIDL. c**</span><span class="sxs-lookup"><span data-stu-id="f9c55-120">**midl /dlldata data.c**</span></span>

## <a name="see-also"></a><span data-ttu-id="f9c55-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9c55-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9c55-122">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="f9c55-122">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




