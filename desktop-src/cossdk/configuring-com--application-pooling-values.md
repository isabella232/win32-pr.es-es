---
description: Puede usar las siguientes instrucciones para configurar los valores de agrupación de aplicaciones COM+ para la aplicación COM+.
ms.assetid: faba5cb7-745e-4fdf-a3e0-62132da4a843
title: Configuración de valores de agrupación de aplicaciones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98922699fff7af7146250bdb504a1f46be08718e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127358912"
---
# <a name="configuring-com-application-pooling-values"></a>Configuración de valores de agrupación de aplicaciones COM+

Puede usar las siguientes instrucciones para configurar los valores de agrupación de aplicaciones COM+ para la aplicación COM+.

> [!Note]  
> Las aplicaciones de biblioteca tienen las propiedades de reciclaje y agrupación de su proceso de host.

 

## <a name="component-services-administrative-tool"></a>Herramienta administrativa de servicios de componentes

Para configurar la agrupación de aplicaciones COM+ para una aplicación COM+, siga estos pasos:

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, haga clic con el botón derecho en la aplicación COM+ que quiera agrupar y, a continuación, haga clic en **Propiedades.**

2.  En la pestaña **Agrupación & reciclaje,** en Agrupación de aplicaciones **,** escriba un valor para Tamaño de grupo **,** en función del número de instancias de la aplicación que quiera tener en ejecución.

3.  Haga clic en **OK**.

## <a name="visual-basic"></a>Visual Basic

La siguiente función de Visual Basic muestra cómo puede establecer el valor de agrupación de aplicaciones COM+ (representado por su propiedad ConcurrentApps) para cualquier aplicación de servidor COM+ que elija. Para usarlo desde Visual Basic, agregue una referencia a la biblioteca de tipos de administrador de COM+.


```VB
Function SetMyApplicationPooling( _
  strApplicationName As String, _
  lngPoolValue As Long _
) As Boolean  ' Return False if any errors occur.

    SetMyApplicationPooling = False  ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim objCatalog As COMAdmin.COMAdminCatalog
    Dim objAppCollection As COMAdmin.COMAdminCatalogCollection
    Dim objApplication As COMAdmin.COMAdminCatalogObject
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
    Set objAppCollection = objCatalog.GetCollection("Applications")
    objAppCollection.Populate 
    For Each objApplication in objAppCollection
        If objApplication.Name = strApplicationName Then
            objApplication.Value("ConcurrentApps") = lngPoolValue
            MsgBox strApplicationName & _
              " pooling value set to " & lngPoolValue
            Exit For
        End If
    Next
    objAppCollection.SaveChanges

    Set objApplication = Nothing
    Set objAppCollection = Nothing
    Set objCatalog = Nothing
    SetMyApplicationPooling = True  ' Successful end to procedure
    Exit Function

My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objApplication = Nothing
    Set objAppCollection = Nothing
    Set objCatalog = Nothing
End Function

```



Para usar la función , proporcione un valor de cadena para el nombre de aplicación del servidor COM+ y un valor entero para la configuración de agrupación de aplicaciones deseada. En el Visual Basic siguiente se muestra cómo establecer el valor de agrupación de aplicaciones en 15 para la aplicación denominada "MyApplication":


```VB
Sub Main()
    If Not SetMyApplicationPooling("MyApplication", 15) Then
        MsgBox "SetMyApplicationPooling failed."
    End If
End Sub

```



## <a name="cc"></a>C/C++

La siguiente función de C++ muestra cómo puede establecer el valor de agrupación de aplicaciones COM+ (representado por su propiedad ConcurrentApps) para cualquier aplicación de servidor COM+ que elija. El método ErrorDescription se describe en [Interpretación de códigos de error](interpreting-error-codes.md).


