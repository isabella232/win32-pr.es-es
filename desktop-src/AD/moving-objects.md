---
title: Mover objetos
description: Mover objetos
ms.assetid: 3afdf480-a7ee-4b7b-99f6-4a8e8cb2096c
ms.tgt_platform: multiple
keywords:
- Active Directory ejemplos Active Directory, mover objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7019904d0de42492b98ddd297ab007a6f4e52f6a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077509"
---
# <a name="moving-objects"></a><span data-ttu-id="bdaa5-104">Mover objetos</span><span class="sxs-lookup"><span data-stu-id="bdaa5-104">Moving Objects</span></span>

<span data-ttu-id="bdaa5-105">Para trasladar un objeto dentro de un dominio, use el método [**IADsContainer. MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) .</span><span class="sxs-lookup"><span data-stu-id="bdaa5-105">To move an object within a domain, use the [**IADsContainer.MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) method.</span></span>

<span data-ttu-id="bdaa5-106">**Para desplace un objeto dentro de un dominio**</span><span class="sxs-lookup"><span data-stu-id="bdaa5-106">**To move an object within a domain**</span></span>

1.  <span data-ttu-id="bdaa5-107">Enlazar a la interfaz [**IADs**](/windows/desktop/api/iads/nn-iads-iads) del objeto que se va a trasladar.</span><span class="sxs-lookup"><span data-stu-id="bdaa5-107">Bind to the [**IADs**](/windows/desktop/api/iads/nn-iads-iads) interface of the object to move.</span></span>
2.  <span data-ttu-id="bdaa5-108">Obtiene el ADsPath del objeto que se va a desplace de la propiedad [**IADs. ADsPath**](/windows/desktop/ADSI/iads-property-methods) .</span><span class="sxs-lookup"><span data-stu-id="bdaa5-108">Get the ADsPath of the object to move from the [**IADs.ADsPath**](/windows/desktop/ADSI/iads-property-methods) property.</span></span>
3.  <span data-ttu-id="bdaa5-109">Enlazar a la interfaz [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) del contenedor al que se va a desplace el objeto.</span><span class="sxs-lookup"><span data-stu-id="bdaa5-109">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface of the container where the object will be moved to.</span></span>
4.  <span data-ttu-id="bdaa5-110">Mueva el objeto con el método [**IADsContainer. MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) .</span><span class="sxs-lookup"><span data-stu-id="bdaa5-110">Move the object with the [**IADsContainer.MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) method.</span></span>

<span data-ttu-id="bdaa5-111">Si existe una interfaz para el objeto que se ha despasado, la interfaz no es válida después de que el objeto se haya despuesto porque el objeto de directorio que la interfaz representa ya no existe.</span><span class="sxs-lookup"><span data-stu-id="bdaa5-111">If an interface exists to the object that was moved, the interface is not valid after the object is moved because the directory object the interface represents no longer exists.</span></span>

<span data-ttu-id="bdaa5-112">Para obtener más información y un ejemplo de código que muestra cómo mover un objeto, vea el [código de ejemplo para mover un objeto](example-code-for-moving-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="bdaa5-112">For more information and a code example that shows how to move an object, see [Example Code for Moving an Object](example-code-for-moving-an-object.md).</span></span>

 

 