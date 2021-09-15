---
description: Filtra la imagen de vista previa.
ms.assetid: 1710211a-a35c-4a51-b3bb-6f03f234f247
title: Método IWiaImageFilter::FilterPreviewImage (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.FilterPreviewImage
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 882aaf0d131ae6fe062c00c0181e2f913a0e1bc5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572289"
---
# <a name="iwiaimagefilterfilterpreviewimage-method"></a>IWiaImageFilter::FilterPreviewImage (método)

Filtra la imagen de vista previa.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FilterPreviewImage(
  [in] LONG      lFlags,
  [in] IWiaItem2 *pWiaChildItem2,
  [in] RECT      InputImageExtents,
  [in] IStream   *pInputStream
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lFlags* \[ En\]
</dt> <dd>

Tipo: **LONG**

No se utiliza. Establecer en 0.

</dd> <dt>

*pWiaChildItem2* \[ En\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

Elemento que se procesa.

</dd> <dt>

*InputImageExtents* \[ En\]
</dt> <dd>

Tipo: **RECT**

Coordenadas (en el área de adquisición física) de la imagen que el componente de vista previa almacena en caché internamente.

</dd> <dt>

*pInputStream* \[ En\]
</dt> <dd>

Tipo: **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\***

Puntero a la interfaz [IStream](/windows/win32/api/objidl/nn-objidl-istream) para los datos de imagen almacenados en caché que se filtran.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

No llame a este método directamente desde la aplicación.

*pWiaChildItem2* debe ser un elemento secundario de *pWiaItem2* que se pasó a [**IWiaImageFilter::InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md).

*InputImageExtents* es necesario porque el filtro de procesamiento de imágenes es responsable de cortar el área de imagen que *pWiaChildItem2* representa a partir de los datos de imagen pasados a través *de pInputStream*.

Una aplicación debe asegurarse de que *pWiaChildItem2* tiene el mismo formato de imagen (WIA \_ IPA FORMAT), resolución \_ (WIA IPS XRES y WIA IPS YRES) y profundidad de \_ \_ bits \_ \_ (WIA \_ IPA DEPTH) que tenía \_ *pWiaItem2* [](-wia-iwiapreview-getnewpreview.md)cuando se pasó a GetNewPreview .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
