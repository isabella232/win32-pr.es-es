---
description: Paso 4.
ms.assetid: ed71f26b-0812-4be8-96a4-b9f5dde45540
title: Paso 4. Crear la página de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52e8ea1a22e30c57c66b263a62afc1e0cf801903
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279669"
---
# <a name="step-4-create-the-property-page"></a>Paso 4. Crear la página de propiedades

En este momento, el filtro admite todo lo que necesita para una página de propiedades. El paso siguiente es implementar la propia página de propiedades. Empiece por derivar una nueva clase de **CBasePropertyPage**. En el ejemplo siguiente se muestra parte de la declaración, incluidas algunas variables miembro privadas que se utilizarán más adelante en el ejemplo:


```C++
class CGrayProp : public CBasePropertyPage
{
private:
    ISaturation *m_pGray;    // Pointer to the filter's custom interface.
    long        m_lVal       // Store the old value, so we can revert.
    long        m_lNewVal;   // New value.
public:
    /* ... */
};
```



A continuación, cree un recurso de cuadro de diálogo en el editor de recursos, junto con un recurso de cadena para el título del cuadro de diálogo. La cadena aparecerá en la pestaña de la página de propiedades. Los dos identificadores de recursos son argumentos del constructor **CBasePropertyPage** :


```C++
CGrayProp::CGrayProp(IUnknown *pUnk) : 
  CBasePropertyPage(NAME("GrayProp"), pUnk, IDD_PROPPAGE, IDS_PROPPAGE_TITLE),
  m_pGray(0)
{ }
```



En la ilustración siguiente se muestra el recurso de cuadro de diálogo de la página de propiedades de ejemplo.

![cuadro de diálogo Página de propiedades](images/proppage.png)

Ahora está listo para implementar la página de propiedades. Estos son los métodos de **CBasePropertyPage** para invalidar:

-   Se llama a **alconnect** cuando el cliente crea la página de propiedades. Establece el puntero **IUnknown** en el filtro.
-   Se llama a **OnActivate** cuando se crea el cuadro de diálogo.
-   Se llama a **OnReceiveMessage** cuando el cuadro de diálogo recibe un mensaje de ventana.
-   Se llama a **OnApplyChanges** cuando el usuario confirma los cambios de propiedad haciendo clic en el botón **Aceptar** o **aplicar** .
-   Se llama a **OnDisconnect** cuando el usuario descarta la hoja de propiedades.

En el resto de este tutorial se describe cada uno de estos métodos.

Siguiente: [paso 5. Almacene un puntero al filtro](step-5--store-a-pointer-to-the-filter.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una página de propiedades de filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



