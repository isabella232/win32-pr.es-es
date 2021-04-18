---
description: Filtra la imagen de vista previa.
ms.assetid: 1710211a-a35c-4a51-b3bb-6f03f234f247
title: 'IWiaImageFilter:: FilterPreviewImage (método) (WIA. h)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715344"
---
# <a name="iwiaimagefilterfilterpreviewimage-method"></a>IWiaImageFilter:: FilterPreviewImage (método)

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

*lFlags* \[ de\]
</dt> <dd>

Tipo: **Long**

No se utiliza. Establecer en 0.

</dd> <dt>

*pWiaChildItem2* \[ de\]
</dt> <dd>

Tipo: **[**IWiaItem2**](-wia-iwiaitem2.md) \** _

Elemento que se procesa.

</dd> <dt>

_InputImageExtents * \[ en\]
</dt> <dd>

Tipo: **Rect**

Las coordenadas (en el área de adquisición física) de la imagen que el componente de vista previa almacena internamente en caché.

</dd> <dt>

*pInputStream* \[ de\]
</dt> <dd>

Tipo: **[IStream](/windows/win32/api/objidl/nn-objidl-istream) \** _

Puntero a la interfaz [IStream](/windows/win32/api/objidl/nn-objidl-istream) para los datos de la imagen almacenada en caché que se filtran.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: _ *HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

No llame a este método directamente desde su aplicación.

*pWiaChildItem2* debe ser un elemento secundario del *pWiaItem2* que se pasó a [**IWiaImageFilter:: InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md).

*InputImageExtents* es necesario porque el filtro de procesamiento de imágenes es responsable de recortar el área de imagen que *pWiaChildItem2* representa de los datos de imagen pasados a través de *pInputStream*.

Una aplicación debe asegurarse de que *pWiaChildItem2* tiene el mismo formato de imagen \_ ( \_ formato de IPA de WIA), resolución (IP \_ de WIA \_ XRES y WIA \_ IPS \_ YRES) y profundidad de bits ( \_ \_ profundidad de IPA de WIA) que tenía *pWiaItem2* cuando se pasó a [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
