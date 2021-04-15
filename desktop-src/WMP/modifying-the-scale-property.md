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
# <a name="modifying-the-scale-property"></a><span data-ttu-id="dfed8-108">Modificar la propiedad Scale</span><span class="sxs-lookup"><span data-stu-id="dfed8-108">Modifying the Scale Property</span></span>

<span data-ttu-id="dfed8-109">La implementación del asistente predeterminada expone la propiedad Scale.</span><span class="sxs-lookup"><span data-stu-id="dfed8-109">The default wizard implementation exposes the scale property.</span></span> <span data-ttu-id="dfed8-110">Puede cambiar la implementación existente para exponer la propiedad tiempo de retraso en su lugar.</span><span class="sxs-lookup"><span data-stu-id="dfed8-110">You can change the existing implementation to expose the delay time property instead.</span></span>

<span data-ttu-id="dfed8-111">En primer lugar, use el ejemplo siguiente para cambiar los prototipos de función para obtener \_ escala y colocar \_ Scale en echo. h.</span><span class="sxs-lookup"><span data-stu-id="dfed8-111">First, use the following example to change the function prototypes for get\_scale and put\_scale in Echo.h.</span></span> <span data-ttu-id="dfed8-112">Cambie el nombre de los métodos y los tipos de datos de los parámetros:</span><span class="sxs-lookup"><span data-stu-id="dfed8-112">Change the name of the methods and the data types for the parameters:</span></span>


```C++
// IEcho methods
STDMETHOD(get_delay)(DWORD *pVal);
STDMETHOD(put_delay)(DWORD newVal);

```



<span data-ttu-id="dfed8-113">A continuación, cambie las implementaciones de los \_ métodos Get scale y put \_ Scale en echo. cpp.</span><span class="sxs-lookup"><span data-stu-id="dfed8-113">Next, change the implementations of the get\_scale and put\_scale methods in Echo.cpp.</span></span> <span data-ttu-id="dfed8-114">Haga que el código coincida con los ejemplos siguientes:</span><span class="sxs-lookup"><span data-stu-id="dfed8-114">Make the code match the following examples:</span></span>


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



<span data-ttu-id="dfed8-115">En el código de ejemplo anterior se cambian los nombres de método y los tipos de datos de parámetro.</span><span class="sxs-lookup"><span data-stu-id="dfed8-115">The preceding example code changes the method names and the parameter data types.</span></span> <span data-ttu-id="dfed8-116">El nombre de la variable de miembro debe haber cambiado previamente.</span><span class="sxs-lookup"><span data-stu-id="dfed8-116">The member variable name should have been changed previously.</span></span> <span data-ttu-id="dfed8-117">Recuerde cambiar también los comentarios que introducen cada método.</span><span class="sxs-lookup"><span data-stu-id="dfed8-117">Remember to change the comments that introduce each method as well.</span></span>

<span data-ttu-id="dfed8-118">Ahora, cambie la definición de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="dfed8-118">Now, change the interface definition.</span></span> <span data-ttu-id="dfed8-119">En el código siguiente se reemplaza el código de la declaración de la interfaz IEcho en echo. idl:</span><span class="sxs-lookup"><span data-stu-id="dfed8-119">The following code replaces the code in the IEcho interface declaration in Echo.idl:</span></span>


```C++
HRESULT get_delay([out] DWORD *pVal);
HRESULT put_delay([in] DWORD newVal);

```



## <a name="related-topics"></a><span data-ttu-id="dfed8-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dfed8-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfed8-121">**Eco de propiedades de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="dfed8-121">**Echo Sample Properties**</span></span>](echo-sample-properties.md)
</dt> </dl>

 

 




