---
title: AuxUserType
description: Especifica el nombre para mostrar corto y los nombres de aplicación de una aplicación.
ms.assetid: 3367eb68-01f4-4cb9-b1d0-27554c28b68d
keywords:
- Clave del registro AuxUserType COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c66fcfbcdc2886e93d08040659b39c42d47c291
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772570"
---
# <a name="auxusertype"></a><span data-ttu-id="5e98b-104">AuxUserType</span><span class="sxs-lookup"><span data-stu-id="5e98b-104">AuxUserType</span></span>

<span data-ttu-id="5e98b-105">Especifica el nombre para mostrar corto y los nombres de aplicación de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="5e98b-105">Specifies an application's short display name and application names.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="5e98b-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="5e98b-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AuxUserType
         2 = ShortDisplayName
         3 = ApplicationName
```

## <a name="remarks"></a><span data-ttu-id="5e98b-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5e98b-107">Remarks</span></span>

<span data-ttu-id="5e98b-108">La longitud máxima recomendada para *ShortDisplayName* es de 15 caracteres.</span><span class="sxs-lookup"><span data-stu-id="5e98b-108">The recommended maximum length for *ShortDisplayName* is 15 characters.</span></span> <span data-ttu-id="5e98b-109">Este nombre se usa en los menús, incluidos los menús emergentes.</span><span class="sxs-lookup"><span data-stu-id="5e98b-109">This name is used in menus, including pop-up menus.</span></span>

<span data-ttu-id="5e98b-110">*ApplicationName* debe contener el nombre real de la aplicación (por ejemplo, "Acme Draw 2,0").</span><span class="sxs-lookup"><span data-stu-id="5e98b-110">*ApplicationName* should contain the actual name of the application (such as "Acme Draw 2.0").</span></span> <span data-ttu-id="5e98b-111">Este nombre se utiliza en el campo **resultados** del cuadro de diálogo **Pegar especial** .</span><span class="sxs-lookup"><span data-stu-id="5e98b-111">This name is used in the **Results** field of the **Paste Special** dialog box.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5e98b-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5e98b-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e98b-113">**IOleObject:: GetUserType**</span><span class="sxs-lookup"><span data-stu-id="5e98b-113">**IOleObject::GetUserType**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype)
</dt> </dl>

 

 




