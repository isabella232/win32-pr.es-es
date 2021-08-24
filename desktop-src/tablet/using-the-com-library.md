---
description: Información general de la biblioteca COM y notas sobre el uso de las secciones tecnología de pc de tableta del SDK Windows Vista.
ms.assetid: fa43fad9-804c-42d9-9717-6686d5f98ed8
title: Uso de la biblioteca COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdbf986d79011301abe6a9f279a83278fda5dd9e33e3a79335d7d94e6081fb11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119819145"
---
# <a name="using-the-com-library"></a>Uso de la biblioteca COM

La referencia de la biblioteca administrada de Tablet PC ahora se puede encontrar en la sección de referencia Windows la biblioteca de clases del SDK de Vista. Proporciona un modelo de objetos para Microsoft Visual C++. La mayoría de los objetos de la biblioteca COM son idénticos a los que se encuentran en la API administrada de Tablet PC.

Sin embargo, la API COM contiene algunos miembros además de los que se encuentran en la API administrada debido a las diferencias entre el entorno estándar de Microsoft Win32 y el entorno del kit de desarrollo de software (SDK) de Microsoft .NET Framework. Por ejemplo, los objetos InkRectangle y InkTransform se usan en COM, pero FrameworkSDK proporciona una implementación nativa para [**InkRectangle Class**](inkrectangle-class.md) y [**InkTransform Class**](inktransform-class.md) que elimina la necesidad de estos objetos en la API administrada de la plataforma de Tablet PC.

> [!Note]  
> Los objetos de la API COM y los controles de entrada de lápiz no están diseñados para su uso en Active Server Pages (ASP).

 

## <a name="working-with-collections"></a>Trabajar con colecciones

Si pasa un valor **NULL** como índice a cualquiera de los objetos de colección de la biblioteca COM, recibirá el primer elemento de la colección porque estos valores de argumento se coaccionan a 0 cuando se realiza la llamada.

La **\_ propiedad NewEnum** se marca como restringida en la definición del lenguaje de definición de interfaz (IDL) para las interfaces de colección.

En C++, use un bucle para recorrer en iteración una colección obteniendo primero la `For...` longitud de la colección. En el ejemplo siguiente se muestra cómo recorrer en iteración los trazos de un [**objeto InkDisp,**](inkdisp-class.md) `pInk` .


```C++
IInkStrokes* pStrokes;
HRESULT result = pInk->get_Strokes(&pStrokes);
if (SUCCEEDED(result))
{
    // Loop over strokes
    long nStrokes;
    result = pStrokes->get_Count(&nStrokes);
    if (SUCCEEDED(result))
    {
        for (int i =0; i < nStrokes; i++)
        {
            IInkStrokeDisp* pStroke;
            result = pStrokes->Item(i, &pStroke);
            if (SUCCEEDED(result))
            {
              // Code that uses pStroke
              // ...
            }
        }
    }
}
```



## <a name="parameters"></a>Parámetros

Si pasa VT EMPTY o VT NULL como índice a cualquiera de los objetos de colección de la biblioteca COM, recibirá el primer elemento de la colección porque estos valores de argumento se coaccionó a 0 cuando se realiza la \_ \_ llamada.

## <a name="using-idispatch"></a>Uso de IDispatch

Para aumentar el rendimiento, la interfaz de programación de aplicaciones COM (API) de la plataforma de Tablet PC no admite la llamada a con una estructura `IDispatchImpl::Invoke` DIS DISRAMS con argumentos con nombre. Tampoco `IDispatchImpl::GetIDsOfNames` se admite . En su lugar, `Invoke` llame a con los DISPID proporcionados en los encabezados del SDK.

## <a name="waiting-for-events"></a>Esperando eventos

El entorno de Tablet PC es multiproceso. Consulte la documentación com para multiproceso.

## <a name="support-for-aggregation"></a>Compatibilidad con agregación

La agregación solo se ha probado para el control [InkEdit,](inkedit-control-reference.md) el control [InkPicture,](inkpicture-control-reference.md) el [**objeto InkDisp**](inkdisp-class.md) y el [**objeto InkOverlay.**](inkoverlay-class.md) No se ha probado la agregación para otros controles y objetos de la biblioteca.

## <a name="c"></a>C++

El uso del SDK de Tablet PC en C++ requiere el uso de algunos conceptos COM, como VARIANT, SAFEARRAY y BSTR. En esta sección se describe cómo usarlas.

