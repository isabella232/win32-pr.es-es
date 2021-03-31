---
description: 'Invoca el filtro de segmentación de controladores y pasa al filtro la imagen sin filtrar almacenada en memoria caché por el método IWiaPreview:: GetNewPreview.'
ms.assetid: 4ae817b5-7091-432e-b004-0e53ae14fdb2
title: IWiaPreview::D método etectRegions (WIA. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275462"
---
# <a name="iwiapreviewdetectregions-method"></a>IWiaPreview::D método etectRegions

Invoca el filtro de segmentación de controladores y pasa al filtro la imagen sin filtrar almacenada en memoria caché por el método [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DetectRegions(
  [in] LONG lFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lFlags* \[ de\]
</dt> <dd>

Tipo: **Long**

No se utiliza. Se establece en cero (0).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Este método puede devolver uno de estos valores.



| Código devuelto                                                                               | Descripción                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>      | La operación se realizó correctamente.<br/>              |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | El controlador no admite la segmentación.<br/> |
| <dl> <dt>**otherwise**</dt> </dl>  | Un código de error COM estándar.<br/>                |



 

## <a name="remarks"></a>Observaciones

Una aplicación debe llamar a [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) antes de llamar a esta función.

Cuando el componente de vista previa de la adquisición de imágenes de Windows (WIA) 2,0 llama a **IWiaPreview::D etectregions**, invoca el filtro de segmentación de controladores y pasa la interfaz [**IWiaItem2**](-wia-iwiaitem2.md) que se pasó previamente a [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md). También pasa la imagen almacenada en caché internamente al filtro. El filtro segmentación utiliza la imagen almacenada en caché para crear las extensiones secundarias.

Si una aplicación cambia cualquier propiedad de la interfaz [**IWiaItem2**](-wia-iwiaitem2.md) después de llamar a [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md), se deben restaurar las propiedades originales antes de que la aplicación llame a **IWiaPreview::D etectregions**. Use [**GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) y [**SetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream) para restaurar las propiedades originales.

**IWiaPreview::D etectregions** se usa para determinar las "subregiones" de la imagen almacenada en caché. Para cada subregión detectada, se crea un nuevo elemento secundario de WIA 2,0 en la interfaz [**IWiaItem2**](-wia-iwiaitem2.md) . Para cada elemento secundario, el filtro de segmentación debe establecer los valores de las siguientes propiedades de WIA 2,0: direcciones IP de WIA, las IP de WIA, XEXTENT y las IP de WIA \_ \_ \_ \_ \_ \_ \_ \_ YEXTENT. Un filtro más avanzado establece otras propiedades de WIA 2,0, como la desfragmentación de las direcciones \_ IP \_ de WIA \_ X y WIA, \_ \_ dessesgado \_ y, si el controlador admite la anulación del sesgo. Las \_ propiedades WIA IP \_ XPOS, WIA \_ IP \_ YPOS, WIA \_ IP \_ XEXTENT y WIA \_ IPS \_ YEXTENT representan el rectángulo delimitador del área que se va a examinar.

Es posible que el controlador no admita la segmentación. Antes de llamar a **IWiaPreview::D etectregions**, una aplicación comprueba normalmente si el controlador admite la \_ propiedad de segmentación de IP de WIA \_ . Si la propiedad no está implementada, no se admite la segmentación y **IWiaPreview::D etectregions** produce un error y devuelve e \_ NOTIMPL.

La aplicación debe limpiar los elementos secundarios que se crean mediante una llamada a **IWiaPreview::D etectregions**. Por ejemplo, si una aplicación realiza una llamada adicional a **IWiaPreview::D etectregions** en el mismo elemento, debe limpiar los elementos secundarios anteriores.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




