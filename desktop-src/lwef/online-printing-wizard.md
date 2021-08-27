---
title: Asistente para impresión en línea
description: El Windows de impresión en línea de Vista ayuda a los usuarios a solicitar copias de fotos de distribuidores de impresión en línea participantes.
ms.assetid: 1e73a5d0-2ca8-4eca-846a-bd69eee257cb
keywords:
- Asistente para impresión en línea
- iconos,Asistente para impresión en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc402f1fe5853c7a255ea45940d62efcd092c424be6905287315c5cfe5fc7504
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975928"
---
# <a name="online-printing-wizard"></a>Asistente para impresión en línea

El Windows de impresión en línea de Vista ayuda a los usuarios a solicitar copias de fotos de distribuidores de impresión en línea participantes. Este asistente está diseñado para que cualquier aplicación que quiera ofrecer a los usuarios la posibilidad de solicitar copias de fotos lo pueda invocar mediante programación. El Asistente para impresión de fotos está disponible en Windows Vista. LAV para Windows

-   [Características proporcionadas por el Asistente para impresión en línea](#features-provided-by-the-online-print-wizard)
-   [Formatos de archivo de fotos admitidos](#supported-photo-file-formats)
-   [Iniciar el Asistente para impresión en línea mediante programación](#programmatically-launching-the-online-print-wizard)
-   [Acceso al icono del Asistente para impresión en línea](#accessing-the-online-print-wizard-icon)
-   [Propiedades de MRU del Asistente para impresión en línea](#online-print-wizard-mru-properties)

## <a name="features-provided-by-the-online-print-wizard"></a>Características proporcionadas por el Asistente para impresión en línea

El Windows de impresión en línea de Vista permite a los usuarios solicitar copias impresas de una selección de distribuidores de impresión en línea participantes. Cuando se invoca, el asistente:

1.  Acepta un archivo o una lista de archivos para los que se van a ordenar las copias impresas.
2.  Recupera automáticamente la lista actual de distribuidores de impresión en línea participantes y permite al usuario seleccionar el distribuidor desde el que comprar las copias impresas.
3.  Guía al usuario a través del proceso u ordenación de las copias impresas.

Cualquier aplicación puede beneficiarse de las características que ofrece Windows Asistente para impresión en línea de Vista. Una aplicación solo necesita pasar el archivo o los archivos para los que se ordenarán las copias impresas, y el asistente guía al usuario a través del proceso de ordenación.

En la ilustración siguiente se muestra Windows Asistente para impresión en línea de Vista que muestra una lista de ejemplo de distribuidores de impresión en línea participantes.

![El Asistente para impresión en línea de Windows Vista](images/opw.png)

## <a name="supported-photo-file-formats"></a>Formatos de archivo de fotos admitidos

El Windows de impresión en línea de Vista admite cualquier formato de archivo de imagen para el que esté instalado un códec Windows Imaging Component (WIC). WIC proporciona varios códecs estándar, entre los que se incluyen:

-   Mapa de bits (BMP)
-   Formato de intercambio de gráficos (GIF)
-   Formato de icono (ICO)
-   Formato JPEG (Joint Photographic Experts Group)
-   Formato PNG (Portable Network Graphics)
-   Tagged Image File Format (TIFF)
-   Windows Formato de foto multimedia

Para obtener más información sobre los códecs WIC y WIC, [vea Windows Imaging Component](https://msdn.microsoft.com/library/ms737408(VS.85).aspx).

Los formatos de archivo admitidos por los distribuidores de impresión en línea varían de minorista a minorista. Es posible que un distribuidor determinado no admita todos los formatos de archivo admitidos por el Asistente para impresión Windows Vista Online. Si el usuario intenta solicitar copias impresas en un formato que no es compatible con el distribuidor seleccionado, el Asistente para impresión en línea de Windows Vista notifica al usuario que el distribuidor seleccionado no admite el formato de archivo enviado.

## <a name="programmatically-launching-the-online-print-wizard"></a>Iniciar el Asistente para impresión en línea mediante programación

Para invocar el asistente Windows impresión en línea de Vista, llame a la [interfaz IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) con el siguiente identificador de clase (CLSID):


```
CLSID_PublishDropTarget
```



Este CLSID se define en Shobjidl.h y Shobjidl.idl. Los archivos que va a procesar el Windows Vista Online Printing se especifican en un [objeto IDataObject.](/windows/win32/api/objidl/nn-objidl-idataobject)

En el ejemplo de código siguiente se muestra cómo invocar Windows Asistente para impresión en línea de Vista.


```
// A data object that contains the list of photos to print.
IDataObject* pDataObject;

// Create the Photo Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
hr = CoCreateInstance(CLSID_PublishDropTarget,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&spDropTarget));

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);}
```



## <a name="accessing-the-online-print-wizard-icon"></a>Acceso al icono del Asistente para impresión en línea

El Windows de impresión en línea de Vista exporta un icono al que pueden acceder y mostrar las aplicaciones que lo llaman. En la ilustración siguiente se muestra Windows asistente para impresión en línea de Vista.

![icono del Asistente para impresión en línea de Windows Vista](images/opw-icon.png)

En el ejemplo de código siguiente se muestra cómo recuperar el índice del Windows asistente para impresión en línea de Vista mediante la lectura de **la propiedad OPWIcon.**


```
// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Get the Online Printing Wizard properties.
CComPtr<IPropertyBag> spPropsBag;

spDropTarget->QueryInterface(IID_PPV_ARGS(&spPropsBag));

// Read the icon index from the properties set. 
CComVariant vtIcon;
int nIndex;
hr = spPropsBag->Read(L"OPWIcon", &vtIcon, NULL);

if SUCCEEDED(hr)
{
    nIndex = vtIcon.lVal;
}
```



## <a name="online-print-wizard-mru-properties"></a>Propiedades de MRU del Asistente para impresión en línea

El Windows de impresión en línea de Vista define tres propiedades relacionadas con el distribuidor de impresión en línea (MRU) usado más recientemente.



| Nombre de la propiedad | Property Value/Function                                                                                                                                                                                                                                                   |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MRUIcon**   | El índice del icono del distribuidor de impresión en línea usado más recientemente se puede leer desde esta propiedad.                                                                                                                                                                 |
| **MRUName**   | El nombre del distribuidor de impresión en línea usado más recientemente se puede leer desde esta propiedad.                                                                                                                                                                               |
| **UseMRU**    | Valor **VARIANT** **VT \_ BOOL** que indica si el asistente debe omitir la página de selección del distribuidor de impresión en línea y simplemente usar el distribuidor de impresión en línea usado más recientemente en su lugar. Establezca esta propiedad en **VARIANT \_ TRUE para** omitir la página de selección del distribuidor. |



 

En el ejemplo de código siguiente se muestra cómo establecer la propiedad UseMRU para que el Asistente para impresión en línea de Windows Vista omita la página de selección del distribuidor de impresión en línea y seleccione automáticamente el distribuidor usado más recientemente.


```
// A data object that contains the list of photos to order prints for.
IDataObject* pDataObject;

// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Set the UserMRU property to true to skip retailer selection and use 
// the MRU retailer instead.    
CComQIPtr<IPropertyBag> spPropsBag(spDropTarget);
if(spPropsBag) 
{
    VARIANT varTrue = {0};
    varTrue.vt = VT_BOOL;
    varTrue.boolVal = VARIANT_TRUE;
    spPropsBag->Write(L"UseMRU", &varTrue);
}

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);
```



En el ejemplo de código siguiente se muestra cómo leer las propiedades MRUName y MRUIcon.


```
// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Get the Online Printing Wizard properties.
CComPtr<IPropertyBag> spPropsBag;
spDropTarget->QueryInterface(IID_PPV_ARGS(&spPropsBag));

CComVariant vtMRUName, vtMRUIconIndex;
CComBSTR bstrMRUName;
int nMRUIconIndex;

// Get the MRU name value.
hr = spPropsBag->Read(L"MRUName", &vtMRUName, NULL);
if SUCCEEDED(hr) 
{
    bstrMRUName = vtMRUName.bstrVal;
}

// Get the MRU icon index value.
hr = spPropsBag->Read(L"MRUIcon", &vtMRUIconIndex, NULL);
if SUCCEEDED(hr)
{
    nMRUIconIndex = vtMRUIconIndex.lVal;
}
```



 

 