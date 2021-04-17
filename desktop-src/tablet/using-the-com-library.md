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
# <a name="using-the-com-library"></a><span data-ttu-id="5b17a-103">Usar la biblioteca COM</span><span class="sxs-lookup"><span data-stu-id="5b17a-103">Using the COM Library</span></span>

<span data-ttu-id="5b17a-104">La referencia de biblioteca administrada de Tablet PC se puede encontrar ahora en la sección referencia de la biblioteca de clases del SDK de Windows Vista normal.</span><span class="sxs-lookup"><span data-stu-id="5b17a-104">The Tablet PC managed library reference can now be found in the regular Windows Vista SDK Class Library reference section.</span></span> <span data-ttu-id="5b17a-105">Proporciona un modelo de objetos para Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="5b17a-105">It provides an object model for Microsoft Visual C++.</span></span> <span data-ttu-id="5b17a-106">La mayoría de los objetos de la biblioteca COM son idénticos a los que se encuentran en la API administrada de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="5b17a-106">The majority of the objects in the COM Library are identical to those found in the Tablet PC Managed API.</span></span>

<span data-ttu-id="5b17a-107">Sin embargo, la API de COM contiene algunos miembros además de los que se encuentran en la API administrada debido a las diferencias entre el entorno estándar de Microsoft Win32 y el Microsoft .NET el entorno del kit de desarrollo de Frameworksoftware (SDK).</span><span class="sxs-lookup"><span data-stu-id="5b17a-107">However, the COM API contains some members in addition to those found in the Managed API because of differences between the standard Microsoft Win32 environment and the Microsoft .NET Frameworksoftware development kit (SDK) environment.</span></span> <span data-ttu-id="5b17a-108">Por ejemplo, los objetos InkRectangle y InkTransform se usan en COM, pero el FrameworkSDK proporciona una implementación nativa para la [**clase InkRectangle**](inkrectangle-class.md) y una [**clase InkTransform**](inktransform-class.md) que elimina la necesidad de estos objetos en la API administrada de la plataforma de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="5b17a-108">For example, the InkRectangle and InkTransform objects are used in COM, but the FrameworkSDK provides native implementation for [**InkRectangle Class**](inkrectangle-class.md) and [**InkTransform Class**](inktransform-class.md) that eliminates the need for these objects in the Tablet PC platform Managed API.</span></span>

> [!Note]  
> <span data-ttu-id="5b17a-109">Los objetos de la API COM y los controles de entrada manuscrita no están diseñados para su uso en páginas Active Server (ASP).</span><span class="sxs-lookup"><span data-stu-id="5b17a-109">The objects in the COM API and the ink controls are not designed for use in Active Server Pages (ASP).</span></span>

 

## <a name="working-with-collections"></a><span data-ttu-id="5b17a-110">Trabajar con colecciones</span><span class="sxs-lookup"><span data-stu-id="5b17a-110">Working with Collections</span></span>

<span data-ttu-id="5b17a-111">Si pasa un valor **null** como índice a cualquiera de los objetos de colección de la biblioteca com, recibirá el primer elemento de la colección porque estos valores de argumento se convierten en 0 cuando se realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="5b17a-111">If you pass in a **NULL** value as the index to any of the collection objects in the COM Library, you receive the first item in the collection because these argument values are coerced to 0 when the call is made.</span></span>

<span data-ttu-id="5b17a-112">La propiedad **\_ NewEnum** se marca como restringida en la definición del lenguaje de definición de interfaz (IDL) para las interfaces de colección.</span><span class="sxs-lookup"><span data-stu-id="5b17a-112">The **\_NewEnum** property is marked restricted in the Interface Definition Language (IDL) definition for the collection interfaces.</span></span>

<span data-ttu-id="5b17a-113">En C++, utilice un `For...` bucle para recorrer en iteración una colección obteniendo primero la longitud de la colección.</span><span class="sxs-lookup"><span data-stu-id="5b17a-113">In C++, use a `For...` loop to iterate through a collection by first obtaining the collection's length.</span></span> <span data-ttu-id="5b17a-114">En el ejemplo siguiente se muestra cómo recorrer en iteración los trazos de un objeto [**InkDisp**](inkdisp-class.md) , `pInk` .</span><span class="sxs-lookup"><span data-stu-id="5b17a-114">The example below shows how to iterate through the strokes of an [**InkDisp**](inkdisp-class.md) object, `pInk`.</span></span>


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



## <a name="parameters"></a><span data-ttu-id="5b17a-115">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5b17a-115">Parameters</span></span>

<span data-ttu-id="5b17a-116">Si pasa VT \_ vacío o VT \_ null como índice a cualquiera de los objetos de colección de la biblioteca com, recibirá el primer elemento de la colección porque estos valores de argumento se convierten en 0 cuando se realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="5b17a-116">If you pass in VT\_EMPTY or VT\_NULL as the index to any of the collection objects in the COM Library, you receive the first item in the collection because these argument values are coerced to 0 when the call is made.</span></span>

