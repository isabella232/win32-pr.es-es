---
title: ActivateAtStorage
description: Configura el cliente para crear instancias de objetos en el mismo equipo que el estado persistente que están usando o desde el que se inicializan.
ms.assetid: bc0f0c1c-dbfc-4b7a-b897-3646afe3f6bb
keywords:
- valor del registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2ddd1330191d7b7baf37973dbfb40e267a2f87e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078458"
---
# <a name="activateatstorage"></a><span data-ttu-id="0df1b-104">ActivateAtStorage</span><span class="sxs-lookup"><span data-stu-id="0df1b-104">ActivateAtStorage</span></span>

<span data-ttu-id="0df1b-105">Configura el cliente para crear instancias de objetos en el mismo equipo que el estado persistente que están usando o desde el que se inicializan.</span><span class="sxs-lookup"><span data-stu-id="0df1b-105">Configures the client to instantiate objects on the same computer as the persistent state they are using or from which they are initialized.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="0df1b-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="0df1b-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ActivateAtStorage = value
```

## <a name="remarks"></a><span data-ttu-id="0df1b-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0df1b-107">Remarks</span></span>

<span data-ttu-id="0df1b-108">Este es un valor de **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="0df1b-108">This is a **REG\_SZ** value.</span></span> <span data-ttu-id="0df1b-109">Cualquier valor que comience por ' Y ' o ' y ' indica que debe usarse **ActivateAtStorage** .</span><span class="sxs-lookup"><span data-stu-id="0df1b-109">Any value that begins with 'Y' or 'y' indicates that **ActivateAtStorage** should be used.</span></span>

<span data-ttu-id="0df1b-110">La funcionalidad **ActivateAtStorage** proporciona una manera transparente de permitir que los clientes busquen objetos en ejecución en el mismo equipo que los datos que usan.</span><span class="sxs-lookup"><span data-stu-id="0df1b-110">The **ActivateAtStorage** capability provides a transparent way to allow clients to locate running objects on the same computer as the data that they use.</span></span> <span data-ttu-id="0df1b-111">Esto reduce el tráfico de red porque el objeto realiza llamadas locales del sistema de archivos en lugar de llamadas a través de la red.</span><span class="sxs-lookup"><span data-stu-id="0df1b-111">This reduces network traffic because the object performs local file-system calls instead of calls across the network.</span></span>

<span data-ttu-id="0df1b-112">Cuando se establece un valor para **ActivateAtStorage**, este se convierte en el comportamiento predeterminado en las llamadas a las funciones [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile) y [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage) , así como a la implementación del moniker de archivo de [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject).</span><span class="sxs-lookup"><span data-stu-id="0df1b-112">When a value is set for **ActivateAtStorage**, this becomes the default behavior in calls to the [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile) and [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage) functions, as well as to the file moniker implementation of [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject).</span></span> <span data-ttu-id="0df1b-113">En todas estas llamadas, si se especifica una estructura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) , se invalida el valor de **ActivateAtStorage** para la duración de la llamada de función.</span><span class="sxs-lookup"><span data-stu-id="0df1b-113">In all of these calls, specifying a [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) structure overrides the setting of **ActivateAtStorage** for the duration of the function call.</span></span> <span data-ttu-id="0df1b-114">El autor de la llamada puede pasar información de **COSERVERINFO** a **IMoniker:: BindToObject** a través de la estructura [**BIND \_ OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1) .</span><span class="sxs-lookup"><span data-stu-id="0df1b-114">The caller can pass **COSERVERINFO** information to **IMoniker::BindToObject** through the [**BIND\_OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1) structure.</span></span>

<span data-ttu-id="0df1b-115">El valor establecido para **ActivateAtStorage** también es el comportamiento predeterminado cuando \_ se especifica CLSCTX Remote \_ Server si no hay información del registro para la clase instalada en el equipo del cliente.</span><span class="sxs-lookup"><span data-stu-id="0df1b-115">The value set for **ActivateAtStorage** is also the default behavior when CLSCTX\_REMOTE\_SERVER is specified if no registry information for the class is installed on the client's computer.</span></span> <span data-ttu-id="0df1b-116">Por tanto, las aplicaciones cliente escritas para aprovechar las ventajas de **ActivateAtStorage** pueden requerir menos administración.</span><span class="sxs-lookup"><span data-stu-id="0df1b-116">Client applications written to take advantage of **ActivateAtStorage** may therefore require less administration.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0df1b-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0df1b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0df1b-118">**CLSCTX**</span><span class="sxs-lookup"><span data-stu-id="0df1b-118">**CLSCTX**</span></span>](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)
</dt> <dt>

[<span data-ttu-id="0df1b-119">**CoGetInstanceFromFile**</span><span class="sxs-lookup"><span data-stu-id="0df1b-119">**CoGetInstanceFromFile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
</dt> <dt>

[<span data-ttu-id="0df1b-120">**CoGetInstanceFromIStorage**</span><span class="sxs-lookup"><span data-stu-id="0df1b-120">**CoGetInstanceFromIStorage**</span></span>](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)
</dt> <dt>

[<span data-ttu-id="0df1b-121">**COSERVERINFO**</span><span class="sxs-lookup"><span data-stu-id="0df1b-121">**COSERVERINFO**</span></span>](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo)
</dt> <dt>

[<span data-ttu-id="0df1b-122">**IMoniker:: BindToObject**</span><span class="sxs-lookup"><span data-stu-id="0df1b-122">**IMoniker::BindToObject**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)
</dt> <dt>

[<span data-ttu-id="0df1b-123">Registrar servidores COM</span><span class="sxs-lookup"><span data-stu-id="0df1b-123">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> </dl>

 

 