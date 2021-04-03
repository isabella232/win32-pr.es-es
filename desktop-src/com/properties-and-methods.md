---
title: Propiedades y métodos
description: Al igual que cualquier objeto OLE, un control proporciona gran parte de su funcionalidad a través de un conjunto de interfaces entrantes con propiedades y métodos.
ms.assetid: 5a0cdb5d-7e27-40e9-94db-cfda853879c6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 701b100be635fdb8db9cb51f258dc722edd23eca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075389"
---
# <a name="properties-and-methods"></a><span data-ttu-id="fa477-103">Propiedades y métodos</span><span class="sxs-lookup"><span data-stu-id="fa477-103">Properties and Methods</span></span>

<span data-ttu-id="fa477-104">Al igual que cualquier objeto OLE, un control proporciona gran parte de su funcionalidad a través de un conjunto de interfaces entrantes con propiedades y métodos.</span><span class="sxs-lookup"><span data-stu-id="fa477-104">Like any OLE object, a control provides much of its functionality through a set of incoming interfaces with properties and methods.</span></span>

<span data-ttu-id="fa477-105">Un control expone propiedades y métodos a través de la automatización OLE para que los contenedores puedan tener acceso a ellos bajo el control de un lenguaje de programación proporcionado por el contenedor.</span><span class="sxs-lookup"><span data-stu-id="fa477-105">A control exposes properties and methods through OLE automation so that containers can access them under the control of a container-supplied programming language.</span></span>

<span data-ttu-id="fa477-106">Para admitir el acceso a las propiedades a través de una interfaz de usuario, un control proporciona páginas de propiedades, compatibilidad con \_ las propiedades de OLEIVERB, la exploración de propiedades y el enlace de datos mediante el cambio de propiedad notfications.</span><span class="sxs-lookup"><span data-stu-id="fa477-106">To support access to properties through a user interface, a control provides property pages, support for OLEIVERB\_PROPERTIES, per property browsing, and data binding through property change notfications.</span></span>

-   <span data-ttu-id="fa477-107">A través de las páginas de propiedades, un control puede mostrar sus propiedades, independientemente de su contenedor, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="fa477-107">Through property pages a control can display its properties, independent of its container, if necessary.</span></span>
-   <span data-ttu-id="fa477-108">Al admitir \_ las propiedades de OLEIVERB, el elemento de propiedades se muestra en el menú del contenedor.</span><span class="sxs-lookup"><span data-stu-id="fa477-108">By supporting OLEIVERB\_PROPERTIES, the Properties item is displayed on the container's menu.</span></span> <span data-ttu-id="fa477-109">A continuación, el usuario final puede seleccionar el elemento **propiedades** para ver las páginas de propiedades del control y modificar las propiedades.</span><span class="sxs-lookup"><span data-stu-id="fa477-109">Then, the end user can select the **Properties** item to view the control's property pages and modify the properties.</span></span>
-   <span data-ttu-id="fa477-110">La exploración por propiedad admite un contenedor que puede mostrar las propiedades del control como parte de una hoja de propiedades más grande que puede incluir propiedades de varios controles del contenedor.</span><span class="sxs-lookup"><span data-stu-id="fa477-110">Per property browsing supports a container that can display the control's properties as part of a larger property sheet that may include properties from several controls in the container.</span></span>
-   <span data-ttu-id="fa477-111">A través de la notificación de cambio de propiedad, un control puede notificar a un cliente que sus propiedades tienen cambios, lo que permite al cliente realizar las acciones necesarias como resultado.</span><span class="sxs-lookup"><span data-stu-id="fa477-111">Through property change notification, a control can notify a client that its properties have change, allowing the client to take any necessary actions as a result.</span></span>

<span data-ttu-id="fa477-112">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="fa477-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="fa477-113">Propiedades del control</span><span class="sxs-lookup"><span data-stu-id="fa477-113">Control Properties</span></span>](control-properties.md)
-   [<span data-ttu-id="fa477-114">Métodos de control</span><span class="sxs-lookup"><span data-stu-id="fa477-114">Control Methods</span></span>](control-methods.md)

## <a name="related-topics"></a><span data-ttu-id="fa477-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fa477-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa477-116">Controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="fa477-116">ActiveX Controls</span></span>](activex-controls.md)
</dt> <dt>

[<span data-ttu-id="fa477-117">Páginas de propiedades y hojas de propiedades</span><span class="sxs-lookup"><span data-stu-id="fa477-117">Property Pages and Property Sheets</span></span>](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




