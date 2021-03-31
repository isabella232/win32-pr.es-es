---
title: Transferencia de datos
description: Transferencia de datos
ms.assetid: 26b16438-f940-4086-869e-74021ed00b1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37dee268b99f205e0093288f6980c8425220a45b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532451"
---
# <a name="data-transfer"></a><span data-ttu-id="dc211-103">Transferencia de datos</span><span class="sxs-lookup"><span data-stu-id="dc211-103">Data Transfer</span></span>

<span data-ttu-id="dc211-104">El modelo de objetos componentes (COM) proporciona un mecanismo estándar para transferir datos entre aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="dc211-104">The Component Object Model (COM) provides a standard mechanism for transferring data between applications.</span></span> <span data-ttu-id="dc211-105">Este mecanismo es el *objeto de datos*, que es simplemente cualquier objeto com que implementa la interfaz [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) .</span><span class="sxs-lookup"><span data-stu-id="dc211-105">This mechanism is the *data object*, which is simply any COM object that implements the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) interface.</span></span> <span data-ttu-id="dc211-106">Algunos objetos de datos, como un fragmento de texto copiado en el portapapeles, tienen **IDataObject** como su única interfaz.</span><span class="sxs-lookup"><span data-stu-id="dc211-106">Some data objects, such as a piece of text copied to the clipboard, have **IDataObject** as their sole interface.</span></span> <span data-ttu-id="dc211-107">Otros, como los objetos de documento compuestos, exponen varias interfaces, de las cuales **IDataObject** es simplemente uno.</span><span class="sxs-lookup"><span data-stu-id="dc211-107">Others, such as compound document objects, expose several interfaces, of which **IDataObject** is simply one.</span></span> <span data-ttu-id="dc211-108">Los objetos de datos son fundamentales para el trabajo de los documentos compuestos, aunque también tienen una aplicación generalizada fuera de esa tecnología OLE.</span><span class="sxs-lookup"><span data-stu-id="dc211-108">Data objects are fundamental to the working of compound documents, although they also have widespread application outside that OLE technology.</span></span>

<span data-ttu-id="dc211-109">Al intercambiar punteros a un objeto de datos, los proveedores y consumidores de datos pueden administrar las transferencias de datos de manera uniforme, independientemente del formato de los datos, el tipo de medio utilizado para transferir los datos o el dispositivo de destino en el que se va a representar.</span><span class="sxs-lookup"><span data-stu-id="dc211-109">By exchanging pointers to a data object, providers and consumers of data can manage data transfers in a uniform manner, regardless of the format of the data, the type of medium used to transfer the data, or the target device on which it is to be rendered.</span></span> <span data-ttu-id="dc211-110">Puede incluir compatibilidad en la aplicación para las transferencias básicas del portapapeles, las transferencias de arrastrar y colocar, y las transferencias de documentos compuestos OLE con una única implementación de [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject).</span><span class="sxs-lookup"><span data-stu-id="dc211-110">You can include support in your application for basic clipboard transfers, drag and drop transfers, and OLE compound document transfers with a single implementation of [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject).</span></span> <span data-ttu-id="dc211-111">Una vez hecho esto, la cantidad de código necesaria para acomodar la semántica especial de cada protocolo es mínima.</span><span class="sxs-lookup"><span data-stu-id="dc211-111">Having done that, the amount of code required to accommodate the special semantics of each protocol is minimal.</span></span>

<span data-ttu-id="dc211-112">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="dc211-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="dc211-113">Interfaces de Transferencia de datos</span><span class="sxs-lookup"><span data-stu-id="dc211-113">Data Transfer Interfaces</span></span>](data-transfer-interfaces.md)
-   [<span data-ttu-id="dc211-114">Formatos de datos y medios de transferencia</span><span class="sxs-lookup"><span data-stu-id="dc211-114">Data Formats and Transfer Media</span></span>](data-formats-and-transfer-media.md)
-   [<span data-ttu-id="dc211-115">Arrastrar y colocar</span><span class="sxs-lookup"><span data-stu-id="dc211-115">Drag and Drop</span></span>](drag-and-drop.md)

## <a name="related-topics"></a><span data-ttu-id="dc211-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dc211-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc211-117">Documentos compuestos</span><span class="sxs-lookup"><span data-stu-id="dc211-117">Compound Documents</span></span>](compound-documents.md)
</dt> </dl>

 

 




