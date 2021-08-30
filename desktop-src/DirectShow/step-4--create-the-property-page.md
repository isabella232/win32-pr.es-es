---
description: Implemente una página de propiedades como parte de la creación de una página de propiedades de filtro para un filtro DirectShow personalizado.
ms.assetid: ed71f26b-0812-4be8-96a4-b9f5dde45540
title: Paso 4. Crear la página de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6cfc2847757e84eb7c59984a6f5042339d2d796562b92cbf7581a9ffb12b012
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107615"
---
# <a name="step-4-create-the-property-page"></a>Paso 4. Crear la página de propiedades

En este momento, el filtro admite todo lo que necesita para una página de propiedades. El siguiente paso es implementar la propia página de propiedades. Comience derivando una nueva clase de **CBasePropertyPage**. En el ejemplo siguiente se muestra parte de la declaración, incluidas algunas variables miembro privadas que se usarán más adelante en el ejemplo:


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



A continuación, cree un recurso de diálogo en el editor de recursos, junto con un recurso de cadena para el título del diálogo. La cadena aparecerá en la pestaña de la página de propiedades. Los dos identificadores de recurso son argumentos del constructor **CBasePropertyPage:**


```C++
CGrayProp::CGrayProp(IUnknown *pUnk) : 
  CBasePropertyPage(NAME("GrayProp"), pUnk, IDD_PROPPAGE, IDS_PROPPAGE_TITLE),
  m_pGray(0)
{ }
```



En la ilustración siguiente se muestra el recurso de diálogo de la página de propiedades de ejemplo.

![cuadro de diálogo de página de propiedades](images/proppage.png)

Ahora está listo para implementar la página de propiedades. Estos son los métodos de **CBasePropertyPage que** se van a invalidar:

-   Se llama a **OnConnect** cuando el cliente crea la página de propiedades. Establece el **puntero IUnknown** al filtro.
-   **Se llama a OnActivate** cuando se crea el cuadro de diálogo.
-   **Se llama a OnReceiveMessage** cuando el cuadro de diálogo recibe un mensaje de ventana.
-   **Se llama a OnApplyChanges** cuando el usuario confirma los cambios de propiedad haciendo clic en **el botón Aceptar** o **Aplicar.**
-   **Se llama a OnDisconnect** cuando el usuario descarta la hoja de propiedades.

En el resto de este tutorial se describe cada uno de estos métodos.

Siguiente: [Paso 5. Almacene un puntero al filtro](step-5--store-a-pointer-to-the-filter.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una página de propiedades de filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



