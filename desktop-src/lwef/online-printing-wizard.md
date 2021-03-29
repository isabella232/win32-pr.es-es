---
title: Asistente para impresión en línea
description: El Asistente para impresión en línea de Windows Vista ayuda a los usuarios a solicitar copias impresas de fotografías de los distribuidores de impresiones en línea.
ms.assetid: 1e73a5d0-2ca8-4eca-846a-bd69eee257cb
keywords:
- Asistente para impresión en línea
- iconos, Asistente para impresión en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8536eea7a51eddb2dbb46d10c9291a60edfdc74e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358960"
---
# <a name="online-printing-wizard"></a>Asistente para impresión en línea

El Asistente para impresión en línea de Windows Vista ayuda a los usuarios a solicitar copias impresas de fotografías de los distribuidores de impresiones en línea. Este asistente está diseñado para que se pueda invocar mediante programación por cualquier aplicación que desee ofrecer a los usuarios la posibilidad de solicitar impresiones de fotografías. El Asistente para impresión de fotografías está disponible en Windows Vista. PIX para Windows

-   [Características proporcionadas por el Asistente para impresión en línea](#features-provided-by-the-online-print-wizard)
-   [Formatos de archivo fotográfico admitidos](#supported-photo-file-formats)
-   [Inicio mediante programación del Asistente para impresión en línea](#programmatically-launching-the-online-print-wizard)
-   [Acceso al icono del Asistente para impresión en línea](#accessing-the-online-print-wizard-icon)
-   [Propiedades MRU del Asistente para impresión en línea](#online-print-wizard-mru-properties)

## <a name="features-provided-by-the-online-print-wizard"></a>Características proporcionadas por el Asistente para impresión en línea

El Asistente para impresión en línea de Windows Vista permite a los usuarios ordenar copias fotográficas a partir de una selección de distribuidores de impresión en línea participantes. Cuando se invoca, el asistente:

1.  Acepta un archivo o una lista de archivos para los que se van a ordenar las impresiones.
2.  Recupera automáticamente la lista actual de los distribuidores de impresión en línea participantes y permite al usuario seleccionar el distribuidor desde el que desea comprar las fotos fotográficas.
3.  Guía al usuario a través del proceso o la ordenación de copias fotográficas.

Cualquier aplicación puede beneficiarse de las características que ofrece el Asistente para impresión en línea de Windows Vista. Una aplicación solo necesita pasar el archivo o los archivos para los que se van a ordenar las impresiones y el asistente guía al usuario a través del proceso de ordenación.

En la siguiente ilustración se muestra el Asistente para impresión en línea de Windows Vista, donde se muestra una lista de ejemplo de los distribuidores de impresión en línea participantes.

![Asistente para impresión en línea de Windows Vista](images/opw.png)

## <a name="supported-photo-file-formats"></a>Formatos de archivo fotográfico admitidos

El Asistente para impresión en línea de Windows Vista admite cualquier formato de archivo de imagen para el que esté instalado un códec de Windows Imaging Component (WIC). WIC proporciona varios códecs estándar, entre los que se incluyen:

-   Mapa de bits (BMP)
-   Formato de intercambio de gráficos (GIF)
-   Formato de icono (ICO)
-   Formato JPEG (Joint Photographic Experts Group)
-   Formato PNG (Portable Network Graphics)
-   Tagged Image File Format (TIFF)
-   Formato de Windows Media Photo

Para obtener más información acerca de los códecs WIC y WIC, vea [Windows Imaging Component](https://msdn.microsoft.com/library/ms737408(VS.85).aspx).

Los formatos de archivo que admiten los distribuidores de impresión en línea varían de un distribuidor a un distribuidor; es posible que un distribuidor determinado no admita todos los formatos de archivo admitidos por el Asistente para impresión en línea de Windows Vista. Si el usuario intenta pedir copias fotográficas en un formato no admitido por el distribuidor seleccionado, el Asistente para impresión en línea de Windows Vista notifica al usuario que el distribuidor seleccionado no admite el formato de archivo enviado.

## <a name="programmatically-launching-the-online-print-wizard"></a>Inicio mediante programación del Asistente para impresión en línea

Para invocar el Asistente para impresión en línea de Windows Vista, llame a la interfaz [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) con el siguiente identificador de clase (CLSID):


```
CLSID_PublishDropTarget
```



Este CLSID se define en shobjidl. h y shobjidl. idl. Los archivos que se van a procesar mediante el Asistente para impresión en línea de Windows Vista se especifican en un objeto [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) .

En el ejemplo de código siguiente se muestra cómo invocar el Asistente para impresión en línea de Windows Vista.


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

El Asistente para impresión en línea de Windows Vista exporta un icono al que pueden tener acceso y mostrar las aplicaciones que lo llaman. En la siguiente ilustración se muestra el icono del Asistente para impresión en línea de Windows Vista.

![icono del Asistente para impresión en línea de Windows Vista](images/opw-icon.png)

En el ejemplo de código siguiente se muestra cómo recuperar el índice para el icono del Asistente para impresión en línea de Windows Vista mediante la lectura de la propiedad **OPWIcon** .


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



## <a name="online-print-wizard-mru-properties"></a>Propiedades MRU del Asistente para impresión en línea

El Asistente para impresión en línea de Windows Vista define tres propiedades relacionadas con el distribuidor de impresión en línea usado más recientemente (MRU).



| Nombre de la propiedad | Valor o función de la propiedad                                                                                                                                                                                                                                                   |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MRUIcon**   | El índice del icono del distribuidor de impresión en línea usado más recientemente se puede leer desde esta propiedad.                                                                                                                                                                 |
| **MRUName**   | El nombre del distribuidor de impresión en línea usado más recientemente se puede leer desde esta propiedad.                                                                                                                                                                               |
| **UseMRU**    | Un valor booleano de VT de **tipo** ** \_ bool** que indica si el asistente debe omitir la página de selección del distribuidor de impresión en línea y usar en su lugar el distribuidor de impresión en línea usado más recientemente. Establezca esta propiedad en **Variant \_ true** para omitir la página de selección del distribuidor. |



 

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



 

 