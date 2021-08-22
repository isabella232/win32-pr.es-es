---
description: El método SetPreviewMode establece el modo de vista previa del grupo.
ms.assetid: 40b7e9ac-30b3-454e-82ac-10ac99f1b86f
title: Método IAMTimelineGroup::SetPreviewMode (Qedit.h)
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
ms.openlocfilehash: 2f4c53372066ec28f3782fe53148eaba99489187c3be9b9ccf73195a7b1e6da9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756315"
---
# <a name="iamtimelinegroupsetpreviewmode-method"></a>Método IAMTimelineGroup::SetPreviewMode

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El método SetPreviewMode establece el modo de vista previa del grupo.

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

Modo de vista previa. Si **es TRUE,** el grupo está en modo de vista previa. Si **es FALSE,** el grupo está en modo de creación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

En el modo de vista previa, los fotogramas se descartan durante efectos lentos o transiciones para mantener el vídeo sincronizado con el audio. Como resultado, el vídeo podría parecer descortesado. En el modo de creación, se representa cada fotograma. El modo de creación es adecuado para escribir archivos; Para la versión preliminar en pantalla, es posible que el vídeo no esté sincronizado con el audio.

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAMTimelineGroup (interfaz)**](iamtimelinegroup.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