## <a name="using-idispatch"></a><span data-ttu-id="5b17a-117">Usar IDispatch</span><span class="sxs-lookup"><span data-stu-id="5b17a-117">Using IDispatch</span></span>

<span data-ttu-id="5b17a-118">Para aumentar el rendimiento, la interfaz de programación de aplicaciones (API) COM de la plataforma de Tablet PC no admite la llamada a `IDispatchImpl::Invoke` con una estructura DISPPARAMS con argumentos con nombre.</span><span class="sxs-lookup"><span data-stu-id="5b17a-118">To increase performance, the Tablet PC Platform COM application programming interface (API) does not support calling `IDispatchImpl::Invoke` with a DISPPARAMS structure with named arguments.</span></span> <span data-ttu-id="5b17a-119">`IDispatchImpl::GetIDsOfNames`Tampoco se admite.</span><span class="sxs-lookup"><span data-stu-id="5b17a-119">The `IDispatchImpl::GetIDsOfNames` is also not supported.</span></span> <span data-ttu-id="5b17a-120">En su lugar, llame a `Invoke` con los DISPID proporcionados en los encabezados del SDK.</span><span class="sxs-lookup"><span data-stu-id="5b17a-120">Instead, call `Invoke` with the DISPIDs supplied in the SDK headers.</span></span>

## <a name="waiting-for-events"></a><span data-ttu-id="5b17a-121">Esperando eventos</span><span class="sxs-lookup"><span data-stu-id="5b17a-121">Waiting for Events</span></span>

<span data-ttu-id="5b17a-122">El entorno de Tablet PC es multiproceso.</span><span class="sxs-lookup"><span data-stu-id="5b17a-122">The Tablet PC environment is multithreaded.</span></span> <span data-ttu-id="5b17a-123">Consulte la documentación de COM para multithreading.</span><span class="sxs-lookup"><span data-stu-id="5b17a-123">Refer to COM documentation for multi-threading.</span></span>

## <a name="support-for-aggregation"></a><span data-ttu-id="5b17a-124">Compatibilidad con la agregación</span><span class="sxs-lookup"><span data-stu-id="5b17a-124">Support for Aggregation</span></span>

<span data-ttu-id="5b17a-125">La agregación se ha probado solo para el control [InkEdit](inkedit-control-reference.md) , el control [InkPicture](inkpicture-control-reference.md) , el objeto [**InkDisp**](inkdisp-class.md) y el objeto [**InkOverlay**](inkoverlay-class.md) .</span><span class="sxs-lookup"><span data-stu-id="5b17a-125">Aggregation has been tested for only the [InkEdit](inkedit-control-reference.md) control, the [InkPicture](inkpicture-control-reference.md) control, the [**InkDisp**](inkdisp-class.md) object, and the [**InkOverlay**](inkoverlay-class.md) object.</span></span> <span data-ttu-id="5b17a-126">No se ha probado la agregación para otros controles y objetos de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="5b17a-126">Aggregation has not been tested for other controls and objects in the library.</span></span>

## <a name="c"></a><span data-ttu-id="5b17a-127">C++</span><span class="sxs-lookup"><span data-stu-id="5b17a-127">C++</span></span>

<span data-ttu-id="5b17a-128">El uso del SDK de Tablet PC en C++ requiere el uso de algunos conceptos de COM, como VARIANT, SAFEARRAY y BSTR.</span><span class="sxs-lookup"><span data-stu-id="5b17a-128">Using the Tablet PC SDK in C++ requires the use of some COM concepts, such as VARIANT, SAFEARRAY, and BSTR.</span></span> <span data-ttu-id="5b17a-129">En esta sección se describe cómo utilizarlos.</span><span class="sxs-lookup"><span data-stu-id="5b17a-129">This section describes how to use them.</span></span>

### <a name="variant-and-safearray"></a><span data-ttu-id="5b17a-130">VARIANT y SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="5b17a-130">VARIANT and SAFEARRAY</span></span>

<span data-ttu-id="5b17a-131">La estructura VARIANT se utiliza para la comunicación entre los objetos COM.</span><span class="sxs-lookup"><span data-stu-id="5b17a-131">The VARIANT structure is used for communication between COM objects.</span></span> <span data-ttu-id="5b17a-132">Esencialmente, la estructura variante es un contenedor para una Unión grande que incluye muchos tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="5b17a-132">Essentially, the VARIANT structure is a container for a large union that carries many types of data.</span></span>

<span data-ttu-id="5b17a-133">El valor del primer miembro de la estructura, VT, describe cuál de los miembros de la Unión es válido.</span><span class="sxs-lookup"><span data-stu-id="5b17a-133">The value in the first member of the structure, vt, describes which of the union members is valid.</span></span> <span data-ttu-id="5b17a-134">Cuando reciba información en una estructura variante, compruebe el miembro VT para averiguar qué miembro contiene datos válidos.</span><span class="sxs-lookup"><span data-stu-id="5b17a-134">When you receive information in a VARIANT structure, check the vt member to find out which member contains valid data.</span></span> <span data-ttu-id="5b17a-135">Del mismo modo, cuando envíe información mediante una estructura VARIANT, establezca siempre VT para reflejar el miembro de Unión que contiene la información.</span><span class="sxs-lookup"><span data-stu-id="5b17a-135">Similarly, when you send information using a VARIANT structure, always set vt to reflect the union member that contains the information.</span></span>

