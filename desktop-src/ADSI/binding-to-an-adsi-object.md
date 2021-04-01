---
title: Enlazar a un objeto ADSI
description: La conexión a un objeto en un servicio de directorio se conoce como enlace.
ms.assetid: f3963019-9b3a-42d5-a978-484f294110e5
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, usar, enlazar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c0fefcdb62d374d98e3007864168e2626ecc5d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773009"
---
# <a name="binding-to-an-adsi-object"></a><span data-ttu-id="6c9f7-104">Enlazar a un objeto ADSI</span><span class="sxs-lookup"><span data-stu-id="6c9f7-104">Binding to an ADSI Object</span></span>

<span data-ttu-id="6c9f7-105">La conexión a un objeto en un servicio de directorio se conoce como enlace.</span><span class="sxs-lookup"><span data-stu-id="6c9f7-105">Connecting to an object in a directory service is known as binding.</span></span> <span data-ttu-id="6c9f7-106">El enlace a un objeto ADSI es el primer paso para comunicarse con el sistema de directorio subyacente.</span><span class="sxs-lookup"><span data-stu-id="6c9f7-106">Binding to an ADSI object is the first step to communicating with the underlying directory system.</span></span> <span data-ttu-id="6c9f7-107">Un objeto debe estar enlazado a para navegar por su espacio de nombres, buscar datos, modificar datos o suplantar a un usuario.</span><span class="sxs-lookup"><span data-stu-id="6c9f7-107">An object must be bound to in order to navigate its namespace, search for data, modify data, or impersonate a user.</span></span> <span data-ttu-id="6c9f7-108">También es posible proporcionar características de enlace adicionales, como el nombre de usuario, la contraseña, el nombre del servidor, los métodos de cifrado y la autenticación segura.</span><span class="sxs-lookup"><span data-stu-id="6c9f7-108">It is also possible to supply additional binding characteristics, such as user name, password, server name, encryption methods, and secured authentication.</span></span> <span data-ttu-id="6c9f7-109">Las características de enlace adicionales reales que se pueden usar dependen del proveedor.</span><span class="sxs-lookup"><span data-stu-id="6c9f7-109">The actual additional binding characteristics that can be used will depend on the provider.</span></span>

<span data-ttu-id="6c9f7-110">Para obtener más información acerca del enlace ADSI, vea:</span><span class="sxs-lookup"><span data-stu-id="6c9f7-110">For more information about ADSI binding, see:</span></span>

-   [<span data-ttu-id="6c9f7-111">Cadena de enlace</span><span class="sxs-lookup"><span data-stu-id="6c9f7-111">Binding String</span></span>](binding-string.md)
-   [<span data-ttu-id="6c9f7-112">Tipos de enlace específicos de Active Directory</span><span class="sxs-lookup"><span data-stu-id="6c9f7-112">Binding Types Specific to Active Directory</span></span>](binding-types-specific-to-active-directory.md)
-   [<span data-ttu-id="6c9f7-113">Problemas de enlace para entornos mixtos</span><span class="sxs-lookup"><span data-stu-id="6c9f7-113">Binding Issues for Mixed Environments</span></span>](binding-issues-for-mixed-environments.md)
-   [<span data-ttu-id="6c9f7-114">Enlazar mediante programación con una interfaz ADSI</span><span class="sxs-lookup"><span data-stu-id="6c9f7-114">Binding Programmatically Using an ADSI Interface</span></span>](binding-programmatically-using-an-adsi-interface.md)
-   [<span data-ttu-id="6c9f7-115">Almacenamiento en caché de conexiones</span><span class="sxs-lookup"><span data-stu-id="6c9f7-115">Connection Caching</span></span>](connection-caching.md)
-   [<span data-ttu-id="6c9f7-116">Enlazar a objetos secundarios</span><span class="sxs-lookup"><span data-stu-id="6c9f7-116">Binding to Child Objects</span></span>](binding-to-child-objects.md)
-   [<span data-ttu-id="6c9f7-117">Enlazar al elemento primario de un objeto</span><span class="sxs-lookup"><span data-stu-id="6c9f7-117">Binding to an Object's Parent</span></span>](binding-to-an-objectampaposs-parent.md)
-   [<span data-ttu-id="6c9f7-118">Opción de enlace rápido para operaciones de escritura/modificación por lotes</span><span class="sxs-lookup"><span data-stu-id="6c9f7-118">Fast Binding Option for Batch Write/Modify Operations</span></span>](fast-binding-option-for-batch-writemodify-operations.md)
-   [<span data-ttu-id="6c9f7-119">Elección de una interfaz para el enlace</span><span class="sxs-lookup"><span data-stu-id="6c9f7-119">Choosing an Interface for Binding</span></span>](choosing-an-interface.md)

 

 




