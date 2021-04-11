---
description: Obtiene el componente de vista previa de la adquisición de imágenes de Windows (WIA) 2,0.
ms.assetid: 0b773c4c-f080-41fa-8902-4243a80fc67c
title: 'IWiaItem2:: GetPreviewComponent (método) (WIA. h)'
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
ms.openlocfilehash: 2e0881f68044c30731322c89d6cc2f19ce7277a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154398"
---
# <a name="iwiaitem2getpreviewcomponent-method"></a>IWiaItem2:: GetPreviewComponent (método)

Obtiene el componente de vista previa de la adquisición de imágenes de Windows (WIA) 2,0.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetPreviewComponent(
  [in]  LONG        lFlags,
  [out] IWiaPreview **ppWiaPreview
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lFlags* \[ de\]
</dt> <dd>

Tipo: **Long**

No se utiliza. Establecer en 0.

</dd> <dt>

*ppWiaPreview* \[ enuncia\]
</dt> <dd>

Tipo: **[ **IWiaPreview**](-wia-iwiapreview.md)\*\***

Devuelve la dirección de un puntero a la interfaz [**IWiaPreview**](-wia-iwiapreview.md) del componente de vista previa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Use esta función para devolver un puntero a la dirección del componente de vista previa de WIA 2,0 para cualquier objeto [**IWiaItem2**](-wia-iwiaitem2.md) en el árbol de objetos de un dispositivo de hardware WIA 2,0.

Las aplicaciones deben llamar al método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros de interfaz que reciben a través del parámetro *ppWiaPreview* .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWiaItem2**](-wia-iwiaitem2.md)
</dt> <dt>

[**IWiaPreview**](-wia-iwiapreview.md)
</dt> </dl>

 

 
