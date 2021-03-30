---
title: Deshabilitar STRICT
description: Para deshabilitar la comprobación estricta de tipos, defina el nombre del símbolo como NO \_ estricto. En Visual C/C++, también puede especificar esta definición en la línea de comandos o en un archivo make si especifica/DNO \_ STRICT como opción del compilador.
ms.assetid: 57b01d2e-1f64-4ac0-b4f0-624c241899d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62bfdfef2aa7988576aa4c1e17f002639de98121
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777514"
---
# <a name="disabling-strict"></a><span data-ttu-id="8c0bf-104">Deshabilitar STRICT</span><span class="sxs-lookup"><span data-stu-id="8c0bf-104">Disabling STRICT</span></span>

<span data-ttu-id="8c0bf-105">Para deshabilitar la comprobación **estricta** de tipos, defina el nombre del símbolo como **no \_ estricto**.</span><span class="sxs-lookup"><span data-stu-id="8c0bf-105">To disable **STRICT** type checking, define the symbol name **NO\_STRICT**.</span></span> <span data-ttu-id="8c0bf-106">En Visual C/C++, también puede especificar esta definición en la línea de comandos o en un archivo make si especifica **/DNO \_ STRICT** como opción del compilador.</span><span class="sxs-lookup"><span data-stu-id="8c0bf-106">In Visual C/C++, you can also specify this definition on the command line or in a makefile by specifying **/DNO\_STRICT** as a compiler option.</span></span>

<span data-ttu-id="8c0bf-107">Para no definir de forma **\_ estricta** cada archivo, inserte una instrucción de **\# definición** antes de incluir Windows. h:</span><span class="sxs-lookup"><span data-stu-id="8c0bf-107">To define **NO\_STRICT** on a file-by-file basis, insert a **\#define** statement before including Windows.h:</span></span>


```C++
#define NO_STRICT
#include <windows.h>
```



<span data-ttu-id="8c0bf-108">Para obtener los mejores resultados, también debe establecer el nivel de advertencia para los mensajes de error en al menos **/W3**.</span><span class="sxs-lookup"><span data-stu-id="8c0bf-108">For best results, you should also set the warning level for error messages to at least **/W3**.</span></span> <span data-ttu-id="8c0bf-109">Esto siempre es aconsejable con las aplicaciones de Windows, ya que una práctica de codificación que genera una advertencia (por ejemplo, pasando el número incorrecto de parámetros) suele provocar un error irrecuperable en tiempo de ejecución si no se corrige.</span><span class="sxs-lookup"><span data-stu-id="8c0bf-109">This is always advisable with applications for Windows, because a coding practice that causes a warning (for example, passing the wrong number of parameters) usually causes a fatal error at run time if it is not corrected.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c0bf-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8c0bf-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c0bf-111">Habilitar STRICT</span><span class="sxs-lookup"><span data-stu-id="8c0bf-111">Enabling STRICT</span></span>](enabling-strict.md)
</dt> <dt>

[<span data-ttu-id="8c0bf-112">Cumplimiento estricto</span><span class="sxs-lookup"><span data-stu-id="8c0bf-112">STRICT Compliance</span></span>](strict-compliance.md)
</dt> </dl>

 

 




