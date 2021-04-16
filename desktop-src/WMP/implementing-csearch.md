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
# <a name="implementing-csearch"></a>Implementación de CSearch

La interfaz **IWMPPluginUI** tiene varios métodos a los que Windows llama Media Player en distintos momentos durante el ciclo de vida de una instancia de complemento. El asistente proporciona implementaciones básicas de estos métodos, así como el constructor de clase y el destructor y otros métodos de clase. El archivo Search. h debe modificarse para que Windows Media Player pueda comunicarse con la interfaz de usuario, que se describe en la sección siguiente.

Para que la clase CPluginWindow tenga acceso a la variable de miembro privado m \_ spCore, se debe realizar una declaración de clase Friend dentro de la definición de clase CSearch, tal y como se muestra en el siguiente fragmento de código:


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación de complementos de la interfaz de usuario**](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 




