---
description: El método SetMediaType especifica el tipo de medio para la conexión en el PIN de entrada del enganche de ejemplo.
ms.assetid: 9568832f-6666-45c9-9421-485c877affb3
title: 'ISampleGrabber:: SetMediaType (método) (QEDIT. h)'
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
ms.openlocfilehash: a39aa79e9311fe3491d0925fdc1b2dd3b1cc65c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681047"
---
# <a name="isamplegrabbersetmediatype-method"></a>ISampleGrabber:: SetMediaType (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `SetMediaType` método especifica el tipo de medio para la conexión en el PIN de entrada del enganche de ejemplo.

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

Puntero a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) especifica el tipo de medio requerido. No es necesario establecer todos los miembros de la estructura; Vea la sección Comentarios para obtener más información.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

De forma predeterminada, el enganche de ejemplo no tiene ningún tipo de medio preferido. Para asegurarse de que el enganche de ejemplo se conecta al filtro correcto, llame a este método antes de generar el gráfico de filtro.

Este método restringe el intervalo de tipos de medios que el filtro aceptará. Cuando el filtro se conecta, intenta coincidir con el tipo de medio proporcionado en *pType*. Para ello, compara el tipo principal, el subtipo y los GUID de tipo de formato, en ese orden. Para cada uno de estos GUID, si *pType* tiene el valor \_ null GUID, el enganche de ejemplo acepta el tipo de medio sin ninguna comprobación adicional. Si *pType* tiene cualquier otro valor, el enganche del ejemplo lo compara con el GUID del tipo de conexión. A menos que los dos GUID coincidan exactamente, el enganche de ejemplo rechaza la conexión.

En el caso de los tipos de medios de vídeo, el enganche de ejemplo omite el bloque de formato. Por lo tanto, aceptará cualquier tamaño de vídeo y velocidad de fotogramas. Cuando llame a `SetMediaType` , establezca el bloque de formato (**pbFormat**) en **null** y el tamaño (**cbFormat**) en cero. En el caso de los tipos de medios de audio, el enganche de ejemplo examinará la estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) y requerirá que el otro filtro se conecte con ese formato, a menos que el bloque de formato de *pType* sea **null**, o la etiqueta de formato sea PCM con formato de onda \_ \_ y los demás miembros de la estructura sean cero.

Ejemplo 1:

-   Tipo principal: vídeo de MEDIATYPE \_
-   Subtipo: GUID \_ null
-   Tipo de formato: GUID \_ null

El enganche de ejemplo aceptará cualquier tipo de vídeo en el que el tipo principal sea igual a MEDIATYPE \_ vídeo. No comprobará el subtipo.

Ejemplo 2:

-   Tipo principal: vídeo de MEDIATYPE \_
-   Subtipo: MEDIASUBTYPE \_ RGB24
-   Tipo de formato: GUID \_ null

Ahora, el enganche de ejemplo comprobará el subtipo y solo aceptará el vídeo RGB 24.

**Limitaciones:** Independientemente del tipo que establezca, el filtro de enganche de ejemplo rechaza los tipos de vídeo con orientación de arriba abajo ( *biheight* negativo) o con un tipo de formato de formato \_ VideoInfo2. En este caso, aunque el `SetMediaType` método se ejecute correctamente, el filtro no se conectará.

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

[Usar el enganche de ejemplo](using-the-sample-grabber.md)
</dt> <dt>

[**Interfaz ISampleGrabber**](isamplegrabber.md)
</dt> </dl>

 

 
