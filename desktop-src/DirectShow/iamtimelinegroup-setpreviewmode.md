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
ms.openlocfilehash: fe03e6be3572b6cc660e51c27551a316db990d80
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126892052"
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

## <a name="remarks"></a>Observaciones

En el modo de vista previa, los fotogramas se descartan durante efectos lentos o transiciones para mantener el vídeo sincronizado con el audio. Como resultado, el vídeo podría parecer descortado. En el modo de creación, se representa cada fotograma. El modo de creación es adecuado para escribir archivos; Para la versión preliminar en pantalla, el vídeo podría estar sin sincronizar con el audio.

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IamTimelineGroup (interfaz)**](iamtimelinegroup.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




