---
description: Establecer propiedades en efectos y transiciones
ms.assetid: ce773140-7e50-4b72-8cb5-e34cba51644d
title: Establecer propiedades en efectos y transiciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1305eb7860b5519b14cfeebc349643c2662db3f133c0bf3424d1d71ccf85753c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904265"
---
# <a name="setting-properties-on-effects-and-transitions"></a>Establecer propiedades en efectos y transiciones

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Muchas [DirectShow y transiciones de Editing Services](directshow-editing-services.md) admiten propiedades que controlan su comportamiento. Una aplicación puede establecer el valor de una propiedad mediante la [**interfaz IPropertySetter.**](ipropertysetter.md) El efecto subyacente o el objeto de transición deben admitir **IDispatch para** establecer las propiedades. Con los efectos de vídeo y las transiciones, la aplicación puede establecer un intervalo de valores que cambian con el tiempo. (Por ejemplo, puede establecer una transición de borrado para moverse hacia delante y hacia atrás a través del marco). Con los efectos de audio, el valor de la propiedad es estático y no puede cambiar con el tiempo. La única excepción es el [efecto Sobre de](volume-envelope-effect.md) volumen, que admite una propiedad dinámica para el nivel de volumen.

Para establecer una propiedad, realice los pasos siguientes.

1.  Cree una instancia del setter de propiedad (CLSID \_ PropertySetter).
2.  Rellene [**las estructuras DE \_ PARAM**](dexter-param.md) [**y VALUE \_ DE LA PROPIEDAD DE LA PROPIEDAD**](dexter-value.md) con los datos de propiedad. Estas estructuras se deban tratar a continuación.
3.  Pase las [**estructuras \_ PARAM y**](dexter-param.md) EL VALOR [**\_ DE LA PROPIEDAD DE CONTROL AL**](dexter-value.md) MÉTODO [**IPropertySetter::AddProp.**](ipropertysetter-addprop.md)
4.  Repita los pasos 2 y 3 para cada propiedad que quiera establecer.
5.  Pase el [**puntero de interfaz IPropertySetter**](ipropertysetter.md) al [**método IAMTimelineObj::SetPropertySetter.**](iamtimelineobj-setpropertysetter.md)

La [**estructura \_ PARAM DE LA**](dexter-param.md) MARCA ESPECIFICA qué propiedad se va a establecer. Contiene los miembros siguientes.

-   **Name:** nombre de la propiedad
-   **dispID:** Reservado, debe ser cero
-   **nValues:** número de valores

La estructura VALUE de LA \_ PROPIEDAD especifica el valor de una propiedad en un momento dado. Contiene los miembros siguientes.

-   **v**: tipo VARIANT que especifica un nuevo valor para la propiedad . El **miembro vt** de esta VARIANT define el tipo de datos de la propiedad . Para más información sobre el **tipo VARIANT,** consulte el SDK Windows.
-   **rt:** hora de referencia en la que la propiedad asume este valor, en relación con la hora de inicio del efecto o la transición. La hora de inicio del efecto o transición es relativa a la hora de inicio de su objeto primario.
-   **dwInterp:** marca que especifica cómo cambia la propiedad del valor anterior al nuevo valor. Con la marca JUMP \_ de LAFF, la propiedad salta al instante al nuevo valor en el momento especificado. Con la marca \_ INTERPOLATE DE INTERPOLACIÓN DE INTERPOLAF, la propiedad se interpola linealmente desde el valor anterior.

Si establece el miembro **vt** en VT \_ BSTR, el establecedor de propiedades realiza las conversiones necesarias. Para los valores de punto flotante, incluya el cero inicial antes de la posición decimal. Por ejemplo, 0,3, no .3.

> [!Note]  
> Las aplicaciones deben evitar confiar en la conversión de **BSTR** s a valores numéricos. Si la propiedad tiene un valor numérico, use el tipo **VARIANT** numérico adecuado.

 

El valor de una propiedad puede cambiar con el tiempo, por lo que el método [**IPropertySetter::AddProp**](ipropertysetter-addprop.md) toma una única estructura [**\_ PARAM DE PARAM y**](dexter-param.md) un puntero a una matriz de estructuras [**VALUE \_ de LA PROPIEDAD.**](dexter-value.md) La matriz define un conjunto de valores basados en tiempo para la propiedad . Los miembros de la matriz deben estar en orden de hora ascendente y el **miembro nValues** de la estructura PARAM DE PARAM de DESER DEBE ser igual a la \_ longitud de la matriz.

En el ejemplo de código siguiente se crean datos de propiedad para la [transición de borrado de SMPTE.](smpte-wipe-transition.md) Establece el código de borrado en 120, lo que crea un borrado oval. Establece el tiempo de referencia en cero, lo que indica el inicio de la transición.


```C++
IPropertySetter     *pProp;   // Property setter
IAMTimelineObj      *pTransObj;  // Transition object
// Create an SMPTE Wipe transition object. (Not shown)

hr = CoCreateInstance(CLSID_PropertySetter, NULL, CLSCTX_INPROC_SERVER,
    IID_IPropertySetter, (void**) &pProp);

// Error checking is omitted for clarity...

DEXTER_PARAM param;
DEXTER_VALUE *pValue = (DEXTER_VALUE*)CoTaskMemAlloc(sizeof(DEXTER_VALUE));

// Initialize the parameter. 
param.Name = SysAllocString(L"MaskNum");
param.dispID = 0;
param.nValues = 1;

// Initialize the value.
pValue->v.vt = VT_I4;
pValue->v.lVal = 120; // Oval
pValue->rt = 0;
pValue->dwInterp = DEXTERF_JUMP;

pProp->AddProp(param, pValue);

// Free allocated resources.
SysFreeString(param.Name);
VariantClear(&(pValue->v));
CoTaskMemFree(pValue);

// Set the property on the transition.
pTransObj->SetPropertySetter(pProp);
pProp->Release();
```



**Cambiar dinámicamente las propiedades**

Después de representar un proyecto de edición de vídeo, es posible modificar las propiedades de un objeto de efecto o transición mientras se ejecuta el gráfico. Sin embargo, esto solo es posible si establece propiedades en ese objeto antes de la aplicación llamada [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md). Si es así, puede llamar a [**IAMTimelineObj::GetPropertySetter**](iamtimelineobj-getpropertysetter.md) en el efecto o la transición, borrar o modificar las propiedades, y los cambios se realizarán dinámicamente a medida que se ejecute el gráfico. Puede haber anomalías visuales mientras se produce el cambio, por lo que solo se recomienda para la versión preliminar. No cambie las propiedades mientras escribe el proyecto en un archivo.

Si no estableció ninguna propiedad en el objeto de efecto o transición antes de llamar a **ConnectFrontEnd,** no puede agregarle propiedades mientras se ejecuta el gráfico.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con efectos y transiciones](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