```C++
#include <windows.h>
#include <stdio.h>
#import "C:\WINDOWS\system32\Com\ComAdmin.dll"
#include "ComAdmin.h"
#include "StrSafe.h"  // For the StringCchLengthW function

BOOL SetMyApplicationPooling (OLECHAR* szMyApp, LONG lPool) {
    IUnknown * pUnknown = NULL;
    ICOMAdminCatalog * pCatalog = NULL;
    ICatalogCollection * pAppColl = NULL;
    ICatalogObject * pApplication = NULL;
    HRESULT hr = S_OK;
    BSTR bstrMyApp = NULL;
    unsigned int uMaxLen = 255;  // Maximum length of szMyApp
    LCID lLan = 1024;// Use the default language for comparing strings.

try {
    // Test the input pool value.
    if ((lPool < 1) || (lPool > 1048576)) throw(E_INVALIDARG);
    
    // Test the input szMyApp to make sure it's OK to use.
    hr = StringCchLengthW(szMyApp, uMaxLen, NULL);
    if (FAILED (hr)) throw(hr);
    
    // Convert szMyApp to a BSTR.
    bstrMyApp = SysAllocString(szMyApp);

    // Create a COMAdminCatalog object and get its IUnknown.
    hr = CoCreateInstance(CLSID_COMAdminCatalog, NULL, 
      CLSCTX_INPROC_SERVER, IID_IUnknown, (void**)&pUnknown);
    if (FAILED (hr)) throw(hr);

    // Get the ICOMAdminCatalog interface.
   hr = pUnknown->QueryInterface(IID_ICOMAdminCatalog, 
      (void**)&pCatalog); 
    if (FAILED (hr)) throw(hr);

    // Get an interface to the Applications collection.
    hr = pCatalog->GetCollection(L"Applications", (IDispatch**)&pAppColl);
    if (FAILED (hr)) throw(hr);

    // Populate all of the Applications collection.
    hr = pAppColl->Populate();
    if (FAILED (hr)) throw(hr);

    // Get the number of applications in the collection.
    LONG lCount = -1;
    hr = pAppColl->get_Count(&lCount);
    if (FAILED (hr)) throw(hr);

    // Iterate through each application in the collection.
    VARIANT varName;
    VariantInit(&varName);
    for (LONG lIdx = 0; lIdx < lCount; lIdx++) {
        hr = pAppColl->get_Item(lIdx, (IDispatch**)&pApplication);
        if (FAILED (hr)) throw(hr);

        // Get the Name value of each application.
       hr = pApplication->get_Name(&varName);
        if (FAILED (hr)) throw(hr);

        // Compare the application name to bstrMyApp.
        hr = VarBstrCmp(varName.bstrVal, bstrMyApp, lLan, NULL);
        if (FAILED (hr)) throw(hr);
        if (VARCMP_EQ == hr) {  // The strings are equal.
            // Set the new pooling value.
            VARIANT varPool;
            VariantInit(&varPool);
            varPool.vt = VT_I4;  // Tell the VARIANT it's holding a LONG.
            varPool.lVal = lPool;
            hr = pApplication->put_Value(L"ConcurrentApps", varPool);
            if (FAILED (hr)) throw(hr);
            printf("%S pooling value set to %ld.\n", bstrMyApp, lPool);
            break;
        }
    }
    LONG lNum;
    hr = pAppColl->SaveChanges(&lNum);
    if (FAILED (hr)) throw(hr);

    // Clean up.
    SysFreeString(bstrMyApp);
    pUnknown->Release();
    pUnknown = NULL;
    pApplication->Release();
    pApplication = NULL;
    pAppColl->Release();
    pAppColl = NULL;
    pCatalog->Release();
    pCatalog = NULL;
    return (TRUE);
}  // Try

catch(HRESULT hr) {  // Replace with specific error handling.
    printf("Error # %#x: ", hr);
    ErrorDescription(hr);
    SysFreeString(bstrMyApp);
    if (NULL != pUnknown) pUnknown>Release();
    pUnknown = NULL;
    if (NULL != pApplication) pApplication->Release();
    pApplication = NULL;
    if (NULL != pAppColl) pAppColl->Release();
    pAppColl = NULL;
    if (NULL != pCatalog) pCatalog->Release();
    pCatalog = NULL;
    return (FALSE);
}catch(...) {
    printf("An unexpected exception occurred.\n");
    throw;
}
}  // SetMyApplicationPooling

```



Para usar la función , proporcione un valor de cadena para el nombre de aplicación del servidor COM+ y un valor entero para la configuración de agrupación de aplicaciones deseada. El siguiente código de C++ muestra cómo establecer el valor de agrupación de aplicaciones en 15 para la aplicación denominada "MyApplication":

``` syntax
#define _WIN32_DCOM  // To use CoInitializeEx()
void main() {
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (FAILED (hr)) {
        printf("CoInitializeEx failed: Error # %#x\n", hr);
        exit(0);  // Replace with specific error handling.
    }
    if (! SetMyApplicationPooling (L"MyApplication", 15))
        printf("SetMyApplicationPooling failed.\n");
    CoUninitialize();
}
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de agrupación de aplicaciones COM+](com--application-pooling-concepts.md)
</dt> </dl>

 

 



