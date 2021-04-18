---
description: La interfaz de usuario (UI) de tarjeta inteligente es un cuadro de diálogo común que permite al usuario especificar o buscar una tarjeta inteligente para abrirla (es decir, conectarse a una aplicación y usarla en ella).
ms.assetid: a64a617a-b2ae-471f-a88f-a73f0fc3a791
title: Interfaz de usuario de tarjeta inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc558446516149529e9a98d28aa9fe94f80b2777
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668256"
---
# <a name="smart-card-user-interface"></a><span data-ttu-id="3a779-103">Interfaz de usuario de tarjeta inteligente</span><span class="sxs-lookup"><span data-stu-id="3a779-103">Smart Card User Interface</span></span>

<span data-ttu-id="3a779-104">La interfaz de [*usuario*](../secgloss/u-gly.md) (UI) de tarjeta inteligente es un [*cuadro de diálogo común*](../secgloss/s-gly.md) que permite al usuario especificar o buscar una tarjeta inteligente para abrirla (es decir, conectarse a una aplicación y usarla en ella).</span><span class="sxs-lookup"><span data-stu-id="3a779-104">The smart card [*user interface*](../secgloss/u-gly.md) (UI) is a single [*common dialog box*](../secgloss/s-gly.md) that lets the user specify or search for a smart card to open (that is, connect to and use in an application).</span></span>

<span data-ttu-id="3a779-105">A continuación se muestran dos maneras de utilizar el cuadro de diálogo común.</span><span class="sxs-lookup"><span data-stu-id="3a779-105">Following are two ways you can use the common dialog box.</span></span> <span data-ttu-id="3a779-106">Ambos suponen que se mostrará la interfaz de usuario del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="3a779-106">Both assume that the dialog box UI will be displayed.</span></span> <span data-ttu-id="3a779-107">Para obtener más información, vea [**OPENCARDNAME**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea).</span><span class="sxs-lookup"><span data-stu-id="3a779-107">For more information, see [**OPENCARDNAME**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea).</span></span>

<span data-ttu-id="3a779-108">**Para seleccionar una tarjeta inteligente para abrirla**</span><span class="sxs-lookup"><span data-stu-id="3a779-108">**To select a smart card to open**</span></span>

1.  <span data-ttu-id="3a779-109">Declare una variable de tipo **OPENCARDNAME**.</span><span class="sxs-lookup"><span data-stu-id="3a779-109">Declare a variable of type **OPENCARDNAME**.</span></span>
2.  <span data-ttu-id="3a779-110">Proporcione suficiente información en el cuadro de diálogo común para restringir la búsqueda de una tarjeta inteligente que esté buscando la aplicación que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="3a779-110">Provide enough information in the common dialog box to narrow the search for a smart card that the calling application is looking for.</span></span> <span data-ttu-id="3a779-111">Esto incluye especificar **lpstrGroupNames**, **lpstrCardNames** y **rgguidInterfaces**.</span><span class="sxs-lookup"><span data-stu-id="3a779-111">This includes specifying **lpstrGroupNames**, **lpstrCardNames**, and **rgguidInterfaces**.</span></span> <span data-ttu-id="3a779-112">También se incluye la especificación de un modo de uso compartido preferido y el protocolo que se debe usar cuando el cuadro de diálogo común se conecta a la tarjeta mediante los miembros **dwShareMode** y **dwPreferredProtocols** de la estructura [**OPENCARDNAME**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea) .</span><span class="sxs-lookup"><span data-stu-id="3a779-112">This also includes specifying a preferred share mode and protocol to use when the common dialog box connects to the card by using the **dwShareMode** and **dwPreferredProtocols** members of the [**OPENCARDNAME**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea) structure.</span></span>
3.  <span data-ttu-id="3a779-113">Llame a la función [**GetOpenCardName**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) para mostrar el cuadro de diálogo común al usuario.</span><span class="sxs-lookup"><span data-stu-id="3a779-113">Call the [**GetOpenCardName**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) function to display the common dialog box to the user.</span></span> <span data-ttu-id="3a779-114">Se mostrará una línea de información de ayuda simple y, si se encuentra una de las tarjetas que se solicitan, la tarjeta se resaltará en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="3a779-114">A simple help information line will be displayed, and if one of the cards being requested is found, the card will be highlighted in the display.</span></span> <span data-ttu-id="3a779-115">En el caso de las búsquedas de varios nombres de tarjeta, se resaltará el primer lector que contenga una de las tarjetas preferidas.</span><span class="sxs-lookup"><span data-stu-id="3a779-115">For multiple card name searches, the first reader that contains one of the preferred cards will be highlighted.</span></span>
4.  <span data-ttu-id="3a779-116">A continuación, el usuario selecciona una tarjeta, hace clic en **Aceptar** y se conecta a la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="3a779-116">The user then selects a card, clicks **OK**, and connects to the smart card.</span></span>

