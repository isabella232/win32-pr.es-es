---
description: El método SetSmartRecompressFormat especifica un formato de compresión de vídeo que se usará para la recompresión inteligente.
ms.assetid: 80c02215-6da2-4b3e-ab0d-004e49480fb9
title: 'IAMTimelineGroup:: SetSmartRecompressFormat (método) (QEDIT. h)'
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
ms.openlocfilehash: 9c8505f54d6ee9f6b2ec02216fd875fddbc619de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690788"
---
# <a name="iamtimelinegroupsetsmartrecompressformat-method"></a>IAMTimelineGroup:: SetSmartRecompressFormat (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `SetSmartRecompressFormat` método especifica un formato de compresión de vídeo que se utilizará para la recompresión inteligente.

La recompresión inteligente no es compatible con los grupos de audio.

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

Puntero a una estructura que describe el formato de compresión. Actualmente, solo la estructura [**SCompFmt0**](scompfmt0.md) es válida. Debe convertir este parámetro en un puntero de tipo **Long**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Antes de llamar a este método, llame al método [**IAMTimelineGroup:: SetMediaType**](iamtimelinegroup-setmediatype.md) en el mismo grupo para especificar un formato sin comprimir.

Si el `SetSmartRecompressFormat` método se ejecuta correctamente, puede usar el motor de representación inteligente para generar un flujo de vídeo comprimido. El vídeo comprimido tendrá el ancho, el alto y la velocidad de fotogramas que se especificó en el parámetro *pFormat* . Estos valores reemplazan a los que se proporcionan para el formato sin comprimir en el método **SetMediaType** . Sin embargo, para obtener las ventajas de la recompresión inteligente, los dos formatos deben coincidir. En otras palabras, los formatos comprimidos y sin comprimir deben tener el mismo alto, ancho y velocidad de fotogramas.

Si el motor de representación inteligente no puede generar el formato comprimido, producirá una secuencia de vídeo sin comprimir en su lugar. Si esto ocurre, el motor de representación inteligente informa de un error de representación del compresor de los identificadores de DEX en \_ \_ \_ \_ el método [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) . La aplicación puede detectar este error a través del método [**IAMErrorLog:: LogError**](iamerrorlog-logerror.md) . (Para obtener más información, vea [registrar errores](logging-errors.md) y [errores de representación](rendering-errors.md)).

El formato de recompresión inteligente no es persistente. Si una aplicación utiliza la recompresión inteligente, debe establecer el formato de recompresión cada vez que cargue un archivo de proyecto.

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
</dt> <dt>

[Smart Render Engine](smart-render-engine.md)
</dt> <dt>

[Escribir un proyecto en un archivo](writing-a-project-to-a-file.md)
</dt> </dl>

 

 




