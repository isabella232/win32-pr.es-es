---
description: Obtiene la imagen sin filtrar almacenada en caché por el método IWiaPreview::GetNewPreview.
ms.assetid: 121b6866-cca1-4170-9bdf-225491f942f5
title: Método IWiaPreview::UpdatePreview (Wia.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247634"
---
# <a name="iwiapreviewupdatepreview-method"></a>IWiaPreview::UpdatePreview (método)

Obtiene la imagen sin filtrar almacenada en caché por [**el método IWiaPreview::GetNewPreview.**](-wia-iwiapreview-getnewpreview.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UpdatePreview(
  [in] LONG      lOptions,
  [in] IWiaItem2 *pChildWiaItem
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lOptions* \[ En\]
</dt> <dd>

Tipo: **LONG**

Especifica si la aplicación requiere que el componente de versión preliminar de WIA 2.0 pase una subrecciones de la imagen almacenada en caché o toda la imagen almacenada en caché al filtro de procesamiento de imágenes.

<dt>

<span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>

<span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>**WiaPreviewReturnOriginalImage**


</dt> <dd>

Pase toda la imagen almacenada en caché al filtro de procesamiento de imágenes.

</dd> </dl> </dd> <dt>

*pChildWiaItem* \[ En\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

Especifica un puntero al elemento [**IWiaItem2,**](-wia-iwiaitem2.md) que es un elemento secundario del elemento **IWiaItem2** especificado por el *parámetro pWiaItem2* del método [**IWiaPreview::GetNewPreview.**](-wia-iwiapreview-getnewpreview.md) O bien, si la aplicación requiere una vista previa de todo el plano, especifica un puntero al *parámetro pWiaItem2* del método **IWiaPreview::GetNewPreview.** Cuando *pChildWiaItem* es un elemento secundario del parámetro *pWiaItem2* de **IWiaPreview::GetNewPreview,** el filtro de segmentación suele crear este elemento secundario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Este método pasa la imagen almacenada en caché sin filtrar a través del filtro de procesamiento de imágenes, que luego escribe los datos filtrados en el flujo proporcionado por la aplicación. El componente de versión preliminar de WIA 2.0 recupera esta secuencia mediante una llamada al método [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) del filtro de procesamiento de imágenes, que luego llama a la implementación **GetNextStream** de la devolución de llamada de la aplicación. Antes de llamar a **IWiaPreview::UpdatePreview**, una aplicación debe llamar primero a [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) para adquirir la imagen del analizador; De lo contrario, el método devuelve un error.

El componente de versión preliminar de WIA 2.0 almacena la imagen sin filtrar descargada del controlador. Es posible que el elemento de WIA 2.0 pasado a **IWiaPreview::UpdatePreview** represente solo una pequeña región de la imagen descargada desde el controlador. Si este es el caso, el componente de versión preliminar de WIA 2.0 realmente elimina esta región de la imagen almacenada en caché antes de pasarla al filtro de procesamiento de imágenes, que a su vez pasa los datos filtrados de la imagen a la aplicación.

Para que una aplicación pase toda la imagen almacenada en caché al filtro de procesamiento de imágenes (que a su vez la pasa a la aplicación), debe establecer *lOptions* en **WiaPreviewReturnOriginalImage** al llamar a **IWiaPreview::UpdatePreview**. Al establecer *lOptions* en **WiaPreviewReturnOriginalImage,** la aplicación debe asegurarse de que la configuración de extensión [**(WIA \_ IPS \_ XEXTENT**](-wia-wiaitempropscanneritem.md) y **WIA \_ IPS \_ YEXTENT)** del elemento pasado a **IWiaPreview::UpdatePreview** coincide con la imagen almacenada en caché completa. En este caso, el filtro de procesamiento de imágenes no necesita hacer nada diferente. simplemente filtra la imagen, en función de las propiedades de *pChildWiaItem* (normalmente, *pChildWiaItem* es el mismo elemento que se pasó a [**IWiaPreview::GetNewPreview).**](-wia-iwiapreview-getnewpreview.md) Las distintas subrecciones se omiten y toda la imagen se filtra con la misma configuración. Hay un par de razones por las que una aplicación haría esto.

1.  Es posible que la aplicación no admita el cambio de la configuración (como [**WIA \_ IPS \_ BRIGHTNESS**](-wia-wiaitempropscanneritem.md) y **WIA \_ IPS \_ CONTRAST)** individualmente para cada región que detecte el filtro de segmentación (o es posible que ni siquiera quiera usar el filtro de segmentación). Es más fácil para la aplicación llamar a **IWiaPreview::UpdatePreview** con **WiaPreviewReturnOriginalImage** para que siempre reciba la imagen completa del componente de versión preliminar de WIA 2.0.
2.  El componente de versión preliminar de WIA 2.0 no admite el formato de imagen de la imagen de vista previa, en cuyo caso no puede realizar las acciones para cortar la región deseada. La compatibilidad con el formato de imagen del componente de vista previa de WIA 2.0 se limita a los formatos para los que Windows GDI+ codificadores y descodificadores 1.1. Estos formatos son bitmap (BMP) (mapa de bits que incluye BITMAPFILEHEADER), Formato de intercambio de gráficos (GIF), JPEG, Portable Network Graphics (PNG) y Tagged Image File Format (TIFF).

Tenga en cuenta que si la aplicación pasa **WiaPreviewReturnOriginalImage** a **IWiaPreview::UpdatePreview,** el componente de vista previa de WIA 2.0 puede admitir cualquier formato de imagen o píxel.

**IWiaPreview::UpdatePreview** establece la propiedad [**WIA \_ DPS \_ PREVIEW**](-wia-wiaitempropscannerdevice.md) (y la restablece antes de que vuelva, a menos que se haya establecido antes). Esto permite que el controlador (y el hardware), así como el filtro de procesamiento de imágenes, sepan que el elemento es un examen de vista previa.

Una aplicación debe asegurarse de que *pChildWiaItem* tiene el mismo formato de imagen [**(WIA \_ IPA \_ FORMAT**](-wia-wiaitempropcommonitem.md)) y resolución [**(WIA \_ IPS \_ XRES**](-wia-wiaitempropscanneritem.md) y **WIA \_ IPS \_ YRES)** que *pWiaItem* tenía cuando se pasó a [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md). El formato del elemento secundario debe corresponder al formato de la imagen almacenada en caché del componente de versión preliminar de WIA 2.0 (el componente de versión preliminar de WIA 2.0 no realiza ninguna conversión de imagen).

## <a name="examples"></a>Ejemplos

Se debe llamar a UpdateRegion cada vez que un usuario cambia, por ejemplo, el brillo o el contraste del elemento secundario representado por `dwRegionNumber` . Este elemento secundario se ha creado previamente mediante el filtro de segmentación ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md). El método [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) de la interfaz de devolución de llamada de transferencia devuelve la imagen escrita en [IStream.](/windows/win32/api/objidl/nn-objidl-istream) El código de GetSubRegionItem se omite en este ejemplo.

Una vez que se ha llamado a esta función, una aplicación normalmente vuelve a dibujar la región en la pantalla.


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
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
