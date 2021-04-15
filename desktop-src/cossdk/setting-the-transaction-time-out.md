---
description: Puede establecer manualmente el tiempo de espera para las transacciones mediante la herramienta administrativa Servicios de componentes, o bien puede configurar el tiempo de espera mediante programación con las interfaces de administración de COM+.
ms.assetid: f7a35bdf-ea6d-40ea-b3c0-c2a3ae2276c4
title: Establecer la Time-Out de transacciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b002448ca21e97e2e4996679d87a4b6a7680161f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496589"
---
# <a name="setting-the-transaction-time-out"></a><span data-ttu-id="9e115-103">Establecer la Time-Out de transacciones</span><span class="sxs-lookup"><span data-stu-id="9e115-103">Setting the Transaction Time-Out</span></span>

<span data-ttu-id="9e115-104">Puede establecer manualmente el tiempo de espera para las transacciones mediante la herramienta administrativa Servicios de componentes, o bien puede configurar el tiempo de espera mediante programación con las [interfaces de administración de com+](com--administration-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="9e115-104">You can manually set the time-out for transactions by using the Component Services administrative tool, or you can programmatically configure the time-out by using the [COM+ administration interfaces](com--administration-interfaces.md).</span></span> <span data-ttu-id="9e115-105">El tiempo de espera se puede configurar en el nivel de equipo local y también para componentes individuales.</span><span class="sxs-lookup"><span data-stu-id="9e115-105">The time-out can be configured at the local computer level and also for individual components.</span></span>

<span data-ttu-id="9e115-106">**Para establecer el tiempo de espera de la transacción para el equipo local mediante la herramienta administrativa Servicios de componentes**</span><span class="sxs-lookup"><span data-stu-id="9e115-106">**To set the transaction time-out for the local computer by using the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="9e115-107">En el árbol de consola, haga clic con el botón secundario en el equipo local que desee configurar y, a continuación, haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="9e115-107">In the console tree, right-click the local computer you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="9e115-108">En el cuadro de diálogo Propiedades del equipo, haga clic en la pestaña **Opciones** .</span><span class="sxs-lookup"><span data-stu-id="9e115-108">In the computer properties dialog box, click the **Options** tab.</span></span>

3.  <span data-ttu-id="9e115-109">En tiempo de **espera de transacción**, escriba el tiempo de espera de la transacción en segundos.</span><span class="sxs-lookup"><span data-stu-id="9e115-109">Under **Transaction Timeout**, enter the transaction time-out in seconds.</span></span> <span data-ttu-id="9e115-110">El tiempo de espera predeterminado es de 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="9e115-110">The default time-out is 60 seconds.</span></span>

4.  <span data-ttu-id="9e115-111">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="9e115-111">Click **OK**.</span></span>

<span data-ttu-id="9e115-112">**Para establecer el tiempo de espera de la transacción para un componente mediante la herramienta administrativa Servicios de componentes**</span><span class="sxs-lookup"><span data-stu-id="9e115-112">**To set the transaction time-out for a component by using the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="9e115-113">En el árbol de consola, haga clic con el botón secundario en el componente que desee configurar y, a continuación, haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="9e115-113">In the console tree, right-click the component you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="9e115-114">En el cuadro de diálogo Propiedades de componente, haga clic en la pestaña **transacciones** .</span><span class="sxs-lookup"><span data-stu-id="9e115-114">In the component properties dialog box, click the **Transactions** tab.</span></span>

3.  <span data-ttu-id="9e115-115">Active la casilla de verificación **invalidar el valor de tiempo de espera de la transacción global**.</span><span class="sxs-lookup"><span data-stu-id="9e115-115">Check the box labeled **Override global transaction timeout value**.</span></span>

    > [!Note]  
    > <span data-ttu-id="9e115-116">No se puede activar la casilla para invalidar el valor de tiempo de espera de la transacción global si la **compatibilidad con transacciones** está establecida en **deshabilitado**, **no compatible o no** **compatible**.</span><span class="sxs-lookup"><span data-stu-id="9e115-116">You cannot check the box to override the global transaction time-out value if the **Transaction support** is set to **Disabled**, **Not Supported**, or **Supported**.</span></span>

     

4.  <span data-ttu-id="9e115-117">En tiempo de **espera de transacción**, escriba el tiempo de espera de la transacción en segundos.</span><span class="sxs-lookup"><span data-stu-id="9e115-117">Under **Transaction Timeout**, enter the transaction time-out in seconds.</span></span> <span data-ttu-id="9e115-118">El tiempo de espera predeterminado es de 0 segundos, lo que significa que el componente nunca hará que se agote el tiempo de espera de la transacción.</span><span class="sxs-lookup"><span data-stu-id="9e115-118">The default time-out is 0 seconds, which means that the component will never cause the transaction to time out.</span></span>

5.  <span data-ttu-id="9e115-119">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="9e115-119">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e115-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9e115-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e115-121">Administrar transacciones automáticas en COM+</span><span class="sxs-lookup"><span data-stu-id="9e115-121">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



