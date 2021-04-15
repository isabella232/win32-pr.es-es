---
description: Las funciones del cuadro de diálogo específicas del proveedor permiten que un proveedor muestre y controle la información específica de la red mediante la modificación de los cuadros de diálogo del sistema o la visualización de cuadros de diálogo personalizados.
ms.assetid: c9a52867-0a0b-40d8-a09d-2b7bed517e13
title: Provider-Specific funciones del cuadro de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 567c4dcb9f1fd6c2e289d678cf09b3d0d66e4207
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648615"
---
# <a name="provider-specific-dialog-box-functions"></a><span data-ttu-id="61eb9-103">Provider-Specific funciones del cuadro de diálogo</span><span class="sxs-lookup"><span data-stu-id="61eb9-103">Provider-Specific Dialog Box Functions</span></span>

<span data-ttu-id="61eb9-104">Las funciones del cuadro de diálogo específicas del proveedor permiten que un proveedor muestre y controle la información específica de la red mediante la modificación de los cuadros de diálogo del sistema o la visualización de cuadros de diálogo personalizados.</span><span class="sxs-lookup"><span data-stu-id="61eb9-104">Provider-specific dialog box functions enable a provider to display and handle network-specific information by altering system dialog boxes or displaying custom dialog boxes.</span></span>

<span data-ttu-id="61eb9-105">Las siguientes funciones de cuadro de diálogo agregan botones al cuadro de diálogo **propiedades** del administrador de archivos.</span><span class="sxs-lookup"><span data-stu-id="61eb9-105">The following dialog box functions add buttons to the File Manager **Properties** dialog box.</span></span> <span data-ttu-id="61eb9-106">A continuación, el proveedor puede controlar los eventos de esos botones para realizar tareas específicas de la red.</span><span class="sxs-lookup"><span data-stu-id="61eb9-106">The provider can then handle the events of those buttons to perform network-specific tasks.</span></span> <span data-ttu-id="61eb9-107">Tenga en cuenta que hay un límite en el número de botones que se pueden agregar.</span><span class="sxs-lookup"><span data-stu-id="61eb9-107">Note that there is a limit to the number of buttons that can be added.</span></span> <span data-ttu-id="61eb9-108">Por este motivo, los proveedores deben usar esta funcionalidad con moderación.</span><span class="sxs-lookup"><span data-stu-id="61eb9-108">Because of this, providers should use this capability sparingly.</span></span> <span data-ttu-id="61eb9-109">Además, un proveedor puede no ser capaz de agregar un botón porque otros proveedores ya han utilizado el espacio disponible.</span><span class="sxs-lookup"><span data-stu-id="61eb9-109">Also, a provider may find itself unable to add a button because the available space has been used already by other providers.</span></span> <span data-ttu-id="61eb9-110">Un proveedor de red debe controlar esta situación.</span><span class="sxs-lookup"><span data-stu-id="61eb9-110">A network provider should handle this situation.</span></span>



| <span data-ttu-id="61eb9-111">Función</span><span class="sxs-lookup"><span data-stu-id="61eb9-111">Function</span></span>                                           | <span data-ttu-id="61eb9-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="61eb9-112">Description</span></span>                                                                                                                             |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61eb9-113">**NPGetPropertyText**</span><span class="sxs-lookup"><span data-stu-id="61eb9-113">**NPGetPropertyText**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext)     | <span data-ttu-id="61eb9-114">Determina los nombres de los botones que se agregan a un cuadro de diálogo de propiedades para un recurso específico.</span><span class="sxs-lookup"><span data-stu-id="61eb9-114">Determines the names of buttons added to a property dialog box for a specific resource.</span></span><br/>                                      |
| [<span data-ttu-id="61eb9-115">**NPPropertyDialog**</span><span class="sxs-lookup"><span data-stu-id="61eb9-115">**NPPropertyDialog**</span></span>](/windows/desktop/api/Npapi/nf-npapi-nppropertydialog)       | <span data-ttu-id="61eb9-116">Se llama cuando un usuario hace clic en un botón agregado mediante la función [**NPGetPropertyText**](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext) .</span><span class="sxs-lookup"><span data-stu-id="61eb9-116">Called when a user clicks a button added by using the [**NPGetPropertyText**](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext) function.</span></span><br/>               |
| [<span data-ttu-id="61eb9-117">**NPSearchDialog**</span><span class="sxs-lookup"><span data-stu-id="61eb9-117">**NPSearchDialog**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npsearchdialog)           | <span data-ttu-id="61eb9-118">Permite a los proveedores de red implementar su propia funcionalidad de búsqueda más allá de la que se proporciona en el cuadro de diálogo de **conexión** .</span><span class="sxs-lookup"><span data-stu-id="61eb9-118">Enables network providers to implement their own search functionality beyond that provided in the **Connection** dialog box.</span></span><br/> |
| [<span data-ttu-id="61eb9-119">**NPFormatNetworkName**</span><span class="sxs-lookup"><span data-stu-id="61eb9-119">**NPFormatNetworkName**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npformatnetworkname) | <span data-ttu-id="61eb9-120">Permite a los proveedores de red dar formato o modificar los nombres de red antes de que se presenten al usuario.</span><span class="sxs-lookup"><span data-stu-id="61eb9-120">Enables network providers to format or otherwise modify network names before they are presented to the user.</span></span><br/>                 |



 

 

 




