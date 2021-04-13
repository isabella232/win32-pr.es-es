---
description: Un lápiz de Tablet PC puede tener más de un extremo que puede interactuar con el digitalizador.
ms.assetid: c1aa0d65-cfea-4720-ad09-7add724e03c7
title: Varias funciones con un lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8313e6a13cb48900e0c0d31c2e1e590e07df6c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361575"
---
# <a name="multiple-functionality-with-one-pen"></a><span data-ttu-id="c4bfa-103">Varias funciones con un lápiz</span><span class="sxs-lookup"><span data-stu-id="c4bfa-103">Multiple Functionality with One Pen</span></span>

<span data-ttu-id="c4bfa-104">Un lápiz de Tablet PC puede tener más de un extremo que puede interactuar con el digitalizador.</span><span class="sxs-lookup"><span data-stu-id="c4bfa-104">A Tablet PC pen may have more than one end that can interact with the digitizer.</span></span> <span data-ttu-id="c4bfa-105">Si los dos extremos del lápiz pueden generar eventos, se puede usar un extremo para establecer la tinta, seleccionar y apuntar, y el otro extremo se puede usar para otras funciones como el borrado.</span><span class="sxs-lookup"><span data-stu-id="c4bfa-105">If both ends of the pen can generate events, one end may be used to lay down ink, select, and point, and the other end may be used for other functions such as erasing.</span></span>

<span data-ttu-id="c4bfa-106">Para implementar esta funcionalidad, la aplicación debe poder determinar qué extremo del lápiz se está usando y, por lo tanto, Cuándo cambiar la apariencia del cursor.</span><span class="sxs-lookup"><span data-stu-id="c4bfa-106">To implement such functionality, your application must be able to determine which end of the pen is being used and hence when to change the appearance of the cursor.</span></span> <span data-ttu-id="c4bfa-107">Para ello, puede buscar el estado de la propiedad [**invertida**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) en el objeto [**cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="c4bfa-107">It can do this by looking for the state of the [**Inverted**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) property on the [**Cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

<span data-ttu-id="c4bfa-108">Para obtener detalles específicos sobre el uso de la parte posterior del lápiz para borrar, vea [borrar la entrada manuscrita con el lápiz](erasing-ink-with-the-pen.md).</span><span class="sxs-lookup"><span data-stu-id="c4bfa-108">For specific details about using the back of the pen for erasing, see [Erasing Ink with the Pen](erasing-ink-with-the-pen.md).</span></span> <span data-ttu-id="c4bfa-109">Además, el [ejemplo de borrado de tinta](ink-erasing-sample.md) muestra cómo usar la parte posterior del lápiz para borrar la entrada manuscrita.</span><span class="sxs-lookup"><span data-stu-id="c4bfa-109">In addition, the [Ink Erasing Sample](ink-erasing-sample.md) demonstrates how to use the back of the pen to erase ink.</span></span>

 

 



