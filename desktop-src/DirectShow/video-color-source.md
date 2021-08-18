---
description: Origen de color de vídeo
ms.assetid: e6addd55-06ca-4d4b-b2b0-fde281fab244
title: Origen de color de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 331640a9240ef0ea16ff565180503066f22ce5ae2550fa1e1ec524dcf05c8fa5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071939"
---
# <a name="video-color-source"></a>Origen de color de vídeo

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El origen de color de vídeo crea una imagen de vídeo continua de un color sólido.

Identificador de clase (CLSID): **{0CFDD070-581A-11D2-9EE6-006008039E37}**

Nombre de la variable CLSID: **CLSID \_ ColorSource**

Propiedades



| Propiedad | Tipo      | Valor predeterminado | Descripción                                   |
|----------|-----------|---------|-----------------------------------------------|
| "Color"  | **DWORD** | 0       | Especifica el color que se generará. Vea la sección Comentarios. |



 

## <a name="remarks"></a>Comentarios

El origen de color de vídeo se usa con objetos de origen. En primer lugar, cree un nuevo objeto de origen. A continuación, establezca el GUID del subobjeto del objeto de origen en CLSID ColorSource, llamando al \_ [**método IAMTimelineObj::SetSubObjectGUID.**](iamtimelineobj-setsubobjectguid.md)

Para establecer el color, cree un [objeto Property Setter](property-setter.md) y aplique la propiedad "Color" en el momento cero. El valor de esta propiedad es un número hexadecimal con el formato *0xAARRGGBB,* donde *AA* es el valor alfa, *RR* es el valor rojo, *GG* es el valor verde y *BB* es el valor azul. Los valores alfa van 0x00 (transparente) a 0xFF (opaco). La propiedad es estática y debe aplicarse en el momento cero.

Si no especifica el valor alfa, el valor predeterminado es cero (transparente). En un proyecto de vídeo de color de 32 bits, esto provocará transiciones o efectos que usan alfa para representar el origen de color de vídeo como completamente transparente. Para que sea seguro, especifique siempre el valor alfa. Por ejemplo, el negro opaco **es 0xFF000000**.

En el ejemplo de código siguiente se muestra cómo usar este objeto . Para obtener más información sobre el [**uso de IPropertySetter,**](ipropertysetter.md)vea [Establecer propiedades en efectos y transiciones:](setting-properties-on-effects-and-transitions.md)


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



En el ejemplo siguiente se muestra la representación XML del objeto creado en el ejemplo anterior. En este caso, [**el elemento param**](param-element.md) no admite [**elementos en**](at-element.md) o [**lineales,**](linear-element.md) porque el objeto no admite propiedades dinámicas:


```C++
<clip start="0" stop="5" clsid="{0CFDD070-581A-11D2-9EE6-006008039E37}">
    <param name="Color" value="16776960"/>
</clip>
```



 

 



