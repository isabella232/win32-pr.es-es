---
description: La interfaz IWiaImageFilter es una interfaz de extensión implementada por los desarrolladores de filtros de procesamiento de imágenes y a la que llaman Windows Image Acquisition (WIA) 2.0.
ms.assetid: 2abe913b-bb2b-486d-a3f4-d5932433fc82
title: Interfaz IWiaImageFilter (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: d7c85a25d7478e0ad51a1d427e74b69a743bc4203ed57b8929a3e4ec856d94b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813985"
---
# <a name="iwiaimagefilter-interface"></a>Interfaz IWiaImageFilter

La **interfaz IWiaImageFilter** es una interfaz de extensión implementada por los desarrolladores de filtros de procesamiento de imágenes y a la que llaman Windows Image Acquisition (WIA) 2.0.

## <a name="members"></a>Miembros

La **interfaz IWiaImageFilter** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWiaImageFilter** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IWiaImageFilter** tiene estos métodos.



| Método                                                                | Descripción                                                                                             |
|:----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**ApplyProperties**](-wia-iwiaimagefilter-applyproperties.md)       | Permite que el filtro de procesamiento de imágenes vuelva a escribir propiedades en el controlador (y el dispositivo).<br/>     |
| [**FilterPreviewImage**](-wia-iwiaimagefilter-filterpreviewimage.md) | Filtra la imagen de vista previa.<br/>                                                                   |
| [**InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md)     | Inicializa el filtro. Lo llama WIA 2.0 antes de que se descargue cada imagen. <br/>                       |
| [**SetNewCallback**](-wia-iwiaimagefilter-setnewcallback.md)         | Establece una nueva devolución de llamada de aplicación para el filtro de procesamiento de imágenes que se usará para reenviar llamadas.<br/> |



 

## <a name="remarks"></a>Comentarios

Los desarrolladores de filtros de procesamiento de imágenes deben implementar esta interfaz y la [**interfaz IWiaTransferCallback.**](-wia-iwiatransfercallback.md)

WIA 2.0 llama a métodos de filtro. Nunca se les llama directamente desde una aplicación.

Microsoft proporciona el componente de versión preliminar de WIA 2.0, que almacena en caché la imagen de vista previa original sin filtrar que se adquiere del analizador. Una aplicación usa [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear de forma co-create una instancia del componente de versión preliminar de WIA 2.0 (CLSID WiaPreview), que carga el filtro mediante \_ [**IWiaItem2::GetExtension**](-wia-iwiaitem2-getextension.md). Se llama automáticamente al filtro cuando la aplicación llama a [**IWiaTransfer::D ownload**](-wia-iwiatransfer-download.md).

El filtro de procesamiento de imágenes siempre se ejecuta cuando se examina una imagen. Una aplicación no puede adquirir una imagen del analizador sin aplicar primero el filtro de creación de imágenes.

Un filtro debe implementar el brillo y el contraste como mínimo. La interfaz de usuario común, que proporciona controles de contraste y brillo al usuario, puede mostrar vistas previas precisas al usuario.

Un filtro de procesamiento de imágenes nunca debe modificar el *miembro lMessage* de la [**estructura WiaTransferParams.**](-wia-wiatransferparams.md)

Para leer las propiedades necesarias, el filtro de procesamiento de imágenes debe llamar a [**IWiaPropertyStorage::GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) en la interfaz [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) que obtiene del elemento llamando a [IWiaImageFilter::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). A continuación, el filtro puede crear una instancia [de IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) en esta secuencia para leer las propiedades de los elementos. El filtro de procesamiento de imágenes no debe llamar a [IWiaPropertyStorage::ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) directamente porque este método llama al controlador , pero el servicio `drvReadItemProperties` WIA 2.0 ya ha bloqueado el controlador en la llamada, por lo que esta llamada agotará el tiempo de espera y producirá un `drvAcquireItemData` error.

Las propiedades en las que está interesado el filtro podrían ser, por ejemplo, la configuración de brillo y contraste. Normalmente, el filtro también debe leer el formato de imagen, así como la propiedad de vista previa, [**WIA \_ DPS \_ PREVIEW**](-wia-wiaitempropscannerdevice.md), de *pWiaItem2*. Todas estas propiedades se usan en el proceso de filtrado.

Los componentes de WIA 2.0 siempre escriben datos sin filtrar en el filtro de procesamiento de imágenes. El algoritmo de procesamiento de imágenes implementado por la secuencia del filtro puede filtrar los datos más de una vez y no tiene que preocuparse de generar los mismos resultados que filtrar los datos una vez.

El filtro debe prestar atención a la propiedad [**WIA \_ DPS \_ PREVIEW,**](-wia-wiaitempropscannerdevice.md) especialmente si algunas tareas relacionadas con el filtro se controlan en hardware. Por ejemplo, un determinado controlador puede cambiar el brillo de la bombilla en el hardware del escáner en función de cómo la aplicación haya establecido el brillo en un elemento de WIA 2.0. Durante el examen final (cuando la aplicación llama a [**IWiaTransfer::D ownload),**](-wia-iwiatransfer-download.md)el controlador normalmente modificaría la bombilla física del analizador. En este caso, es posible que el filtro de procesamiento de imágenes no tenga que realizar ningún procesamiento de brillo. Sin embargo, durante un examen de vista previa, el controlador no debe modificar el brillo de la bombilla; en su lugar, debe ocuparse únicamente del filtro de procesamiento de imágenes. Es importante que el componente de vista previa de WIA 2.0 y el filtro de procesamiento de imágenes devuelvan imágenes precisas en función de las propiedades establecidas en el elemento.

Un filtro de procesamiento de imágenes debe admitir todos los formatos de imagen que admite el controlador.

El filtro de procesamiento de imágenes siempre tiene una imagen correspondiente al área de selección establecida en el elemento para el que se adquiere la imagen. Sin embargo, tenga en cuenta que el controlador puede haber girado la imagen en caso de que admita la [**\_ propiedad WIA IPS \_ ROTATION.**](-wia-wiaitempropscanneritem.md)

El filtro de procesamiento de imágenes se crea a través de [**IWiaItem2::GetExtension**](-wia-iwiaitem2-getextension.md), normalmente no por la aplicación, sino por los componentes de WIA 2.0 cuando una aplicación llama a [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) o [**IWiaTransfer::D ownload**](-wia-iwiatransfer-download.md).

La **interfaz IWiaImageFilter,** al igual que todas las interfaces del Modelo de objetos componentes (COM), hereda los métodos de [interfaz IUnknown.](/windows/win32/api/unknwn/nn-unknwn-iunknown)



| Métodos IUnknown                                        | Descripción                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Devuelve punteros a las interfaces compatibles. |
| [IUnknown::AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrementa el recuento de referencias.               |
| [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Reduce el recuento de referencias.               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
