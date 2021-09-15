---
description: Invoca el filtro de segmentación de controladores y pasa la imagen sin filtrar almacenada en caché por el método IWiaPreview::GetNewPreview al filtro.
ms.assetid: 4ae817b5-7091-432e-b004-0e53ae14fdb2
title: Método IWiaPreview::D etectRegions (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.DetectRegions
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 40665d2aae6e1e2dffa4356540afb05d45050492
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575633"
---
# <a name="iwiapreviewdetectregions-method"></a>IWiaPreview::D etectRegions (método)

Invoca el filtro de segmentación de controladores y pasa la imagen sin filtrar almacenada en caché por el método [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) al filtro.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DetectRegions(
  [in] LONG lFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lFlags* \[ En\]
</dt> <dd>

Tipo: **LONG**

No se usa. Establezca en cero (0).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Este método puede devolver uno de estos valores.



| Código devuelto                                                                               | Descripción                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | La operación se realizó correctamente.<br/>              |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | El controlador no admite la segmentación.<br/> |
| <dl> <dt>**otherwise**</dt> </dl>  | Código de error COM estándar.<br/>                |



 

## <a name="remarks"></a>Observaciones

Una aplicación debe llamar [**a IWiaPreview::GetNewPreview antes**](-wia-iwiapreview-getnewpreview.md) de llamar a esta función.

Cuando el componente de versión preliminar de Windows Image Acquisition (WIA) 2.0 llama a **IWiaPreview::D etectRegions,** invoca el filtro de segmentación de controladores y pasa la interfaz [**IWiaItem2**](-wia-iwiaitem2.md) que se pasó anteriormente a [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md). También pasa la imagen almacenada internamente en caché al filtro. El filtro de segmentación usa la imagen almacenada en caché para crear las extensiones secundarias.

Si una aplicación cambia alguna propiedad de la interfaz [**IWiaItem2**](-wia-iwiaitem2.md) después de llamar a [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md), se deben restaurar las propiedades originales antes de que la aplicación llame a **IWiaPreview::D etectRegions**. Use [**GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) y [**SetPropertyStream para**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream) restaurar las propiedades originales.

**IWiaPreview::D etectRegions** se usa para determinar las "subregiones" de la imagen almacenada en caché. Para cada región secundaria detectada, se crea un nuevo elemento secundario de WIA 2.0 en la [**interfaz IWiaItem2.**](-wia-iwiaitem2.md) Para cada elemento secundario, el filtro de segmentación debe establecer los valores de las siguientes propiedades de WIA 2.0: WIA \_ IPS \_ XPOS, WIA \_ IPS \_ YPOS, WIA \_ IPS \_ XEXTENT y WIA \_ IPS \_ YEXTENT. Un filtro más avanzado establece otras propiedades de WIA 2.0, como WIA \_ IPS DESKEW X y \_ \_ WIA \_ IPS DESKJDBC Y, si el controlador admite la \_ \_ desessestreo. Las propiedades WIA \_ IPS \_ XPOS, WIA \_ IPS \_ YPOS, WIA \_ IPS \_ XEXTENT y WIA \_ IPS \_ YEXTENT representan el rectángulo delimitador del área que se va a examinar.

Es posible que el controlador no admita la segmentación. Antes de llamar a **IWiaPreview::D etectRegions,** una aplicación normalmente comprueba si el controlador admite la propiedad \_ SEGMENTATION de IPS de \_ WIA. Si no se implementa la propiedad , no se admite la segmentación y se produce un error **en IWiaPreview::D etectRegions** y devuelve E \_ NOTIMPL.

La aplicación debe limpiar los elementos secundarios creados mediante una llamada a **IWiaPreview::D etectRegions**. Por ejemplo, si una aplicación realiza una llamada adicional a **IWiaPreview::D etectRegions** en el mismo elemento, debe limpiar los elementos secundarios anteriores.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 




