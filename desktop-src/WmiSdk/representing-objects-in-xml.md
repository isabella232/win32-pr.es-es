---
description: Genera representaciones XML de objetos .
ms.assetid: 06d2b532-7ab2-489d-9021-27b5187c8f2b
ms.tgt_platform: multiple
title: Representar objetos en XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68bcbc47a0e5466b69775b4ff9a6c09ce20bae6f
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879652"
---
# <a name="representing-objects-in-xml"></a>Representar objetos en XML

El componente del codificador XML de WMI genera representaciones XML de objetos.

En C++, puede iniciar el codificador XML con una llamada al método [**IWbemObjectTextSrc.GetText,**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) especificando el objeto que se representará en XML y el formato de texto que se usará en la representación. Para obtener más información y un ejemplo de código, vea Para codificar un objeto en XML mediante C/C++.

En VBScript o Visual Basic, para codificar datos para una instancia XML, llame a [**SWbemObjectEx.GetText**](swbemobjectex-gettext-.md). Para obtener más información y un ejemplo de código, vea Para codificar un objeto en XML mediante VBScript.

En este tema se de abordan las secciones siguientes:

-   [Codificación de un objeto mediante C o C++](#encode-an-object-using-c-or-c)
-   [Codificación de un objeto mediante VBScript](#encode-an-object-using-vbscript)
-   [Temas relacionados](#related-topics)

## <a name="encode-an-object-using-c-or-c"></a>Codificación de un objeto mediante C o C++

<span id="to_encode_an_object_in_xml_using_c_c_"></span><span id="TO_ENCODE_AN_OBJECT_IN_XML_USING_C_C_"></span>

En el procedimiento siguiente se describe cómo codificar un objeto en XML mediante C o C++.

**Para codificar un objeto en XML mediante C o C++**

1.  Configure el programa para acceder a los datos WMI.

    Dado que WMI se basa en la tecnología COM, debe realizar las llamadas necesarias a las funciones [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) y [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para acceder a WMI. Para obtener más información, [vea Inicializar COM para una aplicación WMI.](initializing-com-for-a-wmi-application.md)

2.  Opcionalmente, cree un [**objeto IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) e inicialíclo.

    No es necesario crear el objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) a menos que tenga que cambiar la operación predeterminada. El codificador XML usa el objeto de contexto para controlar la cantidad de información incluida en la representación XML del objeto.

    En la tabla siguiente se enumeran los valores opcionales que se pueden especificar para el objeto de contexto.

    

    <table>
    <thead>
    <tr class="header">
    <th>Valor o tipo</th>
    <th>Significado</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>&quot;LocalOnly &quot; <strong>VT_BOOL</strong></td>
    <td>Cuando <strong>es TRUE</strong>, solo las propiedades y los métodos definidos localmente en la clase están presentes en el XML resultante. El valor predeterminado es <strong>FALSE</strong>.</td>
    </tr>
    <tr class="even">
    <td>&quot;IncludeQualifiers &quot; <strong>VT_BOOL</strong></td>
    <td>Cuando <strong>es TRUE,</strong>la clase, la instancia, las propiedades y los calificadores de método se incluyen en el XML resultante. El valor predeterminado es <strong>FALSE</strong>.</td>
    </tr>
    <tr class="odd">
    <td>&quot;ExcludeSystemProperties &quot; <strong>VT_BOOL</strong></td>
    <td>Cuando <strong>es TRUE,</strong>las propiedades del sistema WMI se filtran fuera de la salida. El valor predeterminado es <strong>FALSE</strong>.</td>
    </tr>
    <tr class="even">
    <td>&quot;PathLevel &quot; <strong>VT_I4</strong></td>
    <td><dl> 0 = Se &lt; genera una clase o un &gt; <INSTANCE> elemento.<br />
1 = Se <VALUE.NAMEDOBJECT> genera un elemento .<br />
2 = Se <VALUE.OBJECTWITHLOCALPATH> genera un elemento .<br />
3 = Se <VALUE.OBJECTWITHPATH> genera A.<br />
    </dl> El valor predeterminado es cero (0).<br/></td>
    </tr>
    </tbody>
    </table>

    

     

    En el ejemplo de código siguiente se muestra cómo se inicializa el objeto de contexto para incluir calificadores y excluir propiedades del sistema.

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

    

3.  Obtenga una referencia a la clase o instancia de para codificar en XML.

    Una vez que haya inicializado COM y esté conectado a WMI, llame a [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) para recuperar una referencia a la clase o instancia especificada. Si usó un BSTR para especificar la clase o instancia, llame a [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar la memoria asignada por [**SysAllocString.**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring)

    En el ejemplo de código siguiente se recupera una referencia a una [**instancia \_ de LogicalDisk de Win32.**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)

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

    

4.  Cree un [**objeto IWbemObjectTextSrc.**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc)

    Una vez que tenga una referencia a un objeto , debe crear el objeto [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) con una llamada a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance). El **objeto IWbemObjectTextSrc** se usa para generar el texto XML real.

    En el ejemplo de código siguiente se muestra cómo crear un [**objeto IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) mediante una [**llamada a CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

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

    

5.  [**Invoque el método IWbemObjectTextSrc.GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) para obtener una representación XML de un objeto.

    Después de establecer el contexto para la representación del objeto, obtener una referencia al objeto y crear un objeto [**IWbemObjectTextSrc,**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) está listo para generar una representación XML del objeto especificado llamando al método [**IWbemObjectTextSrc.GetText.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext)

    El siguiente código de ejemplo de C++ genera una representación XML del objeto al que hace referencia *pClass*. La representación XML se devuelve en *strText*. El tercer parámetro de [**GetText**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) especifica el formato de texto que se va a usar para xml y debe ser WMI \_ OBJ \_ TEXT CIM \_ \_ DTD \_ 2 \_ 0 (0x1) o WMI \_ OBJ TEXT WMI \_ \_ \_ DTD \_ 2 \_ 0 (0x2). Para obtener más información sobre estos valores, [**vea IWbemObjectTextSrc::GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) Parameter Values.

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

    

El siguiente código de ejemplo de C++ incluye todos los pasos del procedimiento anterior y codifica la clase [**\_ LogicalDisk de Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) en XML, incluidos los calificadores de clase, propiedad y método, y excluye las propiedades del sistema.


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



## <a name="encode-an-object-using-vbscript"></a>Codificación de un objeto mediante VBScript

<span id="to_encode_an_object_in_xml_using_vbscript"></span><span id="TO_ENCODE_AN_OBJECT_IN_XML_USING_VBSCRIPT"></span>

En el procedimiento siguiente se describe cómo codificar un objeto en XML mediante VBScript.

**Para codificar un objeto en XML mediante VBScript**

1.  Opcionalmente, cree un [**objeto SWbemNamedValueSet**](swbemnamedvalueset.md) e inicialíicelo para establecer los valores de contexto necesarios para la representación XML.

    En el ejemplo de código siguiente se muestra cómo los valores instruyen al codificador XML que genere <VALUE. OBJECTWITHLOCALPATH>, incluidos todos los calificadores y excluyendo las propiedades del sistema cuando construye la representación XML del objeto.

    ```VB
    ' Create an optional SWbemNamedValueSet object
    set context = CreateObject("wbemscripting.SWbemNamedValueSet")

    ' Initialize the value set object to set the context
    ' Generate a <VALUE.OBJECTWITHLOCALPATH> element
    context.add "PathLevel", 2 
    context.add "IncludeQualifiers", true 
    context.add "ExcludeSystemProperties", true '
    ```

    

2.  Recupere una instancia del objeto o clase que se representará en XML.

    En el ejemplo de código siguiente se recupera una instancia del objeto .

    ```VB
    ' Retrieve the object/class to be represented in XML
    set myObj = GetObject("winmgmts:\\.\root\cimv2:win32_LogicalDisk")
    ```

    

3.  Invoque el método [**GetText \_**](swbemobjectex-gettext-.md) de la instancia creada en el paso anterior, usando 1 como parámetro para especificar el formato de texto que corresponde a CIM DTD versión 2.0 o 2 para especificar el formato de texto que corresponde a la versión 2.0 de DTD de WMI. Si creó el [**objeto SWbemNamedValueSet**](swbemnamedvalueset.md) en el paso 1, insértelo en la lista de parámetros como tercer parámetro.

    En el ejemplo de código siguiente se muestra cómo invocar el [**método GetText \_**](swbemobjectex-gettext-.md) de la instancia de .

    ```VB
    ' Get the XML representation of the object
    strText = myObj.GetText_(2,,context)

    ' If you have not used a SWbemNamedValueSet object
    ' enter the following line.
    strText = myObj.GetText_(2)
    ```

    

4.  Opcionalmente, valide que el XML generado en el paso 3 es XML correcto, mediante la creación e inicialización de un objeto XML Document Object Model (DOM) y, a continuación, cargue el texto XML en él.

    En el ejemplo de código siguiente se muestra cómo crear e inicializar un objeto DOM XML y cargar el texto XML en él.

    ```VB
    ' Create an XMLDOM object
    set xml = CreateObject("Microsoft.xmldom")

    ' Initialize the XMLDOM object so results are returned synchronously
    xml.async = false

    ' Load the XML into the XMLDOM object
    xml.loadxml strText
    ```

    

5.  Generar la representación XML del objeto.

    En el ejemplo de código siguiente se muestra cómo usar wscript para generar el XML.

    ```VB
    wscript.echo strText
    ```

    

    Si eligió usar DOM XML para comprobar que el XML generado tiene el formato correcto, reemplace la línea anterior por lo siguiente.

    ```VB
    wscript.echo xml.xml
    ```

    

En el siguiente ejemplo de código de VBScript se incluyen todos los pasos del procedimiento anterior y se codifica la clase [**\_ LogicalDisk de Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) en XML, incluidos los calificadores de clase, propiedad y método, y se excluyen las propiedades del sistema.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de WMI](using-wmi.md)
</dt> </dl>

 

