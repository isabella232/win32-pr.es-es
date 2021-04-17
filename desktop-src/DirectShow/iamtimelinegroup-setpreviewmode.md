---
description: El método SetPreviewMode establece el modo de vista previa para el grupo.
ms.assetid: 40b7e9ac-30b3-454e-82ac-10ac99f1b86f
title: 'IAMTimelineGroup:: SetPreviewMode (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetPreviewMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fe03e6be3572b6cc660e51c27551a316db990d80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690789"
---
# <a name="iamtimelinegroupsetpreviewmode-method"></a>IAMTimelineGroup:: SetPreviewMode (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El método SetPreviewMode establece el modo de vista previa para el grupo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetPreviewMode(
   BOOL fPreview
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fPreview* 
</dt> <dd>

El modo de vista previa. Si es **true**, el grupo está en modo de vista previa. Si es **false**, el grupo está en modo de creación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

En el modo de vista previa, los fotogramas se quitan durante los efectos lentos o las transiciones para mantener el vídeo sincronizado con el audio. Es posible que el vídeo parezca entrecortado como resultado. En el modo de creación, se representan todos los fotogramas. El modo de creación es adecuado para escribir archivos; en la vista previa en pantalla, es posible que el vídeo no esté sincronizado con el audio.

> [!Note]  
> El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>QEDIT. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IAMTimelineGroup**](iamtimelinegroup.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




