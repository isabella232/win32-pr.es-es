---
title: Archivos de encabezado
description: El archivo de encabezado de interfaz (Name. h) contiene definiciones de tipos y declaraciones de función basadas en la definición de interfaz en el archivo IDL actual, así como todos los tipos de datos y operaciones declarados en los archivos incluidos con la Directiva \ include.
ms.assetid: 81fac1fa-6bd7-4a3e-8aa6-5104d4b25b55
keywords:
- archivos de encabezado MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214ae80877b88d8061769b0d6bd56c13469427fc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665705"
---
# <a name="the-header-files"></a><span data-ttu-id="c919f-104">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c919f-104">The Header Files</span></span>

<span data-ttu-id="c919f-105">El archivo de encabezado de interfaz (Name. h) contiene definiciones de tipos y declaraciones de función basadas en la definición de interfaz en el archivo IDL actual, así como todos los tipos de datos y operaciones declarados en los archivos incluidos con la \# directiva Include.</span><span class="sxs-lookup"><span data-stu-id="c919f-105">The interface header file (Name.h) contains type definitions and function declarations based on the interface definition in the current IDL file, as well as all the data types and operations declared in the files included with the \#include directive.</span></span> <span data-ttu-id="c919f-106">Los tipos de datos de los archivos importados con la Directiva de importación no se replican en el archivo de encabezado; en su lugar, el archivo de encabezado generado contiene una línea de inclusión en el archivo H generado a partir del archivo importado.</span><span class="sxs-lookup"><span data-stu-id="c919f-106">Data types from the files imported with the import directive are not replicated to the header file; instead, the generated header file contains an include line to the H file generated from the imported file.</span></span>

<span data-ttu-id="c919f-107">Incluya este archivo en los archivos de origen para el archivo DLL de proxy y para las aplicaciones cliente que utilizan la interfaz.</span><span class="sxs-lookup"><span data-stu-id="c919f-107">Include this file in the source files for the proxy DLL and for client applications that use the interface.</span></span>

<span data-ttu-id="c919f-108">El nombre predeterminado de un archivo de encabezado generado a partir de un archivo. idl es File. h.</span><span class="sxs-lookup"><span data-stu-id="c919f-108">The default name for a header file generated from a file.idl is File.h.</span></span> <span data-ttu-id="c919f-109">El modificador de compilador de MIDL [**/Header**](-header.md) invalida el nombre predeterminado del archivo de encabezado de interfaz.</span><span class="sxs-lookup"><span data-stu-id="c919f-109">The [**/header**](-header.md) MIDL compiler switch overrides the default name of the interface header file.</span></span>

 

 




