---
description: Información general de la biblioteca COM y notas sobre el uso de las secciones de tecnología de Tablet PC del SDK de Windows Vista.
ms.assetid: fa43fad9-804c-42d9-9717-6686d5f98ed8
title: Usar la biblioteca COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d82671b198114cf45b334e8c4e07146a91964e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360255"
---
# <a name="using-the-com-library"></a>Usar la biblioteca COM

La referencia de biblioteca administrada de Tablet PC se puede encontrar ahora en la sección referencia de la biblioteca de clases del SDK de Windows Vista normal. Proporciona un modelo de objetos para Microsoft Visual C++. La mayoría de los objetos de la biblioteca COM son idénticos a los que se encuentran en la API administrada de Tablet PC.

Sin embargo, la API de COM contiene algunos miembros además de los que se encuentran en la API administrada debido a las diferencias entre el entorno estándar de Microsoft Win32 y el Microsoft .NET el entorno del kit de desarrollo de Frameworksoftware (SDK). Por ejemplo, los objetos InkRectangle y InkTransform se usan en COM, pero el FrameworkSDK proporciona una implementación nativa para la [**clase InkRectangle**](inkrectangle-class.md) y una [**clase InkTransform**](inktransform-class.md) que elimina la necesidad de estos objetos en la API administrada de la plataforma de Tablet PC.

> [!Note]  
> Los objetos de la API COM y los controles de entrada manuscrita no están diseñados para su uso en páginas Active Server (ASP).

 

## <a name="working-with-collections"></a>Trabajar con colecciones

Si pasa un valor **null** como índice a cualquiera de los objetos de colección de la biblioteca com, recibirá el primer elemento de la colección porque estos valores de argumento se convierten en 0 cuando se realiza la llamada.

La propiedad **\_ NewEnum** se marca como restringida en la definición del lenguaje de definición de interfaz (IDL) para las interfaces de colección.

En C++, utilice un `For...` bucle para recorrer en iteración una colección obteniendo primero la longitud de la colección. En el ejemplo siguiente se muestra cómo recorrer en iteración los trazos de un objeto [**InkDisp**](inkdisp-class.md) , `pInk` .


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

Si pasa VT \_ vacío o VT \_ null como índice a cualquiera de los objetos de colección de la biblioteca com, recibirá el primer elemento de la colección porque estos valores de argumento se convierten en 0 cuando se realiza la llamada.

## <a name="using-idispatch"></a>Usar IDispatch

Para aumentar el rendimiento, la interfaz de programación de aplicaciones (API) COM de la plataforma de Tablet PC no admite la llamada a `IDispatchImpl::Invoke` con una estructura DISPPARAMS con argumentos con nombre. `IDispatchImpl::GetIDsOfNames`Tampoco se admite. En su lugar, llame a `Invoke` con los DISPID proporcionados en los encabezados del SDK.

## <a name="waiting-for-events"></a>Esperando eventos

El entorno de Tablet PC es multiproceso. Consulte la documentación de COM para multithreading.

## <a name="support-for-aggregation"></a>Compatibilidad con la agregación

La agregación se ha probado solo para el control [InkEdit](inkedit-control-reference.md) , el control [InkPicture](inkpicture-control-reference.md) , el objeto [**InkDisp**](inkdisp-class.md) y el objeto [**InkOverlay**](inkoverlay-class.md) . No se ha probado la agregación para otros controles y objetos de la biblioteca.

## <a name="c"></a>C++

El uso del SDK de Tablet PC en C++ requiere el uso de algunos conceptos de COM, como VARIANT, SAFEARRAY y BSTR. En esta sección se describe cómo utilizarlos.

### <a name="variant-and-safearray"></a>VARIANT y SAFEARRAY

La estructura VARIANT se utiliza para la comunicación entre los objetos COM. Esencialmente, la estructura variante es un contenedor para una Unión grande que incluye muchos tipos de datos.

El valor del primer miembro de la estructura, VT, describe cuál de los miembros de la Unión es válido. Cuando reciba información en una estructura variante, compruebe el miembro VT para averiguar qué miembro contiene datos válidos. Del mismo modo, cuando envíe información mediante una estructura VARIANT, establezca siempre VT para reflejar el miembro de Unión que contiene la información.

Antes de utilizar la estructura, Inicialícelo mediante una llamada a la función COM VariantInit. Cuando termine con la estructura, desactívela antes de que se libere la memoria que contiene la variante llamando a VariantClear.

Para obtener más información sobre la estructura VARIANT, vea [tipos de datos Variant y VARIANTARG](/windows/win32/api/oaidl/ns-oaidl-variant).

La estructura SAFEARRAY se proporciona como una manera de trabajar con las matrices en COM de forma segura. El campo Parray de la variante es un puntero a un SAFEARRAY. Use funciones como SafeArrayCreateVector, SafeArrayAccessData y SafeArrayUnaccessData para crear y rellenar una SAFEARRAY en una variante.

Para obtener más información sobre el tipo de datos SAFEARRAY, vea [SAFEARRAY (tipo de datos](/windows/win32/api/oaidl/ns-oaidl-safearray)).

En este ejemplo de C++ se crea un [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , `pInkStrokeDisp` , en un objeto [**InkDisp**](inkdisp-class.md) , `pInk` , a partir de una matriz de datos de punto.


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

El formato de cadena admitido para COM es BSTR. Un BSTR tiene un puntero a una cadena terminada en cero, pero también contiene la longitud de la cadena (en bytes, sin contar el terminador), que se almacena en los 4 bytes inmediatamente antes del primer carácter de la cadena.

Para obtener más información sobre BSTR, vea [tipo de datos BSTR](/previous-versions/windows/desktop/automat/bstr).

En este ejemplo de C++ se muestra cómo establecer Factoid en un [**InkRecognizerContext**](inkrecognizercontext-class.md) mediante un BSTR.


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



 

 
