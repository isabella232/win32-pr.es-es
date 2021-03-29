---
title: Tipos de usuarios desconocidos
description: Tipos de usuarios desconocidos
ms.assetid: c2a4bd83-6eaf-4130-8f86-e99f1e18b63d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4843ca2e19508806bba952403a2211a39f5a5ca
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104359454"
---
# <a name="unknown-user-types"></a><span data-ttu-id="fe240-103">Tipos de usuarios desconocidos</span><span class="sxs-lookup"><span data-stu-id="fe240-103">Unknown User Types</span></span>

<span data-ttu-id="fe240-104">Puede facilitar la localización del producto agregando la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="fe240-104">You can ease product localization by adding the following registry key:</span></span>

<span data-ttu-id="fe240-105">**HKEY \_ \_Software de equipos locales \\ \\ Microsoft \\ OLE2** \\ **UnknownUserType**  =  *usertype*</span><span class="sxs-lookup"><span data-stu-id="fe240-105">**HKEY\_LOCAL\_MACHINES\\SOFTWARE\\Microsoft\\OLE2**\\**UnknownUserType** = *usertype*</span></span>

<span data-ttu-id="fe240-106">Esta clave permite que las funciones devuelvan una cadena especificada en lugar de un valor predeterminado de "Unknown", lo que permite a los localizadores especificar un tipo de usuario de otro idioma.</span><span class="sxs-lookup"><span data-stu-id="fe240-106">This key allows functions to return a specified string rather than a default value of "Unknown", enabling localizers to specify a user type of a different language.</span></span>

<span data-ttu-id="fe240-107">La implementación del controlador predeterminado de COM de [**IOleObject:: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) examina el registro llamando a [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype).</span><span class="sxs-lookup"><span data-stu-id="fe240-107">The COM default handler's implementation of [**IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) examines the registry by calling [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype).</span></span> <span data-ttu-id="fe240-108">Si la clase del objeto no se encuentra en el registro, se devuelve el tipo de usuario de la instancia de [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) del objeto.</span><span class="sxs-lookup"><span data-stu-id="fe240-108">If the object's class is not found in the registry, the user type from the object's [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) instance is returned.</span></span> <span data-ttu-id="fe240-109">Si no se encuentra la clase en la instancia **IStorage** del objeto, se devuelve la cadena "Unknown".</span><span class="sxs-lookup"><span data-stu-id="fe240-109">If the class is not found in the object's **IStorage** instance, the string "Unknown" is returned.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe240-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fe240-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe240-111">Registro de aplicaciones COM</span><span class="sxs-lookup"><span data-stu-id="fe240-111">Registering COM Applications</span></span>](registering-com-applications.md)
</dt> </dl>

 

 