---
description: Paso 2.
ms.assetid: 8be83564-07ad-47cf-9538-73136f42ba79
title: Paso 2. Implementar ISpecifyPropertyPages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3125230c8e28c6bd6b8593839d7175bb43d39674
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688084"
---
# <a name="step-2-implement-ispecifypropertypages"></a>Paso 2. Implementar ISpecifyPropertyPages

A continuación, implemente la interfaz **ISpecifyPropertyPages** en el filtro. Esta interfaz tiene un método único, **GetPages**, que devuelve una matriz de CLSID para las páginas de propiedades que admite el filtro. En este ejemplo, el filtro tiene una sola página de propiedades. Empiece generando el CLSID y declarándolo en el archivo de encabezado:


```C++
// Always create new GUIDs! Never copy a GUID from an example.
DEFINE_GUID(CLSID_SaturationProp, 0xa9bd4eb, 0xded5, 
0x4df0, 0xba, 0xf6, 0x2c, 0xea, 0x23, 0xf5, 0x72, 0x61);
```



Ahora implemente el método **GetPages** :


```C++
class CGrayFilter : public ISaturation,
                    public ISpecifyPropertyPages, 
                    /* Other inherited classes. */
{
public:
    STDMETHODIMP GetPages(CAUUID *pPages)
    {
        if (pPages == NULL) return E_POINTER;
        pPages->cElems = 1;
        pPages->pElems = (GUID*)CoTaskMemAlloc(sizeof(GUID));
        if (pPages->pElems == NULL) 
        {
            return E_OUTOFMEMORY;
        }
        pPages->pElems[0] = CLSID_SaturationProp;
        return S_OK;
    }
};

/* ... */

}
```



Asigne memoria para la matriz mediante **CoTaskMemAlloc**. El autor de la llamada liberará la memoria.

Siguiente: [paso 3. Compatibilidad con QueryInterface](step-3--support-queryinterface.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una página de propiedades de filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



