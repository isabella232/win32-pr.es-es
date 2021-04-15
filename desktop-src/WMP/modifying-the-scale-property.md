---
title: Modificar la propiedad Scale
description: Modificar la propiedad Scale
ms.assetid: 32ebaa54-ed13-4b10-8876-bf8e188d7317
keywords:
- Complementos de Media Player de Windows, propiedades de ejemplo de eco
- complementos, propiedades de ejemplo de eco
- Complementos de procesamiento de señal digital, eco de propiedades de ejemplo
- Complementos DSP, propiedades de ejemplo de eco
- Ejemplo de complemento de DSP de eco, propiedad de escala
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd91e2315db9d0d1e14d2aec55f79a8b05c442ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695286"
---
# <a name="modifying-the-scale-property"></a>Modificar la propiedad Scale

La implementación del asistente predeterminada expone la propiedad Scale. Puede cambiar la implementación existente para exponer la propiedad tiempo de retraso en su lugar.

En primer lugar, use el ejemplo siguiente para cambiar los prototipos de función para obtener \_ escala y colocar \_ Scale en echo. h. Cambie el nombre de los métodos y los tipos de datos de los parámetros:


```C++
// IEcho methods
STDMETHOD(get_delay)(DWORD *pVal);
STDMETHOD(put_delay)(DWORD newVal);

```



A continuación, cambie las implementaciones de los \_ métodos Get scale y put \_ Scale en echo. cpp. Haga que el código coincida con los ejemplos siguientes:


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



En el código de ejemplo anterior se cambian los nombres de método y los tipos de datos de parámetro. El nombre de la variable de miembro debe haber cambiado previamente. Recuerde cambiar también los comentarios que introducen cada método.

Ahora, cambie la definición de la interfaz. En el código siguiente se reemplaza el código de la declaración de la interfaz IEcho en echo. idl:


```C++
HRESULT get_delay([out] DWORD *pVal);
HRESULT put_delay([in] DWORD newVal);

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Eco de propiedades de ejemplo**](echo-sample-properties.md)
</dt> </dl>

 

 




