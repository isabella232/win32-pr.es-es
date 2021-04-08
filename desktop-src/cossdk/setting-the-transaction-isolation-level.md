---
description: Puede establecer manualmente el nivel de aislamiento de transacción de los componentes mediante la herramienta administrativa Servicios de componentes, o bien puede configurar mediante programación el nivel de aislamiento de transacción para un componente mediante las interfaces de administración de COM+.
ms.assetid: 3ef5b805-334d-4803-be67-00c9e35cdcc6
title: Establecer el nivel de aislamiento de la transacción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b0447af2591c4f4b3e8e76c017157c02908367
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807783"
---
# <a name="setting-the-transaction-isolation-level"></a><span data-ttu-id="93568-103">Establecer el nivel de aislamiento de la transacción</span><span class="sxs-lookup"><span data-stu-id="93568-103">Setting the Transaction Isolation Level</span></span>

<span data-ttu-id="93568-104">Puede establecer manualmente el nivel de aislamiento de transacción de los componentes mediante la herramienta administrativa Servicios de componentes, o bien puede configurar mediante programación el nivel de aislamiento de transacción para un componente mediante las [interfaces de administración de com+](com--administration-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="93568-104">You can manually set the transaction isolation level of components by using the Component Services administrative tool, or you can programmatically configure the transaction isolation level for a component by using the [COM+ administration interfaces](com--administration-interfaces.md).</span></span>

<span data-ttu-id="93568-105">Para más información sobre los niveles de aislamiento de transacción, consulte [configuración de los niveles de aislamiento de transacción](configuring-transaction-isolation-levels.md).</span><span class="sxs-lookup"><span data-stu-id="93568-105">For more on transaction isolation levels, see [Configuring Transaction Isolation Levels](configuring-transaction-isolation-levels.md).</span></span>

<span data-ttu-id="93568-106">**Para establecer el nivel de aislamiento de transacción mediante la herramienta administrativa Servicios de componentes**</span><span class="sxs-lookup"><span data-stu-id="93568-106">**To set the transaction isolation level by using the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="93568-107">En el árbol de consola, haga clic con el botón secundario en el componente que desee configurar y, a continuación, haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="93568-107">In the console tree, right-click the component you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="93568-108">En el cuadro de diálogo Propiedades de componente, haga clic en la pestaña **transacciones** .</span><span class="sxs-lookup"><span data-stu-id="93568-108">In the component properties dialog box, click the **Transactions** tab.</span></span>

3.  <span data-ttu-id="93568-109">En **nivel de aislamiento de transacción**, seleccione el valor que desee en el cuadro desplegable.</span><span class="sxs-lookup"><span data-stu-id="93568-109">Under **Transaction Isolation Level**, select the value you want from the drop-down box.</span></span> <span data-ttu-id="93568-110">Se **serializa** el valor predeterminado de todos los componentes.</span><span class="sxs-lookup"><span data-stu-id="93568-110">The default value for all components is **Serialized**.</span></span>

    > [!Note]  
    > <span data-ttu-id="93568-111">Si está seleccionada la opción **deshabilitada** o **no admitida** en **compatibilidad con transacciones**, no se puede establecer el nivel de aislamiento de transacción.</span><span class="sxs-lookup"><span data-stu-id="93568-111">If either **Disabled** or **Not Supported** is selected under **Transaction support**, you cannot set the transaction isolation level.</span></span>

     

4.  <span data-ttu-id="93568-112">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="93568-112">Click **OK**.</span></span>

<span data-ttu-id="93568-113">Debe repetir este procedimiento para cada componente.</span><span class="sxs-lookup"><span data-stu-id="93568-113">You must repeat this procedure for each component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="93568-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="93568-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93568-115">Configuración de los niveles de aislamiento de transacción</span><span class="sxs-lookup"><span data-stu-id="93568-115">Configuring Transaction Isolation Levels</span></span>](configuring-transaction-isolation-levels.md)
</dt> </dl>

 

 



