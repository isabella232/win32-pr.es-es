---
description: Defina un mecanismo para establecer la propiedad como parte de la creación de una página de propiedades de filtro para un filtro DirectShow personalizado.
ms.assetid: 1912af22-11dc-4864-8c20-91675d4f45d9
title: Paso 1. Definir un mecanismo para establecer la propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 191014c35e27974c52961c2c6218e3a83effcc99
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160111"
---
# <a name="step-1-define-a-mechanism-for-setting-the-property"></a>Paso 1. Definir un mecanismo para establecer la propiedad

El filtro debe admitir una manera de que la página de propiedades se comunique con ella, de modo que la página de propiedades pueda establecer y recuperar propiedades en el filtro. Entre los posibles mecanismos se incluyen los siguientes:

-   Exponer una interfaz COM personalizada.
-   Admite propiedades de Automation mediante **IDispatch**.
-   Exponga **la interfaz IPropertyBag** y defina un conjunto de propiedades con nombre.

En este ejemplo se usa una interfaz COM personalizada, denominada ISaturation. No se trata de una interfaz DirectShow real; solo se define para este ejemplo. Comience declarando la interfaz en un archivo de encabezado, junto con el identificador de interfaz (IID):


```C++
// Always create new GUIDs! Never copy a GUID from an example.
DEFINE_GUID(IID_ISaturation, 0x19412d6e, 0x6401, 
0x475c, 0xb0, 0x48, 0x7a, 0xd2, 0x96, 0xe1, 0x6a, 0x19);

interface ISaturation : public IUnknown
{
    STDMETHOD(GetSaturation)(long *plSat) = 0;
    STDMETHOD(SetSaturation)(long lSat) = 0;
};
```



También puede definir la interfaz con IDL y usar el compilador MIDL para crear el archivo de encabezado. A continuación, implemente la interfaz personalizada en el filtro. En este ejemplo se usan los métodos "Get" y "Set" para el valor de saturación del filtro. Observe que ambos métodos protegen el miembro \_ m lSaturation con una sección crítica.


```C++
class CGrayFilter : public ISaturation, /* Other inherited classes. */
{
private:
    CCritSec  m_csShared;    // Protects shared data.
    long      m_lSaturation; // Saturation level.
public:
    STDMETHODIMP GetSaturation(long *plSat)
    {
        if (!plSat) return E_POINTER;
        CAutoLock lock(&m_csShared);
        *plSat = m_lSaturation;
        return S_OK;
    }
    STDMETHODIMP SetSaturation(long lSat)
    {
        CAutoLock lock(&m_csShared);
        if (lSat < SATURATION_MIN || lSat > SATURATION_MAX)
        {
            return E_INVALIDARG;
        }
        m_lSaturation = lSat;
        return S_OK;
    }
};
```



Por supuesto, los detalles de su propia implementación serán diferentes del ejemplo que se muestra aquí.

Siguiente: [Paso 2. Implemente ISpecifyPropertyPages](step-2--implement-ispecifypropertypages.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CCritSec (clase)**](ccritsec.md)
</dt> <dt>

[Crear una página de propiedades de filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



