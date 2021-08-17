---
description: El método SetMediaType especifica el tipo de medio para la conexión en la patilla de entrada del sample grabber.
ms.assetid: 9568832f-6666-45c9-9421-485c877affb3
title: Método ISampleGrabber::SetMediaType (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 060ff0cc10fed441fdb2d6f2bf1bd0e66f3e8b9facec3cb52d8f270b350b1f4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817706"
---
# <a name="isamplegrabbersetmediatype-method"></a>ISampleGrabber::SetMediaType (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SetMediaType` método especifica el tipo de medio para la conexión en la patilla de entrada del sample grabber.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetMediaType(
   const AM_MEDIA_TYPE *pType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pType* 
</dt> <dd>

Puntero a una [**estructura \_ AM MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) especifica el tipo de medio necesario. No es necesario establecer todos los miembros de la estructura; Vea Comentarios para obtener más información.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

De forma predeterminada, Sample Grabber no tiene ningún tipo de medio preferido. Para asegurarse de que sample Grabber se conecta al filtro correcto, llame a este método antes de compilar el gráfico de filtros.

Este método restringe el intervalo de tipos de medios que aceptará el filtro. Cuando se conecta el filtro, intenta coincidir con el tipo de medio especificado en *pType*. Para ello, compara los GUID de tipo principal, subtipo y tipo de formato, en ese orden. Para cada uno de estos GUID, si *pType* tiene el valor GUID NULL, sample Grabber acepta el tipo de medio \_ sin más comprobaciones. Si *pType* tiene cualquier otro valor, sample Grabber lo compara con el GUID del tipo de conexión. A menos que los dos GUID coincidan exactamente, sample Grabber rechaza la conexión.

En el caso de los tipos de medios de vídeo, sample Grabber omite el bloque de formato. Por lo tanto, aceptará cualquier tamaño de vídeo y velocidad de fotogramas. Al llamar a `SetMediaType` , establezca el bloque de formato (**pbFormat**) en **NULL** y el tamaño (**cbFormat**) en cero. En el caso de los tipos de medios de audio, sample Grabber examinará la estructura [**WAVEATEX**](/previous-versions/dd757713(v=vs.85)) y requerirá que el otro filtro se conecte con ese formato, a menos que el bloque de formato de *pType* sea **NULL** o que la etiqueta de formato sea WAVE FORMAT PCM y los demás miembros de la estructura \_ sean \_ cero.

Ejemplo 1:

-   Tipo principal: VÍDEO \_ MEDIATYPE
-   Subtipo: GUID \_ NULL
-   Tipo de formato: GUID \_ NULL

Sample Grabber aceptará cualquier tipo de vídeo en el que el tipo principal sea igual a MEDIATYPE \_ Video. No comprobará el subtipo.

Ejemplo 2:

-   Tipo principal: VÍDEO \_ MEDIATYPE
-   Subtipo: MEDIASUBTYPE \_ RGB24
-   Tipo de formato: GUID \_ NULL

Ahora, Sample Grabber comprobará el subtipo y solo aceptará vídeo RGB 24.

**Limitaciones:** Independientemente del tipo que establezca, el filtro sample grabber rechaza cualquier tipo de vídeo con orientación de arriba abajo *(biHeight* negativo) o con un tipo de formato FORMAT \_ VideoInfo2. En este caso, aunque el `SetMediaType` método se realiza correctamente, el filtro no se conectará.

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

[Uso de Sample Grabber](using-the-sample-grabber.md)
</dt> <dt>

[**ISampleGrabber (interfaz)**](isamplegrabber.md)
</dt> </dl>

 

 
