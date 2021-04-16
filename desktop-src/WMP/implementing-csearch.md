---
title: Implementación de CSearch
description: Implementación de CSearch
ms.assetid: 3041807a-e7e0-4022-ab90-a8b846bafc0e
keywords:
- Complementos de Media Player de Windows, clase CSearch
- complementos, clase CSearch
- Complementos de la interfaz de usuario, clase CSearch
- Complementos de la interfaz de usuario, clase CSearch
- Clase CSearch
- Guía de programación, Complementos de la interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36c6446ca0eb6b1cc9dfb5f45044493c2a8fd6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104531996"
---
# <a name="implementing-csearch"></a><span data-ttu-id="ce676-109">Implementación de CSearch</span><span class="sxs-lookup"><span data-stu-id="ce676-109">Implementing CSearch</span></span>

<span data-ttu-id="ce676-110">La interfaz **IWMPPluginUI** tiene varios métodos a los que Windows llama Media Player en distintos momentos durante el ciclo de vida de una instancia de complemento.</span><span class="sxs-lookup"><span data-stu-id="ce676-110">The **IWMPPluginUI** interface has several methods that are called by Windows Media Player at different times during the life cycle of a plug-in instance.</span></span> <span data-ttu-id="ce676-111">El asistente proporciona implementaciones básicas de estos métodos, así como el constructor de clase y el destructor y otros métodos de clase.</span><span class="sxs-lookup"><span data-stu-id="ce676-111">The wizard provides basic implementations of these methods as well as the class constructor and destructor and other class methods.</span></span> <span data-ttu-id="ce676-112">El archivo Search. h debe modificarse para que Windows Media Player pueda comunicarse con la interfaz de usuario, que se describe en la sección siguiente.</span><span class="sxs-lookup"><span data-stu-id="ce676-112">The Search.h file must be modified so that Windows Media Player can communicate with the UI, which is described in the next section.</span></span>

<span data-ttu-id="ce676-113">Para que la clase CPluginWindow tenga acceso a la variable de miembro privado m \_ spCore, se debe realizar una declaración de clase Friend dentro de la definición de clase CSearch, tal y como se muestra en el siguiente fragmento de código:</span><span class="sxs-lookup"><span data-stu-id="ce676-113">For the CPluginWindow class to have access to the private member variable m\_spCore, a friend class declaration must be made inside the CSearch class definition as shown in the following code snippet:</span></span>


```C++
class ATL_NO_VTABLE CSearch : 
    public CComObjectRootEx<CComSingleThreadModel>,
    public CComCoClass<CSearch, &CLSID_Search>,
    public IWMPPluginUI
{

friend class CPluginWindow;

// Rest of class definition...

}

```



## <a name="related-topics"></a><span data-ttu-id="ce676-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ce676-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce676-115">**Guía de programación de complementos de la interfaz de usuario**</span><span class="sxs-lookup"><span data-stu-id="ce676-115">**User Interface Plug-ins Programming Guide**</span></span>](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 




