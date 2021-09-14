---
title: Modificar la propiedad Scale
description: Modificar la propiedad Scale
ms.assetid: 32ebaa54-ed13-4b10-8876-bf8e188d7317
keywords:
- Reproductor de Windows Media complementos, propiedades de ejemplo de eco
- complementos, propiedades de ejemplo de eco
- complementos de procesamiento de señales digitales, propiedades de ejemplo de eco
- Complementos de DSP, propiedades de ejemplo de eco
- Ejemplo de complemento DSP de eco, propiedad scale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd91e2315db9d0d1e14d2aec55f79a8b05c442ac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967463"
---
# <a name="modifying-the-scale-property"></a>Modificar la propiedad Scale

La implementación predeterminada del asistente expone la propiedad scale. Puede cambiar la implementación existente para exponer la propiedad delay time en su lugar.

En primer lugar, use el ejemplo siguiente para cambiar los prototipos de función para obtener escala \_ y colocar la escala en \_ Echo.h. Cambie el nombre de los métodos y los tipos de datos de los parámetros:


```C++
// IEcho methods
STDMETHOD(get_delay)(DWORD *pVal);
STDMETHOD(put_delay)(DWORD newVal);

```



A continuación, cambie las implementaciones de los métodos get \_ scale y scale en \_ Echo.cpp. Haga que el código coincida con los ejemplos siguientes:


```C++
// Formerly get_scale
STDMETHODIMP CEcho::get_delay(DWORD *pVal)
{
    if ( NULL == pVal )
    {
        return E_POINTER;
    }

    *pVal = m_dwDelayTime;

    return S_OK;
}

// Formerly put_scale
STDMETHODIMP CEcho::put_delay(DWORD newVal)
{
    m_dwDelayTime = newVal;

    return S_OK;
}

```



El código de ejemplo anterior cambia los nombres de método y los tipos de datos de parámetro. El nombre de la variable miembro debe haber cambiado previamente. Recuerde cambiar también los comentarios que introducen cada método.

Ahora, cambie la definición de la interfaz. El código siguiente reemplaza el código de la declaración de interfaz IEcho en Echo.idl:


```C++
HRESULT get_delay([out] DWORD *pVal);
HRESULT put_delay([in] DWORD newVal);

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Propiedades de ejemplo de eco**](echo-sample-properties.md)
</dt> </dl>

 

 




