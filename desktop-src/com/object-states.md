---
title: Estados de objeto
description: Estados de objeto
ms.assetid: 8ebef6d6-7a2f-4b95-91ca-999646cde82d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 268b9bc9c69009850a5172259ab7a13c760d2c72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704585"
---
# <a name="object-states"></a><span data-ttu-id="cc608-103">Estados de objeto</span><span class="sxs-lookup"><span data-stu-id="cc608-103">Object States</span></span>

<span data-ttu-id="cc608-104">Un objeto compuesto existe en uno de tres Estados: pasivo, cargado o en ejecución.</span><span class="sxs-lookup"><span data-stu-id="cc608-104">A compound object exists in one of three states: passive, loaded, or running.</span></span> <span data-ttu-id="cc608-105">El estado de un objeto de documento compuesto describe la relación entre el objeto en su contenedor y la aplicación responsable de su creación.</span><span class="sxs-lookup"><span data-stu-id="cc608-105">A compound-document object's state describes the relationship between the object in its container and the application responsible for its creation.</span></span> <span data-ttu-id="cc608-106">En la tabla siguiente se resumen estos Estados.</span><span class="sxs-lookup"><span data-stu-id="cc608-106">The following table summarizes these states.</span></span>



| <span data-ttu-id="cc608-107">Estado de objeto</span><span class="sxs-lookup"><span data-stu-id="cc608-107">Object state</span></span>       | <span data-ttu-id="cc608-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc608-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc608-109">Pasivo</span><span class="sxs-lookup"><span data-stu-id="cc608-109">Passive</span></span><br/> | <span data-ttu-id="cc608-110">El objeto de documento compuesto solo existe en el almacenamiento, ya sea en el disco o en una base de datos.</span><span class="sxs-lookup"><span data-stu-id="cc608-110">The compound-document object exists only in storage, either on disk or in a database.</span></span> <span data-ttu-id="cc608-111">En este estado, el objeto no está disponible para su visualización o edición.</span><span class="sxs-lookup"><span data-stu-id="cc608-111">In this state, the object is unavailable for viewing or editing.</span></span><br/>                                                                                                                                                                                                                                   |
| <span data-ttu-id="cc608-112">Cargado</span><span class="sxs-lookup"><span data-stu-id="cc608-112">Loaded</span></span><br/>  | <span data-ttu-id="cc608-113">Las estructuras de datos del objeto creadas por el controlador de objetos se encuentran en la memoria del contenedor.</span><span class="sxs-lookup"><span data-stu-id="cc608-113">The object's data structures created by the object handler are in the container's memory.</span></span> <span data-ttu-id="cc608-114">El contenedor ha establecido la comunicación con el controlador de objetos y hay datos de presentación en caché disponibles para representar el objeto.</span><span class="sxs-lookup"><span data-stu-id="cc608-114">The container has established communication with the object handler and there is cached presentation data available for rendering the object.</span></span> <span data-ttu-id="cc608-115">El controlador de objetos procesa las llamadas.</span><span class="sxs-lookup"><span data-stu-id="cc608-115">Calls are processed by the object handler.</span></span> <span data-ttu-id="cc608-116">Este estado, debido a su sobrecarga baja, se usa cuando un usuario simplemente está viendo o imprimiendo un objeto.</span><span class="sxs-lookup"><span data-stu-id="cc608-116">This state, because of its low overhead, is used when a user is simply viewing or printing an object.</span></span><br/> |
| <span data-ttu-id="cc608-117">En ejecución</span><span class="sxs-lookup"><span data-stu-id="cc608-117">Running</span></span><br/> | <span data-ttu-id="cc608-118">Se han creado los objetos que controlan la comunicación remota y se está ejecutando la aplicación de servidor OLE.</span><span class="sxs-lookup"><span data-stu-id="cc608-118">The objects that control remoting have been created and the OLE server application is running.</span></span> <span data-ttu-id="cc608-119">Se puede tener acceso a las interfaces del objeto y el contenedor puede recibir notificaciones de cambios.</span><span class="sxs-lookup"><span data-stu-id="cc608-119">The object's interfaces are accessible, and the container can receive notification of changes.</span></span> <span data-ttu-id="cc608-120">En este estado, un usuario final puede editar o manipular de otro modo el objeto.</span><span class="sxs-lookup"><span data-stu-id="cc608-120">In this state, an end user can edit or otherwise manipulate the object.</span></span><br/>                                                                                                                    |



 

<span data-ttu-id="cc608-121">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="cc608-121">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="cc608-122">Entrando en el estado cargado</span><span class="sxs-lookup"><span data-stu-id="cc608-122">Entering the Loaded State</span></span>](entering-the-loaded-state.md)
-   [<span data-ttu-id="cc608-123">Entrar en el estado de ejecución</span><span class="sxs-lookup"><span data-stu-id="cc608-123">Entering the Running State</span></span>](entering-the-running-state.md)
-   [<span data-ttu-id="cc608-124">Entrar en el estado pasivo</span><span class="sxs-lookup"><span data-stu-id="cc608-124">Entering the Passive State</span></span>](entering-the-passive-state.md)

## <a name="related-topics"></a><span data-ttu-id="cc608-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cc608-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc608-126">Documentos compuestos</span><span class="sxs-lookup"><span data-stu-id="cc608-126">Compound Documents</span></span>](compound-documents.md)
</dt> </dl>

 

 





