---
title: El archivo de encabezado
description: El archivo de encabezado contiene definiciones de todos los tipos de datos y operaciones declarados en el archivo IDL, así como todos los tipos de datos y las operaciones declaradas en los archivos incluidos con la Directiva \ include.
ms.assetid: 51789b42-e01c-4233-97da-5e0a044f596f
keywords:
- MIDL y RPC MIDL, interfaces, archivo de encabezado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61331d8bb72d322987c13d02b04632c95424e755
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076057"
---
# <a name="the-header-file"></a><span data-ttu-id="abb03-104">El archivo de encabezado</span><span class="sxs-lookup"><span data-stu-id="abb03-104">The Header File</span></span>

<span data-ttu-id="abb03-105">El archivo de encabezado contiene definiciones de todos los tipos de datos y operaciones declarados en el archivo IDL, así como todos los tipos de datos y las operaciones declaradas en los archivos incluidos con la \# directiva Include.</span><span class="sxs-lookup"><span data-stu-id="abb03-105">The header file contains definitions of all data types and operations declared in the IDL file, as well as all data types and operations declared in the files included with the \#include directive.</span></span> <span data-ttu-id="abb03-106">Los tipos de datos de los archivos importados con la Directiva de importación no se replican en el archivo de encabezado; en su lugar, el archivo de encabezado generado contiene una línea de inclusión en el archivo H generado a partir del archivo importado.</span><span class="sxs-lookup"><span data-stu-id="abb03-106">Data types from the files imported with the import directive are not replicated to the header file; instead the generated header file contains an include line to the H file generated from the imported file.</span></span> <span data-ttu-id="abb03-107">El archivo de encabezado debe estar incluido en todos los módulos de aplicación que llaman a las operaciones definidas, implementan las operaciones definidas o manipulan los tipos definidos.</span><span class="sxs-lookup"><span data-stu-id="abb03-107">The header file must be included by all application modules that call the defined operations, implement the defined operations, or manipulate the defined types.</span></span>

<span data-ttu-id="abb03-108">El compilador MIDL cambia [**/Header**](-header.md) y [**/out**](-out.md) afectan al archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="abb03-108">The MIDL compiler switches [**/header**](-header.md) and [**/out**](-out.md) affect the header file.</span></span>

 

 




