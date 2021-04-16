---
description: Genera representaciones XML de objetos.
ms.assetid: 06d2b532-7ab2-489d-9021-27b5187c8f2b
ms.tgt_platform: multiple
title: Representar objetos en XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9698c54eeff61517a1389ceea14bc2415727f085
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706094"
---
# <a name="representing-objects-in-xml"></a><span data-ttu-id="fd585-103">Representar objetos en XML</span><span class="sxs-lookup"><span data-stu-id="fd585-103">Representing Objects in XML</span></span>

<span data-ttu-id="fd585-104">El componente de codificador XML en WMI genera representaciones XML de objetos.</span><span class="sxs-lookup"><span data-stu-id="fd585-104">The XML encoder component in WMI generates XML representations of objects.</span></span>

<span data-ttu-id="fd585-105">En C++, puede iniciar el codificador XML con una llamada al método [**IWbemObjectTextSrc. gettext**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) , especificando el objeto que se va a representar en XML y el formato de texto que se va a usar en la representación.</span><span class="sxs-lookup"><span data-stu-id="fd585-105">In C++, you can start the XML encoder with a call to the [**IWbemObjectTextSrc.GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) method, specifying the object to be represented in XML and the text format to use in the representation.</span></span> <span data-ttu-id="fd585-106">Para obtener más información y un ejemplo de código, vea para codificar un objeto en XML con C/C++.</span><span class="sxs-lookup"><span data-stu-id="fd585-106">For more information and a code example, see To encode an object in XML using C/C++.</span></span>

<span data-ttu-id="fd585-107">En VBScript o Visual Basic, para codificar los datos de una instancia XML, llame a [**SWbemObjectEx. gettext**](swbemobjectex-gettext-.md).</span><span class="sxs-lookup"><span data-stu-id="fd585-107">In VBScript or Visual Basic, to encode data for an XML instance, call [**SWbemObjectEx.GetText**](swbemobjectex-gettext-.md).</span></span> <span data-ttu-id="fd585-108">Para obtener más información y un ejemplo de código, vea para codificar un objeto en XML con VBScript.</span><span class="sxs-lookup"><span data-stu-id="fd585-108">For more information and a code example, see To encode an object in XML using VBScript.</span></span>

