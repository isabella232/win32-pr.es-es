---
description: Origen de color de vídeo
ms.assetid: e6addd55-06ca-4d4b-b2b0-fde281fab244
title: Origen de color de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e9c751d74a78b027d50f033acb3709d18fe8f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277583"
---
# <a name="video-color-source"></a>Origen de color de vídeo

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El origen de color de vídeo crea una imagen de vídeo continua de un color sólido.

IDENTIFICADOR de clase (CLSID): **{0CFDD070-581A-11D2-9EE6-006008039E37}**

Nombre de la variable CLSID: **CLSID \_ ColorSource**

Propiedades



| Propiedad | Tipo      | Valor predeterminado | Descripción                                   |
|----------|-----------|---------|-----------------------------------------------|
| Color  | **DWORD** | 0       | Especifica el color que se va a generar. Vea la sección Comentarios. |



 

## <a name="remarks"></a>Observaciones

El origen de color de vídeo se usa con los objetos de origen. En primer lugar, cree un nuevo objeto de origen. A continuación, establezca el GUID del subobjeto del objeto de origen en CLSID \_ ColorSource llamando al método [**IAMTimelineObj:: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) .

Para establecer el color, cree un objeto [setter de propiedad](property-setter.md) y aplique la propiedad "color" en el tiempo cero. El valor de esta propiedad es un número hexadecimal con el formato *0xAARRGGBB*, donde *AA* es el valor alfa, *RR* es el valor rojo, *GG* es el valor verde y *BB* es el valor azul. Los valores alfa van de 0x00 (transparente) a 0xFF (opaco). La propiedad es estática y debe aplicarse en el tiempo cero.

Si no especifica el valor alfa, el valor predeterminado es cero (transparente). En un proyecto de vídeo de color de 32 bits, esto hará que las transiciones o los efectos que usan alfa representen el origen de color de vídeo como completamente transparente. Para que sea segura, especifique siempre el alfa. Por ejemplo, el negro opaco es **0xFF000000**.

En el ejemplo de código siguiente se muestra cómo utilizar este objeto. Para obtener más información sobre el uso de [**IPropertySetter**](ipropertysetter.md), vea [establecer propiedades en efectos y transiciones](setting-properties-on-effects-and-transitions.md):


```C++
DWORD           dwYellow = 0xFFFF00;
IAMTimelineObj  *pSource = NULL;

// Create the source.
HRESULT hr = pTimeline->CreateEmptyNode(&pSource, TIMELINE_MAJOR_TYPE_SOURCE);
if (SUCCEEDED(hr))
{
    hr = pSource->SetStartStop(0, 50000000);
}

if (SUCCEEDED(hr))
{
    hr = pSource->SetSubObjectGUID(CLSID_ColorSource);
}

// Create a property setter.
if (SUCCEEDED(hr))
{
    IPropertySetter *pProp = NULL;
    
    hr = CoCreateInstance(CLSID_PropertySetter, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pProp));

    if SUCCEEDED(hr))
    {
        // Set the color.    
        DEXTER_PARAM param;
        DEXTER_VALUE val;

        param.Name = SysAllocString(OLESTR("Color"));
        param.dispID = 0;
        param.nValues = 1;

        if (param.Name == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
        else
        {
            val.v.vt = VT_I4;
            val.v.lVal = dwYellow;
            val.rt = 0;  // Time must be zero.
            val.dwInterp = DEXTERF_JUMP;

            hr = pProp->AddProp(param, &val);
            
            SysFreeString(param.Name);
        }

        if (SUCCEEDED(hr))
        {
            hr = pSource->SetPropertySetter(pProp); 
        }
        pProp->Release();
    }
}
```



En el ejemplo siguiente se muestra la representación XML del objeto creado en el ejemplo anterior. En este caso, el elemento [**param**](param-element.md) no admite elementos [**en**](at-element.md) o [**lineales**](linear-element.md) , porque el objeto no admite propiedades dinámicas:


```C++
<clip start="0" stop="5" clsid="{0CFDD070-581A-11D2-9EE6-006008039E37}">
    <param name="Color" value="16776960"/>
</clip>
```



 

 



