---
description: El método SetMediaType establece el tipo de medio sin comprimir para el grupo.
ms.assetid: 51778563-f119-42e0-826b-966324a85024
title: Método IAMTimelineGroup::SetMediaType (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8ac32439be94234ee612bce4f3c962839099bb8239a1cfc8b48222129680d01e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107825"
---
# <a name="iamtimelinegroupsetmediatype-method"></a>Método IAMTimelineGroup::SetMediaType

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SetMediaType` método establece el tipo de medio sin comprimir para el grupo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetMediaType(
  [in] AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pmt* \[ En\]
</dt> <dd>

Puntero a una [**estructura \_ AM MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) que describe el formato.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes **valores HRESULT:**



| Código devuelto                                                                                             | Descripción                                     |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Correcto.<br/>                             |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>               | **Argumento de** puntero NULL.<br/>           |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | El tipo de medio especificado no es válido.<br/> |



 

## <a name="remarks"></a>Comentarios

Se admiten los siguientes tipos de medios:

-   Vídeo RGB sin comprimir
-   16 bits por píxel, formato 555 (MEDIASUBTYPE \_ RGB555)
-   24 bits por píxel (MEDIASUBTYPE \_ RGB24)
-   32 bits por píxel, con alfa (MEDIASUBTYPE \_ ARGB32, no MEDIASUBTYPE \_ RGB32)
-   Audio PCM estéreo de 16 bits (MEDIASUBTYPE \_ PCM)

Los tipos de vídeo deben usar FORMAT \_ VideoInfo para el tipo de formato y [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) para el bloque de formato. No [**se admite el formato VIDEOINFOHEADER2.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) Además, no se admiten los formatos de vídeo de nivel superior *(biHeight* < 0).

Para especificar un formato de compresión para el grupo, llame al método [**IAMTimelineGroup::SetSmartRecompressFormat.**](iamtimelinegroup-setsmartrecompressformat.md)

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

[**IamTimelineGroup (interfaz)**](iamtimelinegroup.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