<span data-ttu-id="fd585-109">En este tema se describen las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="fd585-109">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="fd585-110">Codificar un objeto mediante C o C++</span><span class="sxs-lookup"><span data-stu-id="fd585-110">Encode an Object Using C or C++</span></span>](#encode-an-object-using-c-or-c)
-   [<span data-ttu-id="fd585-111">Codificar un objeto mediante VBScript</span><span class="sxs-lookup"><span data-stu-id="fd585-111">Encode an Object Using VBScript</span></span>](#encode-an-object-using-vbscript)
-   [<span data-ttu-id="fd585-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fd585-112">Related topics</span></span>](#related-topics)

## <a name="encode-an-object-using-c-or-c"></a><span data-ttu-id="fd585-113">Codificar un objeto mediante C o C++</span><span class="sxs-lookup"><span data-stu-id="fd585-113">Encode an Object Using C or C++</span></span>

<span id="to_encode_an_object_in_xml_using_c_c_"></span><span id="TO_ENCODE_AN_OBJECT_IN_XML_USING_C_C_"></span>

<span data-ttu-id="fd585-114">En el procedimiento siguiente se describe cómo codificar un objeto en XML mediante C o C++.</span><span class="sxs-lookup"><span data-stu-id="fd585-114">The following procedure describes how to encode an object in XML using C or C++.</span></span>

<span data-ttu-id="fd585-115">**Para codificar un objeto en XML mediante C o C++**</span><span class="sxs-lookup"><span data-stu-id="fd585-115">**To encode an object in XML using C or C++**</span></span>

1.  <span data-ttu-id="fd585-116">Configure el programa para obtener acceso a los datos de WMI.</span><span class="sxs-lookup"><span data-stu-id="fd585-116">Set up your program to access WMI data.</span></span>

    <span data-ttu-id="fd585-117">Dado que WMI se basa en la tecnología COM, debe realizar las llamadas necesarias a las funciones [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) y [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para tener acceso a WMI.</span><span class="sxs-lookup"><span data-stu-id="fd585-117">Because WMI is based on COM technology, you must perform the requisite calls to the [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) functions to access WMI.</span></span> <span data-ttu-id="fd585-118">Para obtener más información, vea [inicializar com para una aplicación WMI](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="fd585-118">For more information, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

2.  <span data-ttu-id="fd585-119">Opcionalmente, cree un objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) e inicialícela.</span><span class="sxs-lookup"><span data-stu-id="fd585-119">Optionally, create an [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object and initialize it.</span></span>

    <span data-ttu-id="fd585-120">No es necesario crear el objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) a menos que necesite cambiar la operación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="fd585-120">You do not need to create the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object unless you need to change the default operation.</span></span> <span data-ttu-id="fd585-121">El codificador XML utiliza el objeto de contexto para controlar la cantidad de información que se incluye en la representación XML del objeto.</span><span class="sxs-lookup"><span data-stu-id="fd585-121">The context object is used by the XML encoder to control the amount of information included in the object's XML representation.</span></span>

    <span data-ttu-id="fd585-122">En la tabla siguiente se enumeran los valores opcionales que se pueden especificar para el objeto de contexto.</span><span class="sxs-lookup"><span data-stu-id="fd585-122">The following table lists the optional values that can be specified for the context object.</span></span>

    

    <table>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="fd585-123">Valor/tipo</span><span class="sxs-lookup"><span data-stu-id="fd585-123">Value/type</span></span></th>
    <th><span data-ttu-id="fd585-124">Significado</span><span class="sxs-lookup"><span data-stu-id="fd585-124">Meaning</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="fd585-125">&quot;LocalOnly &quot; <strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="fd585-125">&quot;LocalOnly&quot; <strong>VT_BOOL</strong></span></span></td>
    <td><span data-ttu-id="fd585-126">Cuando <strong>es true</strong>, solo las propiedades y los métodos definidos localmente en la clase están presentes en el XML resultante.</span><span class="sxs-lookup"><span data-stu-id="fd585-126">When <strong>TRUE</strong>, only properties and methods defined locally in the class are present in the resulting XML.</span></span> <span data-ttu-id="fd585-127">El valor predeterminado es <strong>FALSE</strong>.</span><span class="sxs-lookup"><span data-stu-id="fd585-127">The default value is <strong>FALSE</strong>.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="fd585-128">&quot;&quot; <strong>VT_BOOL</strong> IncludeQualifiers</span><span class="sxs-lookup"><span data-stu-id="fd585-128">&quot;IncludeQualifiers&quot; <strong>VT_BOOL</strong></span></span></td>
    <td><span data-ttu-id="fd585-129">Cuando <strong>es true</strong>, la clase, la instancia, las propiedades y los calificadores de método se incluyen en el XML resultante.</span><span class="sxs-lookup"><span data-stu-id="fd585-129">When <strong>TRUE</strong>, class, instance, properties, and method qualifiers are included in the resulting XML.</span></span> <span data-ttu-id="fd585-130">El valor predeterminado es <strong>FALSE</strong>.</span><span class="sxs-lookup"><span data-stu-id="fd585-130">The default value is <strong>FALSE</strong>.</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="fd585-131">&quot;&quot; <strong>VT_BOOL</strong> ExcludeSystemProperties</span><span class="sxs-lookup"><span data-stu-id="fd585-131">&quot;ExcludeSystemProperties&quot; <strong>VT_BOOL</strong></span></span></td>
    <td><span data-ttu-id="fd585-132">Si <strong>es true</strong>, las propiedades del sistema WMI se filtran de la salida.</span><span class="sxs-lookup"><span data-stu-id="fd585-132">When <strong>TRUE</strong>, WMI system properties are filtered out of the output.</span></span> <span data-ttu-id="fd585-133">El valor predeterminado es <strong>FALSE</strong>.</span><span class="sxs-lookup"><span data-stu-id="fd585-133">The default value is <strong>FALSE</strong>.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="fd585-134">&quot;&quot; <strong>VT_I4</strong> PathLevel</span><span class="sxs-lookup"><span data-stu-id="fd585-134">&quot;PathLevel&quot; <strong>VT_I4</strong></span></span></td>
    <td><dl> <span data-ttu-id="fd585-135">0 = <CLASS> <INSTANCE> se genera un elemento o.</span><span class="sxs-lookup"><span data-stu-id="fd585-135">0 = A <CLASS> or <INSTANCE> element is generated.</span></span><br />
<span data-ttu-id="fd585-136">1 = <VALUE.NAMEDOBJECT> se genera un elemento.</span><span class="sxs-lookup"><span data-stu-id="fd585-136">1 = A <VALUE.NAMEDOBJECT> element is generated.</span></span><br />
<span data-ttu-id="fd585-137">2 = <VALUE.OBJECTWITHLOCALPATH> se genera un elemento.</span><span class="sxs-lookup"><span data-stu-id="fd585-137">2 = A <VALUE.OBJECTWITHLOCALPATH> element is generated.</span></span><br />
<span data-ttu-id="fd585-138">3 = <VALUE.OBJECTWITHPATH> se genera un.</span><span class="sxs-lookup"><span data-stu-id="fd585-138">3 = A <VALUE.OBJECTWITHPATH> is generated.</span></span><br />
    </dl> <span data-ttu-id="fd585-139">El valor predeterminado es cero (0).</span><span class="sxs-lookup"><span data-stu-id="fd585-139">The default is 0 (zero).</span></span><br/></td>
    </tr>
    </tbody>
    </table>

    

     

    <span data-ttu-id="fd585-140">En el ejemplo de código siguiente se muestra cómo se inicializa el objeto de contexto para incluir los calificadores y excluir las propiedades del sistema.</span><span class="sxs-lookup"><span data-stu-id="fd585-140">The following code example shows how the context object is initialized to include qualifiers and exclude system properties.</span></span>

    ```C++
    VARIANT vValue;
    IWbemContext *pContext = NULL;
    HRESULT hr = CoCreateInstance (CLSID_WbemContext, 
                           NULL, 
                           CLSCTX_INPROC_SERVER,
                           IID_IWbemContext, 
                           (void**) &pContext);
    if (FAILED(hr))
    {
      printf("Create context failed with %x\n", hr);
      return hr;
    }

    // Generate a <VALUE.OBJECTWITHLOCALPATH> element
    VariantInit(&vValue);
    vValue.vt = VT_I4;
    vValue.lVal = 2;
    pContext->SetValue(L"PathLevel", 0, &vValue);
    VariantClear(&vValue);

    // Include qualifiers
    VariantInit(&vValue);
    vValue.vt = VT_BOOL;
    vValue.boolVal = VARIANT_TRUE;
    pContext->SetValue(L"IncludeQualifiers", 0, &vValue);
    VariantClear(&vValue);

    // Exclude system properties
    VariantInit(&vValue);
    vValue.vt = VT_BOOL;
    vValue.boolVal = VARIANT_TRUE;
    pContext->SetValue(L"ExcludeSystemProperties", 0, &vValue);
    VariantClear(&vValue);
    ```

    

3.  <span data-ttu-id="fd585-141">Obtenga una referencia a la clase o instancia para codificar en XML.</span><span class="sxs-lookup"><span data-stu-id="fd585-141">Get a reference to the class or instance to encode in XML.</span></span>

    <span data-ttu-id="fd585-142">Después de inicializar COM y estar conectado a WMI, llame a [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) para recuperar una referencia a la clase o instancia especificada.</span><span class="sxs-lookup"><span data-stu-id="fd585-142">After you have initialized COM and are connected to WMI, call [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) to retrieve a reference to the specified class or instance.</span></span> <span data-ttu-id="fd585-143">Si usó un BSTR para especificar la clase o la instancia, llame a [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar la memoria asignada por [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring).</span><span class="sxs-lookup"><span data-stu-id="fd585-143">If you used a BSTR to specify the class or instance, call [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free up the memory allocated by [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring).</span></span>

    <span data-ttu-id="fd585-144">En el ejemplo de código siguiente se recupera una referencia a una instancia de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="fd585-144">The following code example retrieves a reference to an [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) instance.</span></span>

    ```C++
    HRESULT hr = NULL;
    IWbemClassObject *pClass = NULL;
    BSTR strObj = SysAllocString(L"Win32_LogicalDisk");

    hr = pConnection->GetObject(strObj, 
                                0, 
                                NULL, 
                                &pClass, 
                                NULL);

    SysFreeString(strObj);
    if (FAILED(hr))
    {
      printf("GetObject failed with %x\n",hr)
      return hr;
    }
    ```

    

4.  <span data-ttu-id="fd585-145">Cree un objeto [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) .</span><span class="sxs-lookup"><span data-stu-id="fd585-145">Create an [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) object.</span></span>

    <span data-ttu-id="fd585-146">Una vez que tenga una referencia a un objeto, debe crear el objeto [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) con una llamada a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="fd585-146">After you have a reference to an object you must create the [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) object with a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="fd585-147">El objeto **IWbemObjectTextSrc** se usa para generar el texto XML real.</span><span class="sxs-lookup"><span data-stu-id="fd585-147">The **IWbemObjectTextSrc** object is used to generate the actual XML text.</span></span>

    <span data-ttu-id="fd585-148">En el ejemplo de código siguiente se muestra cómo crear un objeto [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) llamando a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="fd585-148">The following code example shows how to create an [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) object by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    ```C++
    HRESULT hr = NULL;
    IWbemObjectTextSrc *pSrc = NULL;

    hr = CoCreateInstance (CLSID_WbemObjectTextSrc, 
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_IWbemObjectTextSrc, 
                           (void**) &pSrc);

    if (FAILED(hr))
    {
        printf("CoCreateInstance of IWbemObjectTextSrc failed %x\n",hr);
        return hr;
    }
    ```

    

5.  <span data-ttu-id="fd585-149">Invoque el método [**IWbemObjectTextSrc. gettext**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) para obtener una representación XML de un objeto.</span><span class="sxs-lookup"><span data-stu-id="fd585-149">Invoke the [**IWbemObjectTextSrc.GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) method to get an XML representation of an object.</span></span>

    <span data-ttu-id="fd585-150">Después de establecer el contexto para la representación del objeto, obtener una referencia al objeto y crear un objeto [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) , está listo para generar una representación XML del objeto especificado llamando al método [**IWbemObjectTextSrc. gettext**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) .</span><span class="sxs-lookup"><span data-stu-id="fd585-150">After setting the context for the object's representation, getting a reference to the object, and creating an [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) object, you are ready to generate an XML representation of the specified object by calling the [**IWbemObjectTextSrc.GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) method.</span></span>

    <span data-ttu-id="fd585-151">En el siguiente código de ejemplo de C++ se genera una representación XML del objeto al que hace referencia *pClass*.</span><span class="sxs-lookup"><span data-stu-id="fd585-151">The following C++ example code generates an XML representation of the object referenced by *pClass*.</span></span> <span data-ttu-id="fd585-152">La representación XML se devuelve en *strText*.</span><span class="sxs-lookup"><span data-stu-id="fd585-152">The XML representation is returned in *strText*.</span></span> <span data-ttu-id="fd585-153">El tercer parámetro de [**gettext**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) especifica el formato de texto que se va a usar para el XML y debe ser texto de tipo CIM de WMI \_ \_ \_ \_ DTD \_ 2 \_ 0 (0x1) o \_ texto de obj WMI \_ \_ \_ DTD \_ 2 \_ 0 (0X2).</span><span class="sxs-lookup"><span data-stu-id="fd585-153">The third parameter of [**GetText**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) specifies the text format to be used for the XML and must be either WMI\_OBJ\_TEXT\_CIM\_DTD\_2\_0 (0x1) or WMI\_OBJ\_TEXT\_WMI\_DTD\_2\_0 (0x2).</span></span> <span data-ttu-id="fd585-154">Para obtener más información sobre estos valores, vea valores de los parámetros [**IWbemObjectTextSrc:: gettext**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) .</span><span class="sxs-lookup"><span data-stu-id="fd585-154">For more information about these values, see [**IWbemObjectTextSrc::GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) Parameter Values.</span></span>

    ```C++
    HRESULT hr = NULL;
    BSTR strText = NULL;
    hr = pSrc->GetText(0, 
                       pClass, 
                       WMI_OBJ_TEXT_CIM_DTD_2_0,
                       pContext, 
                       &strText);

    // Perform a task with strText
    SysFreeString(strText);

    if (FAILED(hr))
    {
      printf("GetText failed with %x\n", hr);
      return hr;
    }
    ```

    

<span data-ttu-id="fd585-155">En el siguiente código de ejemplo de C++ se incluyen todos los pasos del procedimiento anterior y se codifica la clase [**Win32 \_ LOGICALDISK**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) en XML, incluidos los calificadores de clase, propiedad y método, y se excluyen las propiedades del sistema.</span><span class="sxs-lookup"><span data-stu-id="fd585-155">The following C++ example code includes all of the steps in the previous procedure and encodes the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class in XML including class, property, and method qualifiers and excluding system properties.</span></span>


```C++
// The following #define statement is needed so that 
// the proper values are loaded by the #include files.
#define _WIN32_WINNT 0x0500

#include <stdio.h>
#include <wbemcli.h>
#pragma comment(lib, "wbemuuid.lib")

// Initialize the context object
// ---------------------------------------------
void FillUpContext(IWbemContext *pContext)
{
  VARIANT vValue;

  // IncludeQualifiers
  VariantInit(&vValue);
  vValue.vt = VT_BOOL;
  vValue.boolVal = VARIANT_FALSE;
  pContext->SetValue(L"IncludeQualifiers", 0, &vValue);
  VariantClear(&vValue);

  VariantInit(&vValue);
  vValue.vt = VT_I4;
  vValue.lVal = 0;
  pContext->SetValue(L"PathLevel", 0, &vValue);
  VariantClear(&vValue);

  // ExcludeSystemProperties
  VariantInit(&vValue);
  vValue.vt = VT_BOOL;
  vValue.boolVal = VARIANT_TRUE;
  pContext->SetValue(L"ExcludeSystemProperties", 0, &vValue);
  VariantClear(&vValue);
}

// Main method ... drives the program
// ---------------------------------------------
int _cdecl main(int argc, char * argv[])
{
  BSTR strNs = NULL;
  BSTR strObj = NULL;
  BSTR strText = NULL;

  if(FAILED(CoInitialize(NULL)))
    return 1;
  HRESULT hr = E_FAIL;
  IWbemObjectTextSrc *pSrc = NULL;

  IWbemLocator *pL = NULL;
  if(SUCCEEDED(hr = CoCreateInstance (CLSID_WbemLocator, 
                                      NULL, 
                                      CLSCTX_INPROC_SERVER,
                                      IID_IWbemLocator, 
                                      (void**) &pL)))
  {
    // Create a context object
    IWbemContext *pContext = NULL;
    if(SUCCEEDED(hr = CoCreateInstance (CLSID_WbemContext, 
                                        NULL, 
                                        CLSCTX_INPROC_SERVER,
                                        IID_IWbemContext, 
                                        (void**) &pContext)))
    {
      FillUpContext(pContext);
      IWbemServices *pConnection = NULL;
      strNs = SysAllocString(L"root\\cimv2");
      strText = NULL;
      if(SUCCEEDED(hr = pL->ConnectServer(strNs, 
                                          NULL, 
                                          NULL, 
                                          NULL, 
                                          0, 
                                          NULL, 
                                          NULL, 
                                          &pConnection)))
      {
        IWbemClassObject *pClass = NULL;
        strObj = SysAllocString(L"Win32_LogicalDisk");

        if(SUCCEEDED(hr = CoCreateInstance (CLSID_WbemObjectTextSrc, 
                                            NULL,
                                            CLSCTX_INPROC_SERVER,
                                            IID_IWbemObjectTextSrc, 
                                            (void**) &pSrc)))
        {
          // Test for GetObject
          if(SUCCEEDED(hr = pConnection->GetObject(strObj, 
                                                   0, 
                                                   NULL, 
                                                   &pClass, 
                                                   NULL)))
          {
            if(SUCCEEDED(hr = pSrc->GetText(0, 
                                            pClass, 
                                            WMI_OBJ_TEXT_CIM_DTD_2_0,
                                            pContext, 
                                            &strText)))
            {
              printf("GETOBJECT SUCCEEDED\n");
              printf("==========================================\n");
              wprintf(strText);
              pContext->Release();
              pClass->Release();
            }
            else
            {
              printf("GetText failed with %x\n", hr);
              // Free up the object
              pContext->Release();
              pClass->Release();
            }
          }
          else
            printf("GetObject failed with %x\n", hr);
        }
        else
          printf("CoCreateInstance on WbemObjectTextSrc failed with %x\n", hr);
      }
      else
        printf("ConnectServer on root\\cimv2 failed with %x\n", hr);
    }
    else
      printf("CoCreateInstance on Context failed with %x\n", hr);
  }
  else
    printf("CoCreateInstance on Locator failed with %x\n", hr);

// Clean up memory
  if (strNs != NULL)
    SysFreeString(strNs);
  if (strObj != NULL)
    SysFreeString(strObj);
  if (strText != NULL)
    SysFreeString(strText);
  if (pSrc != NULL)
    pSrc->Release();
  if (pL != NULL)
    pL->Release();
  return 0;
}
```



## <a name="encode-an-object-using-vbscript"></a><span data-ttu-id="fd585-156">Codificar un objeto mediante VBScript</span><span class="sxs-lookup"><span data-stu-id="fd585-156">Encode an Object Using VBScript</span></span>

<span id="to_encode_an_object_in_xml_using_vbscript"></span><span id="TO_ENCODE_AN_OBJECT_IN_XML_USING_VBSCRIPT"></span>

<span data-ttu-id="fd585-157">En el procedimiento siguiente se describe cómo codificar un objeto en XML con VBScript.</span><span class="sxs-lookup"><span data-stu-id="fd585-157">The following procedure describes how to encode an object in XML using VBScript.</span></span>

<span data-ttu-id="fd585-158">**Para codificar un objeto en XML mediante VBScript**</span><span class="sxs-lookup"><span data-stu-id="fd585-158">**To encode an object in XML using VBScript**</span></span>

1.  <span data-ttu-id="fd585-159">Opcionalmente, cree un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) e Inicialícelo para establecer los valores de contexto necesarios para la representación XML.</span><span class="sxs-lookup"><span data-stu-id="fd585-159">Optionally, create an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object and initialize it so as to set the context values required for the XML representation.</span></span>

    <span data-ttu-id="fd585-160">En el ejemplo de código siguiente se muestra cómo los valores indican al codificador XML que genere un valor de <. OBJECTWITHLOCALPATH> elemento, incluidos todos los calificadores y excluidas las propiedades del sistema al construir la representación XML del objeto.</span><span class="sxs-lookup"><span data-stu-id="fd585-160">The following code example shows how the values instruct the XML encoder to generate a <VALUE.OBJECTWITHLOCALPATH> element, including all of the qualifiers and excluding system properties when it constructs the XML representation of the object.</span></span>

    ```VB
    ' Create an optional SWbemNamedValueSet object
    set context = CreateObject("wbemscripting.SWbemNamedValueSet")

    ' Initialize the value set object to set the context
    ' Generate a <VALUE.OBJECTWITHLOCALPATH> element
    context.add "PathLevel", 2 
    context.add "IncludeQualifiers", true 
    context.add "ExcludeSystemProperties", true '
    ```

    

2.  <span data-ttu-id="fd585-161">Recupera una instancia del objeto o la clase que se va a representar en XML.</span><span class="sxs-lookup"><span data-stu-id="fd585-161">Retrieve an instance of the object or class to represent in XML.</span></span>

    <span data-ttu-id="fd585-162">En el ejemplo de código siguiente se recupera una instancia del objeto.</span><span class="sxs-lookup"><span data-stu-id="fd585-162">The following code example retrieves an instance of the object.</span></span>

    ```VB
    ' Retrieve the object/class to be represented in XML
    set myObj = GetObject("winmgmts:\\.\root\cimv2:win32_LogicalDisk")
    ```

    

3.  <span data-ttu-id="fd585-163">Invoque el método [**gettext \_**](swbemobjectex-gettext-.md) de la instancia creada en el paso anterior, usando 1 como parámetro para especificar el formato de texto que corresponde a CIM DTD versión 2,0 o 2 para especificar el formato de texto que corresponde a la DTD de WMI versión 2,0.</span><span class="sxs-lookup"><span data-stu-id="fd585-163">Invoke the [**GetText\_**](swbemobjectex-gettext-.md) method of the instance created in the preceding step, using 1 as the parameter to specify the text format that corresponds to CIM DTD version 2.0, or 2 to specify the text format that corresponds to WMI DTD version 2.0.</span></span> <span data-ttu-id="fd585-164">Si creó el objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) en el paso 1, inclúyalo en la lista de parámetros como tercer parámetro.</span><span class="sxs-lookup"><span data-stu-id="fd585-164">If you created the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object in Step 1, include it in the parameter list as the third parameter.</span></span>

    <span data-ttu-id="fd585-165">En el ejemplo de código siguiente se muestra cómo invocar el método [**gettext \_**](swbemobjectex-gettext-.md) de la instancia.</span><span class="sxs-lookup"><span data-stu-id="fd585-165">The following code example shows how to invoke the [**GetText\_**](swbemobjectex-gettext-.md) method of the instance.</span></span>

    ```VB
    ' Get the XML representation of the object
    strText = myObj.GetText_(2,,context)

    ' If you have not used a SWbemNamedValueSet object
    ' enter the following line.
    strText = myObj.GetText_(2)
    ```

    

4.  <span data-ttu-id="fd585-166">Opcionalmente, valide que el XML generado en el paso 3 sea XML con formato correcto, creando e inicializando un objeto de Document Object Model XML (DOM) y, a continuación, cargue el texto XML en él.</span><span class="sxs-lookup"><span data-stu-id="fd585-166">Optionally, validate that the XML generated in Step 3 is well-formed XML, by creating and initializing an XML Document Object Model (DOM) object and then load the XML text into it.</span></span>

    <span data-ttu-id="fd585-167">En el ejemplo de código siguiente se muestra cómo crear e inicializar un objeto DOM XML y cargar en él el texto XML.</span><span class="sxs-lookup"><span data-stu-id="fd585-167">The following code example shows how to create and initialize an XML DOM object and load the XML text into it.</span></span>

    ```VB
    ' Create an XMLDOM object
    set xml = CreateObject("Microsoft.xmldom")

    ' Initialize the XMLDOM object so results are returned synchronously
    xml.async = false

    ' Load the XML into the XMLDOM object
    xml.loadxml strText
    ```

    

5.  <span data-ttu-id="fd585-168">Genera la representación XML del objeto.</span><span class="sxs-lookup"><span data-stu-id="fd585-168">Output the XML representation of the object.</span></span>

    <span data-ttu-id="fd585-169">En el ejemplo de código siguiente se muestra cómo usar Wscript para generar el XML.</span><span class="sxs-lookup"><span data-stu-id="fd585-169">The following code example shows how to use wscript to output the XML.</span></span>

    ```VB
    wscript.echo strText
    ```

    

    <span data-ttu-id="fd585-170">Si decide usar DOM XML para comprobar que el XML generado está bien formado, reemplace la línea anterior por lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="fd585-170">If you chose to use XML DOM to verify that the XML generated is well-formed, replace the previous line with the following.</span></span>

    ```VB
    wscript.echo xml.xml
    ```

    

<span data-ttu-id="fd585-171">El siguiente ejemplo de código de VBScript incluye todos los pasos del procedimiento anterior y codifica la clase [**Win32 \_ LOGICALDISK**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) en XML, incluidos los calificadores de clase, propiedad y método, y excluyendo las propiedades del sistema.</span><span class="sxs-lookup"><span data-stu-id="fd585-171">The following VBScript code example includes all of the steps in the preceding procedure and encodes the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class in XML, including class, property, and method qualifiers and excluding system properties.</span></span>


```VB
' Create optional SWbemNamedValueSet object
set context = CreateObject("Wbemscripting.SWbemNamedValueSet")

' Initialize the context object
context.add "PathLevel", 2
context.add "IncludeQualifiers", true
context.add "ExcludeSystemProperties", true

' Retrieve the object/class to be represented in XML
set myObj = GetObject("winmgmts:\\.\root\cimv2:Win32_LogicalDisk")

' Get the XML representation of the object
strText = myObj.GetText_(2,,context)
' If you have not used a SWbemNamedValueSet object 
'   use the following line
'   strText = myObj.GetText(2)

' Print the XML representation
wscript.echo strText

' If you choose to use the XML DOM to verify 
'   that the XML generated is well-formed, replace the last
'   line in the above code example with the following lines:

' Create an XMLDOM object
set xml = CreateObject("Microsoft.xmldom")

' Initialize the XMLDOM object so results are 
'   returned synchronously
xml.async = false

' Load the XML into the XMLDOM object
xml.loadxml strText

' Print the XML representation
wscript.echo xml.xml
```



## <a name="related-topics"></a><span data-ttu-id="fd585-172">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fd585-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd585-173">Usar WMI</span><span class="sxs-lookup"><span data-stu-id="fd585-173">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

