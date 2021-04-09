---
title: include (atributo)
description: La instrucción de inclusión ACF especifica uno o varios archivos de encabezado que se incluirán en el código auxiliar generado.
ms.assetid: f83a704b-2f6e-4498-97ff-593fef2e92dc
keywords:
- atributo de inclusión MIDL
topic_type:
- apiref
api_name:
- include
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2aab7b7262bceb330e3f4645e4f16035b783197
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104148889"
---
# <a name="include-attribute"></a><span data-ttu-id="d7072-104">include (atributo)</span><span class="sxs-lookup"><span data-stu-id="d7072-104">include attribute</span></span>

<span data-ttu-id="d7072-105">La instrucción de **inclusión** ACF especifica uno o varios archivos de encabezado que se incluirán en el código auxiliar generado.</span><span class="sxs-lookup"><span data-stu-id="d7072-105">The ACF **include** statement specifies one or more header files to be included in the generated stub code.</span></span>

``` syntax
include filenames;
```

## <a name="parameters"></a><span data-ttu-id="d7072-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d7072-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7072-107">*nombres*</span><span class="sxs-lookup"><span data-stu-id="d7072-107">*filenames*</span></span> 
</dt> <dd>

<span data-ttu-id="d7072-108">Especifica el nombre de uno o más archivos de encabezado de lenguaje C.</span><span class="sxs-lookup"><span data-stu-id="d7072-108">Specifies the name of one or more C-language header files.</span></span> <span data-ttu-id="d7072-109">Use el nombre de archivo completo, incluido. H y escriba cada nombre de archivo entre comillas.</span><span class="sxs-lookup"><span data-stu-id="d7072-109">Use the full file name, including the .H extension and enclose each file name in quotation marks.</span></span> <span data-ttu-id="d7072-110">Separe varios nombres de archivo de encabezado de lenguaje C con comas.</span><span class="sxs-lookup"><span data-stu-id="d7072-110">Separate multiple C-language header file names with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7072-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7072-111">Remarks</span></span>

<span data-ttu-id="d7072-112">Como resultado de la instrucción **include** , el código auxiliar generado contendrá una instrucción **\# include** de C-preprocesador.</span><span class="sxs-lookup"><span data-stu-id="d7072-112">As a result of the **include** statement, the generated stub code will contain a C-preprocessor **\#include** statement.</span></span> <span data-ttu-id="d7072-113">El archivo de encabezado del lenguaje C se proporciona al compilar el código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="d7072-113">You supply the C-language header file when compiling the stubs.</span></span> <span data-ttu-id="d7072-114">Las instrucciones include se basan en el mecanismo del compilador de C para buscar archivos incluidos en la estructura de directorios.</span><span class="sxs-lookup"><span data-stu-id="d7072-114">Include statements rely on the C-compiler mechanism of searching the directory structure for included files.</span></span>

> [!Note]  
> <span data-ttu-id="d7072-115">Use la Directiva de [**importación**](import.md) en lugar de la directiva **include** para los archivos del sistema que contengan tipos de datos que desee poner a disposición del archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="d7072-115">Use the [**import**](import.md) directive rather than the **include** directive for system files that contain data types you want to make available to the IDL file.</span></span> <span data-ttu-id="d7072-116">La Directiva de **importación** omite los prototipos de función y permite utilizar modificadores de compilador MIDL que optimizan la generación de rutinas de soporte.</span><span class="sxs-lookup"><span data-stu-id="d7072-116">The **import** directive ignores function prototypes and allows you to use MIDL compiler switches that optimize the generation of support routines.</span></span>

 

## <a name="examples"></a><span data-ttu-id="d7072-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d7072-117">Examples</span></span>

``` syntax
include "local.h";
include "gendefs.h", "protos.h", "mystuff.h";
```

## <a name="see-also"></a><span data-ttu-id="d7072-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7072-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7072-119">Archivo de configuración de la aplicación (ACF)</span><span class="sxs-lookup"><span data-stu-id="d7072-119">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="d7072-120">**importar**</span><span class="sxs-lookup"><span data-stu-id="d7072-120">**import**</span></span>](import.md)
</dt> <dt>

[<span data-ttu-id="d7072-121">Importar archivos y bibliotecas de tipos</span><span class="sxs-lookup"><span data-stu-id="d7072-121">Importing Files and Type Libraries</span></span>](importing-files-and-type-libraries.md)
</dt> <dt>

[<span data-ttu-id="d7072-122">Importación de archivos de encabezado del sistema</span><span class="sxs-lookup"><span data-stu-id="d7072-122">Importing System Header Files</span></span>](importing-system-header-files.md)
</dt> </dl>

 

 




