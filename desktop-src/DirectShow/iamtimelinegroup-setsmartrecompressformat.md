---
description: El método SetSmartRecompressFormat especifica un formato de compresión de vídeo que se usará para la recompresión inteligente.
ms.assetid: 80c02215-6da2-4b3e-ab0d-004e49480fb9
title: Método IAMTimelineGroup::SetSmartRecompressFormat (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetSmartRecompressFormat
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8bf19ee67c08fc674681ade174966fe415a950103099011f52102e8c6edede7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083885"
---
# <a name="iamtimelinegroupsetsmartrecompressformat-method"></a>Método IAMTimelineGroup::SetSmartRecompressFormat

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SetSmartRecompressFormat` método especifica un formato de compresión de vídeo que se usará para la recompresión inteligente.

No se admite la recompresión inteligente para grupos de audio.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetSmartRecompressFormat(
   long *pFormat
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFormat* 
</dt> <dd>

Puntero a una estructura que describe el formato de compresión. Actualmente, solo la [**estructura SCompFmt0**](scompfmt0.md) es válida. Debe convertir este parámetro en un puntero de tipo **long**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Antes de llamar a este método, llame al método [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md) del mismo grupo para especificar un formato sin comprimir.

Si el `SetSmartRecompressFormat` método se realiza correctamente, puede usar el motor de representación inteligente para generar una secuencia de vídeo comprimida. El vídeo comprimido tendrá el ancho, el alto y la velocidad de fotogramas que se especificó en el *parámetro pFormat.* Estos valores invalidarán los especificados para el formato sin comprimir en el **método SetMediaType.** Sin embargo, para obtener las ventajas de la recompresión inteligente, los dos formatos deben coincidir. En otras palabras, los formatos comprimidos y sin comprimir deben tener el mismo alto, ancho y velocidad de fotogramas.

Si el motor de representación inteligente no puede generar el formato comprimido, producirá una secuencia de vídeo sin comprimir en su lugar. Si esto ocurre, el motor de representación inteligente notifica un error de representación DEX IDS CANT FIND DISPOSE durante el \_ \_ método \_ \_ [**IRenderEngine::ConnectFrontEnd.**](irenderengine-connectfrontend.md) La aplicación puede detectar este error a través del [**método IAMErrorLog::LogError.**](iamerrorlog-logerror.md) (Para obtener más información, vea [Errores de registro y](logging-errors.md) errores de [representación).](rendering-errors.md)

El formato de recompresión inteligente no es persistente. Si una aplicación usa la recompresión inteligente, debe establecer el formato de recompresión cada vez que cargue un archivo de proyecto.

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
</dt> <dt>

[Motor de representación inteligente](smart-render-engine.md)
</dt> <dt>

[Escribir un Project en un archivo](writing-a-project-to-a-file.md)
</dt> </dl>

 

 




