---
description: El método SetRecompFormatFromSource establece el formato de recompresión de vídeo mediante el formato de compresión de un archivo de origen.
ms.assetid: 2d42876a-524b-454d-b4f1-353afe3a4d28
title: Método IAMTimelineGroup::SetRecompFormatFromSource (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetRecompFormatFromSource
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: adf4bfcf9d76ed40092eba7c612f4213c7aacb0d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126892036"
---
# <a name="iamtimelinegroupsetrecompformatfromsource-method"></a>Método IAMTimelineGroup::SetRecompFormatFromSource

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SetRecompFormatFromSource` método establece el formato de recompresión de vídeo mediante el formato de compresión de un archivo de origen.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetRecompFormatFromSource(
   IAMTimelineSrc *pSource
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSource* 
</dt> <dd>

Puntero a la [**interfaz IAMTimelineSrc**](iamtimelinesrc.md) del objeto de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve valores **HRESULT.** Estos son algunos de los valores posibles.



| Código devuelto                                                                                             | Descripción                                                                                            |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Correcto.<br/>                                                                                    |
| <dl> <dt>**E \_ NO \_ TIMELINE**</dt> </dl>          | El grupo no está dentro de una escala de tiempo.<br/>                                                         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>           | Memoria insuficiente.<br/>                                                                        |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>               | **Argumento de** puntero NULL.<br/>                                                                  |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Tipo de medio no válido. El grupo no es un grupo de vídeo o el archivo de origen no tiene ninguna secuencia de vídeo.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método busca el archivo de origen asociado a *pSource,* recupera el tipo de medio de la primera secuencia de vídeo del archivo y establece el formato de compresión de grupo con ese tipo. Para obtener más información sobre los formatos de compresión, [**vea IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md).

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

[**IAMTimelineGroup (interfaz)**](iamtimelinegroup.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




