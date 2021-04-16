---
description: Una secuencia del cuadro de diálogo FirstRun recopila información sobre el nombre de usuario, el nombre de la compañía y el ID. del producto. El instalador comprueba el ID. de producto durante este cuadro de diálogo.
ms.assetid: bb77296f-705a-4409-b2ca-a76bbaf7ea57
title: Cuadro de diálogo FirstRun
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2024683d7a10395340a18ddd2015b94e1207bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275930"
---
# <a name="firstrun-dialog"></a><span data-ttu-id="2d147-104">Cuadro de diálogo FirstRun</span><span class="sxs-lookup"><span data-stu-id="2d147-104">FirstRun Dialog</span></span>

<span data-ttu-id="2d147-105">Una secuencia del cuadro de diálogo FirstRun recopila información sobre el nombre de usuario, el nombre de la compañía y el ID. del producto.</span><span class="sxs-lookup"><span data-stu-id="2d147-105">A FirstRun dialog box sequence collects user name, company name, and product ID information.</span></span> <span data-ttu-id="2d147-106">El instalador comprueba el ID. de producto durante este cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2d147-106">The installer verifies the product ID during this dialog.</span></span>

<span data-ttu-id="2d147-107">Normalmente, una secuencia del cuadro de diálogo FirstRun no forma parte de la secuencia de acción y, en su lugar, la llama la función [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) en la primera ejecución del producto.</span><span class="sxs-lookup"><span data-stu-id="2d147-107">A FirstRun dialog box sequence is usually not a part of the action sequence and is instead called by the [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) function on the first run of the product.</span></span>

<span data-ttu-id="2d147-108">Un autor de un paquete del instalador puede usar la secuencia del cuadro de diálogo de plantilla o crear una secuencia diferente.</span><span class="sxs-lookup"><span data-stu-id="2d147-108">An author of an installer package may use the template dialog sequence or create a different sequence.</span></span> <span data-ttu-id="2d147-109">Sin embargo, la secuencia de diálogo necesita que el usuario establezca las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="2d147-109">The dialog sequence however needs to have the user set the following properties:</span></span>

-   <span data-ttu-id="2d147-110">Propiedad [**username**](username.md)</span><span class="sxs-lookup"><span data-stu-id="2d147-110">[**USERNAME**](username.md) property</span></span>
-   <span data-ttu-id="2d147-111">Propiedad [**CompanyName**](companyname.md)</span><span class="sxs-lookup"><span data-stu-id="2d147-111">[**COMPANYNAME**](companyname.md) property</span></span>
-   <span data-ttu-id="2d147-112">Propiedad [**PIDKEY**](pidkey.md)</span><span class="sxs-lookup"><span data-stu-id="2d147-112">[**PIDKEY**](pidkey.md) property</span></span>

<span data-ttu-id="2d147-113">El identificador de producto se validará durante el diálogo con la [Acción ValidateProductID](validateproductid-action.md) o [ValidateProductID ControlEvent,](validateproductid-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="2d147-113">The product ID will be validated during the dialog using the [ValidateProductID action](validateproductid-action.md) or the [ValidateProductID ControlEvent](validateproductid-controlevent.md).</span></span>

<span data-ttu-id="2d147-114">Si el ID. del producto se establece como una propiedad en la línea de comandos o mediante una transformación, la necesidad de que el usuario vuelva a escribir el ID. de producto durante el primer cuadro de diálogo de ejecución se puede eludir controlando la presentación mediante la propiedad [**ProductID**](productid.md) .</span><span class="sxs-lookup"><span data-stu-id="2d147-114">If the product ID is set as a property on the command line, or by a transform, then the necessity of having the user reenter the product ID during the first-run dialog can be circumvented by controlling the display using the [**ProductID**](productid.md) property.</span></span> <span data-ttu-id="2d147-115">Tras la validación correcta del ID. del producto, la propiedad **ProductID** se establece en el identificador de producto válido completo.</span><span class="sxs-lookup"><span data-stu-id="2d147-115">Following the successful validation of the product ID the **ProductID** property is set to the full, valid product ID.</span></span>

 

 



