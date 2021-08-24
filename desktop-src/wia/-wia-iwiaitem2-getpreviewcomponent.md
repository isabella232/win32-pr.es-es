---
description: Obtiene el Windows versión preliminar de adquisición de imágenes (WIA) 2.0.
ms.assetid: 0b773c4c-f080-41fa-8902-4243a80fc67c
title: Método IWiaItem2::GetPreviewComponent (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetPreviewComponent
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3ac3705b4be60ce53fee411df1142fb64bbd1c393864b644e260829080be8f81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450435"
---
# <a name="iwiaitem2getpreviewcomponent-method"></a>IWiaItem2::GetPreviewComponent (método)

Obtiene el Windows versión preliminar de adquisición de imágenes (WIA) 2.0.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetPreviewComponent(
  [in]  LONG        lFlags,
  [out] IWiaPreview **ppWiaPreview
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lFlags* \[ En\]
</dt> <dd>

Tipo: **LONG**

No se utiliza. Establecer en 0.

</dd> <dt>

*ppWiaPreview* \[ out\]
</dt> <dd>

Tipo: **[ **IWiaPreview**](-wia-iwiapreview.md)\*\***

Devuelve la dirección de un puntero a la [**interfaz IWiaPreview**](-wia-iwiapreview.md) del componente de vista previa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Use esta función para devolver un puntero a la dirección del componente de vista previa de WIA 2.0 para cualquier objeto [**IWiaItem2**](-wia-iwiaitem2.md) en el árbol de objetos de un dispositivo de hardware WIA 2.0.

Las aplicaciones deben llamar [al método IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros de interfaz que reciben a través del *parámetro ppWiaPreview.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWiaItem2**](-wia-iwiaitem2.md)
</dt> <dt>

[**IWiaPreview**](-wia-iwiapreview.md)
</dt> </dl>

 

 