<span data-ttu-id="3a779-117">**Para buscar una tarjeta específica**</span><span class="sxs-lookup"><span data-stu-id="3a779-117">**To search for a specific card**</span></span>

1.  <span data-ttu-id="3a779-118">Declare una variable de tipo **OPENCARDNAME**.</span><span class="sxs-lookup"><span data-stu-id="3a779-118">Declare a variable of type **OPENCARDNAME**.</span></span>
2.  <span data-ttu-id="3a779-119">Proporcione suficiente información en el cuadro de diálogo común para restringir la búsqueda de una tarjeta inteligente que esté buscando la aplicación que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="3a779-119">Provide enough information in the common dialog box to narrow the search for a smart card that the calling application is looking for.</span></span> <span data-ttu-id="3a779-120">Esto incluye especificar **lpstrGroupNames**, **lpstrCardNames** y **rgguidInterfaces**.</span><span class="sxs-lookup"><span data-stu-id="3a779-120">This includes specifying **lpstrGroupNames**, **lpstrCardNames**, and **rgguidInterfaces**.</span></span>
3.  <span data-ttu-id="3a779-121">Cree las funciones de devolución de llamada **Connect**, **check** y **Disconnect** y establezca los miembros de datos **lpfnConnect**, **lpfnCheck** y **lpfnDisconnect** de forma adecuada.</span><span class="sxs-lookup"><span data-stu-id="3a779-121">Create the **Connect**, **Check**, and **Disconnect** callback functions, and set the **lpfnConnect**, **lpfnCheck**, and **lpfnDisconnect** data members appropriately.</span></span>
    > [!Note]  
    > <span data-ttu-id="3a779-122">Las tres funciones y los miembros deben estar disponibles al usar el cuadro de diálogo común de esta manera.</span><span class="sxs-lookup"><span data-stu-id="3a779-122">All three functions and members must be available when using the common dialog box in this way.</span></span>

     

4.  <span data-ttu-id="3a779-123">Llame a la función de cuadro de diálogo común [**GetOpenCardName**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) .</span><span class="sxs-lookup"><span data-stu-id="3a779-123">Call the [**GetOpenCardName**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) common dialog box function.</span></span>
5.  <span data-ttu-id="3a779-124">El cuadro de diálogo común buscará las tarjetas solicitadas.</span><span class="sxs-lookup"><span data-stu-id="3a779-124">The common dialog box will then search for the requested cards.</span></span> <span data-ttu-id="3a779-125">Si se encuentra un nombre de tarjeta coincidente o una [*cadena ATR*](../secgloss/a-gly.md) , se llamará a las funciones de devolución de llamada **Connect**, **check** y **Disconnect** en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="3a779-125">If a matching card name or [*ATR string*](../secgloss/a-gly.md) is found, the **Connect**, **Check**, and **Disconnect** callback functions will be called in sequence.</span></span> <span data-ttu-id="3a779-126">Si una tarjeta pasa la rutina **check** (es decir, la devolución de llamada **check** devuelve **true**), esta tarjeta se resalta en la pantalla al usuario.</span><span class="sxs-lookup"><span data-stu-id="3a779-126">If a card passes the **Check** routine (that is, the **Check** callback returns **TRUE**), this card is highlighted in the display to the user.</span></span>
    > [!Note]  
    > <span data-ttu-id="3a779-127">Si se especifican varios nombres de tarjeta, el primer lector que contiene una de las tarjetas solicitadas y pasa la rutina de **comprobación** será la tarjeta seleccionada.</span><span class="sxs-lookup"><span data-stu-id="3a779-127">If multiple card names are given, the first reader that contains one of the requested cards and passes the **Check** routine will be the selected card.</span></span>

     

6.  <span data-ttu-id="3a779-128">Si no se encuentran coincidencias, aparecerá un cuadro de diálogo común.</span><span class="sxs-lookup"><span data-stu-id="3a779-128">If no matches are found, a common dialog box will appear.</span></span>

 

 
