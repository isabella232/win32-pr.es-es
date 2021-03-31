---
description: 'Obtiene la imagen sin filtrar almacenada en memoria caché por el método IWiaPreview:: GetNewPreview.'
ms.assetid: 121b6866-cca1-4170-9bdf-225491f942f5
title: 'IWiaPreview:: UpdatePreview (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.UpdatePreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 4a5d469179f341f3bad5d2b9b5ed25a5715be694
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154396"
---
# <a name="iwiapreviewupdatepreview-method"></a>IWiaPreview:: UpdatePreview (método)

Obtiene la imagen sin filtrar almacenada en memoria caché por el método [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UpdatePreview(
  [in] LONG      lOptions,
  [in] IWiaItem2 *pChildWiaItem
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lOptions* \[ de\]
</dt> <dd>

Tipo: **Long**

Especifica si la aplicación requiere que el componente de vista previa de WIA 2,0 pase una subregión de la imagen almacenada en caché o toda la imagen almacenada en caché al filtro de procesamiento de imágenes.

<dt>

<span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>

<span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>**WiaPreviewReturnOriginalImage**


</dt> <dd>

Pase toda la imagen almacenada en caché al filtro de procesamiento de imágenes.

</dd> </dl> </dd> <dt>

*pChildWiaItem* \[ de\]
</dt> <dd>

Tipo: **[**IWiaItem2**](-wia-iwiaitem2.md) \** _

Especifica un puntero al elemento [_ *IWiaItem2* *](-wia-iwiaitem2.md) , que es un elemento secundario del elemento **IWiaItem2** especificado por el parámetro *pWiaItem2* del método [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) . O bien, si la aplicación requiere una vista previa de todo el plano, especifica un puntero al parámetro *pWiaItem2* del método **IWiaPreview:: GetNewPreview** . Cuando *pChildWiaItem* es un elemento secundario del parámetro *pWiaItem2* de **IWiaPreview:: GetNewPreview**, este elemento secundario se crea normalmente mediante el filtro de segmentación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Este método pasa la imagen almacenada en caché sin filtrar a través del filtro de procesamiento de imágenes, que después escribe los datos filtrados en la secuencia proporcionada por la aplicación. El componente de vista previa de WIA 2,0 recupera esta secuencia llamando al método [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) del filtro de procesamiento de imágenes, que luego llama a la implementación de **GetNextStream** de la devolución de llamada de la aplicación. Antes de llamar a **IWiaPreview:: UpdatePreview**, una aplicación debe llamar primero a [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) para adquirir la imagen del escáner. de lo contrario, el método devuelve un error.

El componente WIA 2,0 Preview almacena la imagen sin filtrar descargada del controlador. Es posible que el elemento de WIA 2,0 pasado a **IWiaPreview:: UpdatePreview** represente solo una pequeña región de la imagen descargada del controlador. Si este es el caso, el componente de vista previa de WIA 2,0 descompone realmente esta región de la imagen almacenada en caché antes de pasarla al filtro de procesamiento de imágenes, que a su vez pasa los datos de la imagen filtrada de nuevo a la aplicación.

Para que una aplicación pase toda la imagen almacenada en caché al filtro de procesamiento de imágenes (que a su vez la pasa a la aplicación), debe establecer *lOptions* en **WiaPreviewReturnOriginalImage** al llamar a **IWiaPreview:: UpdatePreview**. Al establecer *lOptions* en **WiaPreviewReturnOriginalImage**, la aplicación debe asegurarse de que la configuración de extensión ([**IP de WIA \_ IP \_ XEXTENT**](-wia-wiaitempropscanneritem.md) y **WIA \_ IP \_ YEXTENT**) del elemento pasado a **IWiaPreview:: UpdatePreview** coincide con la imagen almacenada en caché completa. El filtro de procesamiento de imágenes no necesita hacer nada diferente en este caso; simplemente filtra la imagen, en función de las propiedades de *pChildWiaItem* (normalmente, en este caso, *pChildWiaItem* es el mismo elemento que se pasó a [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md)). Se omiten las distintas subregiones y se filtra toda la imagen con la misma configuración. Hay un par de razones por las que una aplicación lo haría.

1.  Es posible que la aplicación no admita el cambio de la configuración (por ejemplo, el contraste de [**\_ IP \_**](-wia-wiaitempropscanneritem.md) de WIA y el contraste de las **\_ direcciones \_ IP de WIA**) individualmente para cada región detectada por el filtro de segmentación (o incluso puede que no desee usar el filtro de segmentación). Es más fácil que la aplicación llame a **IWiaPreview:: UpdatePreview** con **WiaPreviewReturnOriginalImage** para que siempre reciba la imagen completa del componente de vista previa de WIA 2,0.
2.  El componente de vista previa de WIA 2,0 no admite el formato de imagen de la imagen de vista previa, en cuyo caso no puede realizar las acciones para cortar la región deseada. La compatibilidad con el formato de imagen del componente de vista previa de WIA 2,0 está limitada a formatos para los que hay codificadores y descodificadores de Windows GDI+ 1,1. Estos formatos son Bitmap (BMP) (un mapa de bits que incluye BITMAPFILEHEADER), formato de intercambio de gráficos (GIF), JPEG, Portable Network Graphics (PNG) y Tagged Image File Format (TIFF).

Tenga en cuenta que si la aplicación pasa **WiaPreviewReturnOriginalImage** a **IWiaPreview:: UpdatePreview**, el componente de vista previa de WIA 2,0 puede admitir cualquier formato de imagen o píxel.

**IWiaPreview:: UpdatePreview** establece la propiedad de [**\_ \_ vista previa de DPS de WIA**](-wia-wiaitempropscannerdevice.md) (y lo restablece antes de que se devuelva, a menos que se haya establecido antes). Esto permite que el controlador (y el hardware) y el filtro de procesamiento de imágenes sepan que el elemento es un examen de vista previa.

Una aplicación debe asegurarse de *que pChildWiaItem* tenga el mismo formato de imagen ([**\_ \_ formato de IPA de WIA**](-wia-wiaitempropcommonitem.md)) y la resolución (IP de [**WIA \_ \_ XRES**](-wia-wiaitempropscanneritem.md) y **WIA \_ IPS \_ YRES**) que tenía *pWiaItem* cuando se pasó a [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md). El formato del elemento secundario debe coincidir con el formato de la imagen almacenada en caché del componente WIA 2,0 Preview (el componente WIA 2,0 Preview no realiza ninguna conversión de imagen).

## <a name="examples"></a>Ejemplos

Se debe llamar a UpdateRegion cada vez que un usuario cambia, por ejemplo, el brillo o el contraste del elemento secundario representado por `dwRegionNumber` . Este elemento secundario se ha creado anteriormente con el filtro de segmentación ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md). La imagen escrita en [IStream](/windows/win32/api/objidl/nn-objidl-istream) se devuelve mediante el método [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) de la interfaz de devolución de llamada de transferencia. El código de GetSubRegionItem se omite en este ejemplo.

Después de llamar a esta función, una aplicación normalmente volvería a dibujar la región en la pantalla.


```C++
HRESULT
UpdateRegion(
   IN  DWORD dwRegionNumber)
{
   IWiaItem2 *pSubRegion = GetSubRegionItem(dwRegionNumber);

   return m_pWiaPreview->UpdatePreview(0,pSubRegion);
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