<span data-ttu-id="5b17a-136">Antes de utilizar la estructura, Inicialícelo mediante una llamada a la función COM VariantInit.</span><span class="sxs-lookup"><span data-stu-id="5b17a-136">Before using the structure, initialize it by calling the VariantInit COM function.</span></span> <span data-ttu-id="5b17a-137">Cuando termine con la estructura, desactívela antes de que se libere la memoria que contiene la variante llamando a VariantClear.</span><span class="sxs-lookup"><span data-stu-id="5b17a-137">When finished with the structure, clear it before the memory that contains the VARIANT is freed by calling VariantClear.</span></span>

<span data-ttu-id="5b17a-138">Para obtener más información sobre la estructura VARIANT, vea [tipos de datos Variant y VARIANTARG](/windows/win32/api/oaidl/ns-oaidl-variant).</span><span class="sxs-lookup"><span data-stu-id="5b17a-138">For more information on the VARIANT structure, see [VARIANT and VARIANTARG Data Types](/windows/win32/api/oaidl/ns-oaidl-variant).</span></span>

<span data-ttu-id="5b17a-139">La estructura SAFEARRAY se proporciona como una manera de trabajar con las matrices en COM de forma segura.</span><span class="sxs-lookup"><span data-stu-id="5b17a-139">The SAFEARRAY structure is provided as a way to safely work with arrays in COM.</span></span> <span data-ttu-id="5b17a-140">El campo Parray de la variante es un puntero a un SAFEARRAY.</span><span class="sxs-lookup"><span data-stu-id="5b17a-140">The VARIANT's parray field is a pointer to a SAFEARRAY.</span></span> <span data-ttu-id="5b17a-141">Use funciones como SafeArrayCreateVector, SafeArrayAccessData y SafeArrayUnaccessData para crear y rellenar una SAFEARRAY en una variante.</span><span class="sxs-lookup"><span data-stu-id="5b17a-141">Use functions such as SafeArrayCreateVector, SafeArrayAccessData, and SafeArrayUnaccessData to create and fill a SAFEARRAY in a VARIANT.</span></span>

<span data-ttu-id="5b17a-142">Para obtener más información sobre el tipo de datos SAFEARRAY, vea [SAFEARRAY (tipo de datos](/windows/win32/api/oaidl/ns-oaidl-safearray)).</span><span class="sxs-lookup"><span data-stu-id="5b17a-142">For more information on the SAFEARRAY data type, see [SafeArray Data Type](/windows/win32/api/oaidl/ns-oaidl-safearray).</span></span>

<span data-ttu-id="5b17a-143">En este ejemplo de C++ se crea un [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , `pInkStrokeDisp` , en un objeto [**InkDisp**](inkdisp-class.md) , `pInk` , a partir de una matriz de datos de punto.</span><span class="sxs-lookup"><span data-stu-id="5b17a-143">This C++ example creates an [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , `pInkStrokeDisp`, in an [**InkDisp**](inkdisp-class.md) object, `pInk`, from an array of point data.</span></span>


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



### <a name="bstr"></a><span data-ttu-id="5b17a-144">BSTR</span><span class="sxs-lookup"><span data-stu-id="5b17a-144">BSTR</span></span>

<span data-ttu-id="5b17a-145">El formato de cadena admitido para COM es BSTR.</span><span class="sxs-lookup"><span data-stu-id="5b17a-145">The supported string format for COM is BSTR.</span></span> <span data-ttu-id="5b17a-146">Un BSTR tiene un puntero a una cadena terminada en cero, pero también contiene la longitud de la cadena (en bytes, sin contar el terminador), que se almacena en los 4 bytes inmediatamente antes del primer carácter de la cadena.</span><span class="sxs-lookup"><span data-stu-id="5b17a-146">A BSTR has a pointer to a zero-terminated string, but it also contains the length of the string (in bytes, not counting the terminator), which is stored in the 4 bytes immediately preceding the first character of the string.</span></span>

<span data-ttu-id="5b17a-147">Para obtener más información sobre BSTR, vea [tipo de datos BSTR](/previous-versions/windows/desktop/automat/bstr).</span><span class="sxs-lookup"><span data-stu-id="5b17a-147">For more information on BSTR, see [BSTR Data Type](/previous-versions/windows/desktop/automat/bstr).</span></span>

<span data-ttu-id="5b17a-148">En este ejemplo de C++ se muestra cómo establecer Factoid en un [**InkRecognizerContext**](inkrecognizercontext-class.md) mediante un BSTR.</span><span class="sxs-lookup"><span data-stu-id="5b17a-148">This C++ sample shows how to set the factoid on an [**InkRecognizerContext**](inkrecognizercontext-class.md) using a BSTR.</span></span>


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



 

 
