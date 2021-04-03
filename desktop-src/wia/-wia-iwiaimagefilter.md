---
description: La interfaz IWiaImageFilter es una interfaz de extensión implementada por desarrolladores de filtros de procesamiento de imágenes y llamada por la adquisición de imágenes de Windows (WIA) 2,0.
ms.assetid: 2abe913b-bb2b-486d-a3f4-d5932433fc82
title: Interfaz IWiaImageFilter (WIA. h)
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
ms.openlocfilehash: 8d859b79d15db627bb09cb60f758791a8b5860f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909858"
---
# <a name="iwiaimagefilter-interface"></a>Interfaz IWiaImageFilter

La interfaz **IWiaImageFilter** es una interfaz de extensión implementada por desarrolladores de filtros de procesamiento de imágenes y llamada por la adquisición de imágenes de Windows (WIA) 2,0.

## <a name="members"></a>Miembros

La interfaz **IWiaImageFilter** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaImageFilter** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IWiaImageFilter** tiene estos métodos.



| Método                                                                | Descripción                                                                                             |
|:----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**ApplyProperties**](-wia-iwiaimagefilter-applyproperties.md)       | Permite que el filtro de procesamiento de imágenes escriba las propiedades de nuevo en el controlador (y en el dispositivo).<br/>     |
| [**FilterPreviewImage**](-wia-iwiaimagefilter-filterpreviewimage.md) | Filtra la imagen de vista previa.<br/>                                                                   |
| [**InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md)     | Inicializa el filtro. Lo llama WIA 2,0 antes de descargar cada imagen. <br/>                       |
| [**SetNewCallback**](-wia-iwiaimagefilter-setnewcallback.md)         | Establece una nueva devolución de llamada de aplicación para el filtro de procesamiento de imágenes que se va a usar para las llamadas de reenvío.<br/> |



 

## <a name="remarks"></a>Observaciones

Los desarrolladores de filtros de procesamiento de imágenes deben implementar esta interfaz y la interfaz [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) .

WIA 2,0 llama a los métodos de filtro. Nunca se llama directamente desde una aplicación.

Microsoft proporciona el componente WIA 2,0 Preview, que almacena en caché la imagen de vista previa original y sin filtrar que se adquiere del escáner. Una aplicación utiliza [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear una instancia del componente de vista previa de WIA 2,0 (CLSID \_ WiaPreview), que carga el filtro mediante [**IWiaItem2:: getExtension**](-wia-iwiaitem2-getextension.md). Se llama al filtro automáticamente cuando la aplicación llama a [**IWiaTransfer::D scargar**](-wia-iwiatransfer-download.md).

El filtro de procesamiento de imágenes siempre se ejecuta cuando se examina una imagen. Una aplicación no puede adquirir una imagen del escáner sin tener primero aplicado el filtro de creación de imágenes.

Un filtro debe implementar el brillo y el contraste como mínimo. La interfaz de usuario común, que proporciona controles de brillo y contraste al usuario, puede mostrar vistas previas exactas al usuario.

Un filtro de procesamiento de imágenes nunca debe modificar el miembro *lMessage* de la estructura [**WiaTransferParams**](-wia-wiatransferparams.md) .

Para leer las propiedades necesarias, el filtro de procesamiento de imágenes debe llamar a [**IWiaPropertyStorage:: GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) en la interfaz [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) que obtiene del elemento mediante una llamada a [IWiaImageFilter:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). Después, el filtro puede crear instancias de una instancia de [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) en esta secuencia para leer las propiedades de los elementos. El filtro de procesamiento de imágenes no debe llamar directamente a [IWiaPropertyStorage:: ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) porque este método llama a la del controlador `drvReadItemProperties` , pero el servicio WIA 2,0 ya ha bloqueado el controlador en la `drvAcquireItemData` llamada, por lo que esta llamada superará el tiempo de espera y producirá un error.

Las propiedades que le interesa el filtro pueden ser, por ejemplo, la configuración de brillo y contraste. Normalmente, el filtro también necesita leer el formato de imagen, así como la propiedad de vista previa, [**WIA \_ DPS \_ Preview**](-wia-wiaitempropscannerdevice.md), de *pWiaItem2*. Todas estas propiedades se usan en el proceso de filtrado.

Los componentes de WIA 2,0 siempre escriben datos sin filtrar en el filtro de procesamiento de imágenes. El algoritmo de procesamiento de imágenes implementado por el flujo del filtro puede filtrar los datos más de una vez y no tiene que preocuparse por la generación de los mismos resultados que al filtrar los datos una vez.

El filtro debe prestar atención a la propiedad de [**\_ \_ vista previa de DPS de WIA**](-wia-wiaitempropscannerdevice.md) , especialmente si algunas tareas relacionadas con el filtro se tratan en el hardware. Por ejemplo, un determinado controlador puede cambiar el brillo de la lámpara en el hardware del escáner, en función de cómo la aplicación haya establecido el brillo en un elemento de WIA 2,0. Durante el análisis final (cuando la aplicación llama a [**IWiaTransfer::D scargar**](-wia-iwiatransfer-download.md)), el controlador normalmente modificaría la lámpara física del escáner. En este caso, es posible que el filtro de procesamiento de imágenes no tenga que realizar ningún procesamiento de brillo. Sin embargo, durante un examen de vista previa, el controlador no debe modificar el brillo de la lámpara; en su lugar, se debe tener cuidado únicamente en el filtro de procesamiento de imágenes. Es importante que el componente de vista previa de WIA 2,0 y el filtro de procesamiento de imágenes devuelvan imágenes precisas en función de las propiedades establecidas en el elemento.

Un filtro de procesamiento de imágenes debe admitir todos los formatos de imagen admitidos por el controlador.

Al filtro de procesamiento de imágenes siempre se le proporciona una imagen que corresponde al área de selección establecida en el elemento para el que se está adquiriendo la imagen. Sin embargo, tenga en cuenta que el controlador puede haber girado la imagen en caso de que admita la propiedad de [**\_ \_ rotación de IP de WIA**](-wia-wiaitempropscanneritem.md) .

El filtro de procesamiento de imágenes se crea a través de [**IWiaItem2:: getExtension**](-wia-iwiaitem2-getextension.md), normalmente no de la aplicación, sino por componentes de WIA 2,0 cuando una aplicación llama a [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) o [**IWiaTransfer::D scargar**](-wia-iwiatransfer-download.md).

La interfaz **IWiaImageFilter** , al igual que todas las interfaces del modelo de objetos componentes (com), hereda los métodos de interfaz [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .



| Métodos IUnknown                                        | Descripción                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Devuelve punteros a las interfaces compatibles. |
| [IUnknown:: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrementa el recuento de referencias.               |
| [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Reduce el recuento de referencias.               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
