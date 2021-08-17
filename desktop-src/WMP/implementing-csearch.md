---
title: Implementación de CSearch
description: Implementación de CSearch
ms.assetid: 3041807a-e7e0-4022-ab90-a8b846bafc0e
keywords:
- Reproductor de Windows Media complementos, clase CSearch
- plug-ins,CSearch (clase)
- complementos de interfaz de usuario, clase CSearch
- Complementos de interfaz de usuario, clase CSearch
- CSearch (clase)
- guía de programación, complementos de interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56f99f3e232d11075bde9905169099649a3b6e754454ac10af60b8a83493fcd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748160"
---
# <a name="implementing-csearch"></a>Implementación de CSearch

La **interfaz IWMPPluginUI** tiene varios métodos a los que llama Reproductor de Windows Media en momentos diferentes durante el ciclo de vida de una instancia de complemento. El asistente proporciona implementaciones básicas de estos métodos, así como el constructor y destructor de clase y otros métodos de clase. El archivo Search.h debe modificarse para que Reproductor de Windows Media pueda comunicarse con la interfaz de usuario, que se describe en la sección siguiente.

Para que la clase CPluginWindow tenga acceso a la variable miembro privada m spCore, se debe realizar una declaración de clase friend dentro de la definición de clase CSearch, como se muestra en el siguiente fragmento de \_ código:


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

[**Interfaz de usuario de programación de complementos de Interfaz de usuario**](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 




