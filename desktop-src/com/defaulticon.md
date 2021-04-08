---
title: DefaultIcon
description: Proporciona información de icono predeterminada para presentaciones con iconos de objetos.
ms.assetid: 45a3289b-d9c4-4857-bf48-1fd664ce4430
keywords:
- Clave del registro DefaultIcon COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0079fb02f4429c1939f54d643e0a6b08fbc90eb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078423"
---
# <a name="defaulticon"></a><span data-ttu-id="280f3-104">DefaultIcon</span><span class="sxs-lookup"><span data-stu-id="280f3-104">DefaultIcon</span></span>

<span data-ttu-id="280f3-105">Proporciona información de icono predeterminada para presentaciones con iconos de objetos.</span><span class="sxs-lookup"><span data-stu-id="280f3-105">Provides default icon information for iconic presentations of objects.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="280f3-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="280f3-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      DefaultIcon = path, resourceID
```

## <a name="remarks"></a><span data-ttu-id="280f3-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="280f3-107">Remarks</span></span>

<span data-ttu-id="280f3-108">Se trata de un valor de **reg \_ SZ** que especifica la ruta de acceso completa al nombre del archivo ejecutable de la aplicación de objeto y el índice de recursos del icono en el ejecutable.</span><span class="sxs-lookup"><span data-stu-id="280f3-108">This is a **REG\_SZ** value that specifies the full path to the executable name of the object application and the resource index of the icon within the executable.</span></span>

<span data-ttu-id="280f3-109">**DefaultIcon** identifica el icono que se va a usar cuando, por ejemplo, un control se minimice a un icono.</span><span class="sxs-lookup"><span data-stu-id="280f3-109">**DefaultIcon** identifies the icon to use when, for example, a control is minimized to an icon.</span></span> <span data-ttu-id="280f3-110">Esta entrada contiene la ruta de acceso completa al nombre del archivo ejecutable de la aplicación de servidor y el índice de recursos del icono dentro del archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="280f3-110">This entry contains the full path to the executable name of the server application and the resource index of the icon within the executable.</span></span> <span data-ttu-id="280f3-111">Las aplicaciones pueden usar la información proporcionada por **DefaultIcon** para obtener un identificador de icono con [**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona).</span><span class="sxs-lookup"><span data-stu-id="280f3-111">Applications can use the information provided by **DefaultIcon** to obtain an icon handle with [**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona).</span></span>

 

 