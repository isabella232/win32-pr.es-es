---
title: Consulta de información de derechos simples
description: Consulta de información de derechos simples
ms.assetid: 21ed3fb2-35b8-478a-a17e-f6b4da08d50d
keywords:
- SDK de Windows Media Format, consultando los derechos simples
- SDK de Windows Media Format, consultas de derechos simples
- Administración de derechos digitales (DRM), consulta de derechos simples
- DRM (administración de derechos digitales), consulta de derechos simples
- Administración de derechos digitales (DRM), consultas de derechos simples
- DRM (administración de derechos digitales), consultas de derechos simples
- API extendidas del cliente DRM, consultando derechos simples
- API extendidas del cliente, consultando derechos simples
- API extendidas del cliente DRM, consultas de derechos simples
- API extendidas de cliente, consultas de derechos simples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d65929a369ad86753a0e549eb929ad344cdc368
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418716"
---
# <a name="querying-for-simple-rights-information"></a><span data-ttu-id="fd9e0-113">Consulta de información de derechos simples</span><span class="sxs-lookup"><span data-stu-id="fd9e0-113">Querying for Simple Rights Information</span></span>

<span data-ttu-id="fd9e0-114">Las API extendidas del cliente DRM de Windows Media permiten obtener rápidamente información sencilla sobre si se puede tener acceso al contenido protegido para varias acciones.</span><span class="sxs-lookup"><span data-stu-id="fd9e0-114">The Windows Media DRM Client Extended APIs enable you to quickly get simple information about whether protected content can be accessed for various actions.</span></span>

<span data-ttu-id="fd9e0-115">El método [**IWMDRMLicenseQuery:: QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) se puede usar para determinar rápidamente si una acción está permitida por una licencia en el almacén de licencias local.</span><span class="sxs-lookup"><span data-stu-id="fd9e0-115">The [**IWMDRMLicenseQuery::QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) method can be used to determine quickly whether an action is permitted by a license in the local license store.</span></span> <span data-ttu-id="fd9e0-116">**QueryActionAllowed** se ha optimizado para que sea mucho más rápido que las consultas de información similar con los objetos del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="fd9e0-116">**QueryActionAllowed** has been optimized to be much faster than queries for similar information using the objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="fd9e0-117">Sin embargo, este tipo de consulta agrega las licencias en el almacén de licencias local y solo se debe usar para características sencillas, como podría ser necesaria para los elementos de la interfaz de usuario, por ejemplo, para mostrar un indicador de permisos.</span><span class="sxs-lookup"><span data-stu-id="fd9e0-117">However, this type of query aggregates the licenses in the local license store and should be used only for simple features, such as might be needed for user interface elements, for example displaying a permission indicator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd9e0-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fd9e0-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd9e0-119">**Obtención de información de licencias en el almacén de licencias local**</span><span class="sxs-lookup"><span data-stu-id="fd9e0-119">**Getting Information from Licenses in the Local License Store**</span></span>](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




