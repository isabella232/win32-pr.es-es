---
description: Windows carga y ejecuta el archivo DLL estándar de Microsoft GINA (MSGina.dll). Para cargar un GINA diferente, debe modificar un valor de clave del registro.
ms.assetid: 408511af-4430-4dd7-a2a1-c32b375821c4
title: Cargar y ejecutar un archivo DLL de GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6242ac0124d85d280d951cbc0bfbdbe748fde0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652725"
---
# <a name="loading-and-running-a-gina-dll"></a><span data-ttu-id="67b13-104">Cargar y ejecutar un archivo DLL de GINA</span><span class="sxs-lookup"><span data-stu-id="67b13-104">Loading and Running a GINA DLL</span></span>

<span data-ttu-id="67b13-105">Windows carga y ejecuta el archivo DLL estándar de Microsoft GINA (MSGina.dll).</span><span class="sxs-lookup"><span data-stu-id="67b13-105">Windows loads and executes the standard Microsoft GINA DLL (MSGina.dll).</span></span> <span data-ttu-id="67b13-106">Para cargar un [*Gina*](../secgloss/g-gly.md)diferente, debe modificar el siguiente valor de clave del registro:</span><span class="sxs-lookup"><span data-stu-id="67b13-106">To load a different [*GINA*](../secgloss/g-gly.md), you must alter the following registry key value:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows NT
            CurrentVersion
               Winlogon
                  GinaDLL<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_SZ</dd>
</dl>
```

<span data-ttu-id="67b13-107">Si el valor de la clave GinaDLL está presente, debe contener el nombre de un archivo DLL de GINA, que [*Winlogon*](../secgloss/w-gly.md) cargará y usará.</span><span class="sxs-lookup"><span data-stu-id="67b13-107">If the GinaDLL key value is present, it must contain the name of a GINA DLL, which [*Winlogon*](../secgloss/w-gly.md) will load and use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="67b13-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="67b13-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67b13-109">Compilar y probar un archivo DLL de GINA</span><span class="sxs-lookup"><span data-stu-id="67b13-109">Building and Testing a GINA DLL</span></span>](building-and-testing-a-gina-dll.md)
</dt> <dt>

[<span data-ttu-id="67b13-110">Funciones de exportación de GINA</span><span class="sxs-lookup"><span data-stu-id="67b13-110">GINA Export Functions</span></span>](authentication-functions.md)
</dt> <dt>

[<span data-ttu-id="67b13-111">Estructuras GINA</span><span class="sxs-lookup"><span data-stu-id="67b13-111">GINA Structures</span></span>](authentication-structures.md)
</dt> <dt>

[<span data-ttu-id="67b13-112">Terminal Services funciones GINA</span><span class="sxs-lookup"><span data-stu-id="67b13-112">Terminal Services GINA Functions</span></span>](terminal-services-gina-functions.md)
</dt> </dl>

 

 
