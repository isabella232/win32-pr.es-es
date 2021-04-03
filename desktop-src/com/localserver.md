---
title: LocalServer
description: Especifica la ruta de acceso completa a una aplicación de servidor local de 16 bits.
ms.assetid: 6eadadd5-f4d3-4e0d-9491-2ea366861aa7
keywords:
- Clave del registro de LocalServer COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7413f9d7c4d17e9498e80d19b70192fbb21911b6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076066"
---
# <a name="localserver"></a><span data-ttu-id="939ea-104">LocalServer</span><span class="sxs-lookup"><span data-stu-id="939ea-104">LocalServer</span></span>

<span data-ttu-id="939ea-105">Especifica la ruta de acceso completa a una aplicación de servidor local de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="939ea-105">Specifies the full path to a 16-bit local server application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="939ea-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="939ea-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      LocalServer = path
```

## <a name="remarks"></a><span data-ttu-id="939ea-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="939ea-107">Remarks</span></span>

<span data-ttu-id="939ea-108">Se trata de un valor de **reg \_ SZ** que especifica la ruta de acceso completa y puede incluir cualquier argumento de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="939ea-108">This is a **REG\_SZ** value that specifies the full path and can include any command-line arguments.</span></span>

<span data-ttu-id="939ea-109">COM anexa la marca "-Embedding" a la cadena, por lo que la aplicación que usa marcas debe analizar toda la cadena y comprobar la marca-Embedding.</span><span class="sxs-lookup"><span data-stu-id="939ea-109">COM appends the "-Embedding" flag to the string, so the application that uses flags must parse the whole string and check for the -Embedding flag.</span></span>

<span data-ttu-id="939ea-110">Para ejecutar un servidor de objetos COM en un espacio de memoria independiente, cambie el valor de **LocalServer** de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="939ea-110">To run a COM object server in a separate memory space, change the value of **LocalServer** as follows:</span></span>

<span data-ttu-id="939ea-111">**cmd/c Start/separate** *ruta de acceso \* \* *. exe**</span><span class="sxs-lookup"><span data-stu-id="939ea-111">**cmd /c start /separate** *path\*\*\*.exe*\*</span></span>

## <a name="related-topics"></a><span data-ttu-id="939ea-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="939ea-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="939ea-113">**LocalServer32**</span><span class="sxs-lookup"><span data-stu-id="939ea-113">**LocalServer32**</span></span>](localserver32.md)
</dt> </dl>

 

 




