---
description: Establecer propiedades en efectos y transiciones
ms.assetid: ce773140-7e50-4b72-8cb5-e34cba51644d
title: Establecer propiedades en efectos y transiciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4ddd129eb9d4ab24ebef6f5c760a4211f26c9a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677029"
---
# <a name="setting-properties-on-effects-and-transitions"></a>Establecer propiedades en efectos y transiciones

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Muchos efectos y transiciones de los [servicios de edición de DirectShow](directshow-editing-services.md) admiten propiedades que controlan su comportamiento. Una aplicación puede establecer el valor de una propiedad mediante la interfaz [**IPropertySetter**](ipropertysetter.md) . El objeto de efecto o transición subyacente debe admitir **IDispatch** para establecer las propiedades. Con las transiciones y los efectos de vídeo, la aplicación puede establecer un intervalo de valores que cambian con el tiempo. (Por ejemplo, puede establecer una transición de borrado para retroceder y avanzar por el marco). Con los efectos de audio, el valor de la propiedad es estático y no puede cambiar con el tiempo. La única excepción es el efecto de [sobre de volumen](volume-envelope-effect.md) , que admite una propiedad dinámica para el nivel de volumen.

Para establecer una propiedad, realice los pasos siguientes.

1.  Cree una instancia del establecedor de propiedad (CLSID \_ PropertySetter).
2.  Rellene las estructuras [**de \_ valor**](dexter-value.md) de [**Dexterity \_**](dexter-param.md) y Dexterity con los datos de la propiedad. Estas estructuras se describen a continuación.
3.  Pase las estructuras de valor [**Dexterity \_**](dexter-param.md) y [**Dexterity \_**](dexter-value.md) al método [**IPropertySetter:: AddProp**](ipropertysetter-addprop.md) .
4.  Repita los pasos 2 y 3 para cada propiedad que desee establecer.
5.  Pase el puntero de la interfaz [**IPropertySetter**](ipropertysetter.md) al método [**IAMTimelineObj:: SetPropertySetter**](iamtimelineobj-setpropertysetter.md) .

La estructura del [**\_ parámetro dexterss**](dexter-param.md) especifica qué propiedad se establece. Contiene los miembros siguientes.

-   **Nombre**: nombre de la propiedad
-   **DISPID**: Reserved, debe ser cero
-   **nvalores**: número de valores

La \_ estructura de valores de Dexterity especifica el valor de una propiedad en un momento dado. Contiene los miembros siguientes.

-   **v**: tipo Variant que especifica un nuevo valor para la propiedad. El miembro **VT** de esta variante define el tipo de datos de la propiedad. Para obtener más información sobre el tipo **Variant** , vea el Windows SDK.
-   **RT**: tiempo de referencia cuando la propiedad asume este valor, en relación con la hora de inicio del efecto o la transición. La hora de inicio del efecto o la transición es relativa a la hora de inicio de su objeto primario.
-   **dwInterp**: marca que especifica cómo cambia la propiedad del valor anterior al nuevo valor. Con la \_ marca de salto DEXTERF, la propiedad salta inmediatamente al nuevo valor en el momento especificado. Con la \_ marca DEXTERF Interpolate, la propiedad se interpola linealmente desde el valor anterior.

Si establece el miembro **VT** en VT \_ BSTR, el establecedor de propiedad realiza las conversiones necesarias. En el caso de valores de punto flotante, incluya el cero a la izquierda delante de la posición decimal. Por ejemplo, 0,3, no. 3.

> [!Note]  
> Las aplicaciones deben evitar depender de la conversión de **BSTR** s a valores numéricos. Si la propiedad tiene un valor numérico, puede usar el tipo de **variante** numérica adecuado.

 

El valor de una propiedad puede cambiar con el tiempo, por lo que el método [**IPropertySetter:: AddProp**](ipropertysetter-addprop.md) toma una única estructura de [**\_ parámetros de Dexterity**](dexter-param.md) y un puntero a una matriz de estructuras de [**\_ valor de Dexterity**](dexter-value.md) . La matriz define un conjunto de valores basados en el tiempo para la propiedad. Los miembros de la matriz deben estar en orden de tiempo ascendente y el miembro **nvalores** de la estructura del \_ parámetro Dexterity debe ser igual a la longitud de la matriz.

En el ejemplo de código siguiente se crean datos de propiedades para la transición de [borrado de SMPTE](smpte-wipe-transition.md) . Establece el código de borrado en 120, que crea un barrido de óvalo. Establece el tiempo de referencia en cero, lo que indica el inicio de la transición.


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



**Cambiar propiedades dinámicamente**

Después de representar un proyecto de edición de vídeo, es posible modificar las propiedades de un objeto de efecto o transición mientras el gráfico se está ejecutando. Sin embargo, esto solo es posible si establece propiedades en ese objeto antes de que la aplicación llame a [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md). Si es así, puede llamar a [**IAMTimelineObj:: GetPropertySetter**](iamtimelineobj-getpropertysetter.md) en el efecto o la transición, borrar o modificar las propiedades y los cambios se realizarán de forma dinámica a medida que el gráfico se esté ejecutando. Puede haber anomalías visuales mientras se produce el cambio, por lo que solo se recomienda para la vista previa. No cambie las propiedades mientras escribe el proyecto en un archivo.

Si no ha establecido ninguna propiedad en el objeto de efecto o transición antes de llamar a **ConnectFrontEnd**, no podrá agregarle propiedades mientras se esté ejecutando el gráfico.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con efectos y transiciones](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



