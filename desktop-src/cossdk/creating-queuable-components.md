---
description: Un componente con al menos una interfaz queuable es un componente queuable.
ms.assetid: 8183f640-4bf3-4555-8837-90a26130c618
title: Creación de componentes de Queuable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03533168a24da1e1f7279a6f2108e25717054103
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423340"
---
# <a name="creating-queuable-components"></a><span data-ttu-id="ab21b-103">Creación de componentes de Queuable</span><span class="sxs-lookup"><span data-stu-id="ab21b-103">Creating Queuable Components</span></span>

<span data-ttu-id="ab21b-104">Un componente con al menos una interfaz queuable es un *componente queuable*.</span><span class="sxs-lookup"><span data-stu-id="ab21b-104">A component with at least one queuable interface is a *queuable component*.</span></span> <span data-ttu-id="ab21b-105">Para que una cola invoque un componente, las interfaces se deben marcar como queuable y el componente debe estar instalado en una aplicación en cola.</span><span class="sxs-lookup"><span data-stu-id="ab21b-105">For a component to be invoked by a queue, the interfaces must be marked as queuable and the component must be installed in a queued application.</span></span> <span data-ttu-id="ab21b-106">Sin embargo, un componente queuable puede ser un componente de una aplicación no en cola.</span><span class="sxs-lookup"><span data-stu-id="ab21b-106">However, a queuable component can be a component of a non-queued application.</span></span>

<span data-ttu-id="ab21b-107">Una interfaz queuable debe contener solo parámetros in: sin parámetros de salida y sin valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="ab21b-107">A queuable interface must contain only in parameters—no out parameters and no return values.</span></span> <span data-ttu-id="ab21b-108">Estas características se comprueban mediante el análisis de la información de tipo durante la instalación del componente.</span><span class="sxs-lookup"><span data-stu-id="ab21b-108">These characteristics are verified by analyzing the type information during component installation.</span></span> <span data-ttu-id="ab21b-109">Si la interfaz no es queuable, no se puede activar la cola de la aplicación que contiene el componente.</span><span class="sxs-lookup"><span data-stu-id="ab21b-109">If the interface is not queuable, the queue of the application containing the component cannot be activated.</span></span>

<span data-ttu-id="ab21b-110">Para especificar una interfaz de COM+ como queuable, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="ab21b-110">To specify a COM+ interface as queuable, use the following steps:</span></span>

1.  <span data-ttu-id="ab21b-111">En el árbol de consola de la herramienta administrativa Servicios de componentes, en **servicios de componentes**, abra la carpeta **aplicaciones com+** asociada con el equipo que desea administrar.</span><span class="sxs-lookup"><span data-stu-id="ab21b-111">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you wish to manage.</span></span>

2.  <span data-ttu-id="ab21b-112">Abra la carpeta **interfaces** del componente de la aplicación com+ que desea convertir en queuable.</span><span class="sxs-lookup"><span data-stu-id="ab21b-112">Open the **Interfaces** folder of the component of the COM+ application that you want to make queuable.</span></span>

3.  <span data-ttu-id="ab21b-113">Haga clic con el botón secundario en la interfaz que desea marcar como queuable y, a continuación, haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="ab21b-113">Right-click the interface that you want to mark as queuable, and then click **Properties**.</span></span>

4.  <span data-ttu-id="ab21b-114">Seleccione la pestaña **puesta en cola** en el cuadro de diálogo Propiedades.</span><span class="sxs-lookup"><span data-stu-id="ab21b-114">Select the **Queuing** tab in the properties dialog.</span></span>

5.  <span data-ttu-id="ab21b-115">Active la casilla de verificación con la etiqueta **en cola**.</span><span class="sxs-lookup"><span data-stu-id="ab21b-115">Activate the check box labeled **Queued**.</span></span>

    > [!Note]  
    > <span data-ttu-id="ab21b-116">Si la casilla de verificación **en cola** está atenuada, la interfaz no cumple las restricciones de queuable descritas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ab21b-116">If the **Queued** check box is grayed out, the interface does not satisfy the queuable constraints described above.</span></span>

     

6.  <span data-ttu-id="ab21b-117">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="ab21b-117">Click **OK**.</span></span>

    <span data-ttu-id="ab21b-118">Un componente queuable se puede identificar como tal agregando la macro de atributo en cola a la sección interfaz del archivo de código fuente del lenguaje de definición de interfaz (IDL) para todas las interfaces que son queuable.</span><span class="sxs-lookup"><span data-stu-id="ab21b-118">A queuable component can be identified as such by adding the QUEUEABLE attribute macro to the Interface section of the Interface Definition Language (IDL) source file for all interfaces that are queuable.</span></span>

    ``` syntax
#include "mtxattr.h"
    [ object, dual, uuid(), helpstring(IShiphip"), QUEUEABLE ]
    interface IShip:IDispatch{
       [propput, id(1)] HRESULT CustomerId ([in] long CustId);
       [propput, id(2)] HRESULT OrderId ([in] long OrderID);
       [id(3)] HRESULT LineItem ([in] long Qty);
       [id(4)] HRESULT Process ();
    }
    ```

## <a name="related-topics"></a><span data-ttu-id="ab21b-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ab21b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab21b-120">Crear colas de componentes</span><span class="sxs-lookup"><span data-stu-id="ab21b-120">Creating Component Queues</span></span>](creating-component-queues.md)
</dt> <dt>

[<span data-ttu-id="ab21b-121">Desarrollar componentes en cola</span><span class="sxs-lookup"><span data-stu-id="ab21b-121">Developing Queued Components</span></span>](developing-queued-components.md)
</dt> </dl>

 

 