### <a name="variant-and-safearray"></a>VARIANT y SAFEARRAY

La estructura VARIANT se usa para la comunicación entre objetos COM. Básicamente, la estructura VARIANT es un contenedor para una unión grande que contiene muchos tipos de datos.

El valor del primer miembro de la estructura, vt, describe cuál de los miembros de unión es válido. Cuando reciba información en una estructura VARIANT, compruebe el miembro vt para averiguar qué miembro contiene datos válidos. Del mismo modo, cuando envíe información mediante una estructura VARIANT, establezca siempre vt para reflejar el miembro de unión que contiene la información.

Antes de usar la estructura , inicialíclice mediante una llamada a la función COM VariantInit. Cuando termine con la estructura , descálela antes de que la memoria que contiene variant se libera mediante una llamada a VariantClear.

Para obtener más información sobre la estructura VARIANT, vea [VARIANT y VARIANTARG Data Types](/windows/win32/api/oaidl/ns-oaidl-variant).

La estructura SAFEARRAY se proporciona como una manera de trabajar de forma segura con matrices en COM. El campo parray de VARIANT es un puntero a safearray. Use funciones como SafeArrayCreateVector, SafeArrayAccessData y SafeArrayUnaccessData para crear y rellenar una SAFEARRAY en variant.

Para obtener más información sobre el tipo de datos SAFEARRAY, vea [SafeArray Data Type](/windows/win32/api/oaidl/ns-oaidl-safearray).

En este ejemplo de C++ se [**crea un elemento IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , , en un objeto InkDisp, , a partir de una `pInkStrokeDisp` [](inkdisp-class.md) `pInk` matriz de datos de punto.


```C++
VARIANT   var, varPK;
LONG*   plongArray=NULL;
POINT   ptArray[2]={0};
long   lSize=0;
IInkStrokeDisp* pInkStrokeDisp;

IInkDisp*   pInk;   // the object should be created correctly 
                    // elsewhere and assigned here.
HRESULT   hr=E_FAIL;

ptArray[0].x = 20;
ptArray[0].y = 100;
ptArray[1].x = 30;
ptArray[1].y = 110;
lSize = 2;   // two points

VariantInit( &var );
VariantInit( &varPK );
SAFEARRAY* psa = SafeArrayCreateVector( VT_I4, 0, lSize*2 );
if( psa )
{
  if( SUCCEEDED( hr = SafeArrayAccessData( psa, (void**)&plongArray) ))
   {
      for( long i = 0; i < lSize; i++ ) 
      {
         plongArray[2*i] = ptArray[i].x;
         plongArray[2*i+1] = ptArray[i].y;
      }
      hr = SafeArrayUnaccessData( psa );

      if ( SUCCEEDED( hr ) ) 
      {
         var.vt     = VT_ARRAY | VT_I4;
         var.parray = psa;

        // varPK (packet description) is currently reserved, so it is
        // just empty variant for now.
         pInk->CreateStroke( var, varPK, &pInkStrokeDisp );   
      }
   }
}
VariantClear( &var );
VariantClear( &varPK );
```



### <a name="bstr"></a>BSTR

El formato de cadena admitido para COM es BSTR. Un BSTR tiene un puntero a una cadena terminada en cero, pero también contiene la longitud de la cadena (en bytes, sin contar el terminador), que se almacena en los 4 bytes inmediatamente anteriores al primer carácter de la cadena.

Para obtener más información sobre BSTR, vea [Tipo de datos BSTR](/previous-versions/windows/desktop/automat/bstr).

En este ejemplo de C++ se muestra cómo establecer factoid en [**inkRecognizerContext**](inkrecognizercontext-class.md) mediante un BSTR.


```C++
IInkRecognizerContext* pRecognizerContext = NULL;
result = CoCreateInstance(CLSID_InkRecognizerContext, 
    NULL, CLSCTX_INPROC_SERVER,
    IID_IInkRecognizerContext, 
    (void **) &pRecognizerContext);
if SUCCEEDED(result)
{
    BSTR bstrFactoid = SysAllocString(FACTOID_DATE);
    result = pRecognizerContext->put_Factoid(bstrFactoid);
    if SUCCEEDED(result)
    {
      // Use recognizer context...
      // ...
    }
    SysFreeString(bstrFactoid);
}
```



 

 
