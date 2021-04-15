---
description: Una aplicación llama al método PeriodicUpdatePicture para configurar un temporizador en la secuencia que pedirá actualizaciones de la imagen periódicamente. Las actualizaciones de imágenes causan un uso elevado de ancho de banda, por lo que este método se utilizará normalmente en lugar de UpdatePicture.
ms.assetid: 6ae3b5e9-bc11-4f3f-972b-21c9ac299987
title: IKeyFrameControl::P método eriodicUpdatePicture (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50bbfb18b0be96d611f0fe385cc825602dc316ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690007"
---
# <a name="ikeyframecontrolperiodicupdatepicture-method"></a>IKeyFrameControl::P método eriodicUpdatePicture

\[**PeriodicUpdatePicture** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

Una aplicación llama al método **PeriodicUpdatePicture** para configurar un temporizador en la secuencia que pedirá actualizaciones de la imagen periódicamente. Las actualizaciones de imágenes causan un uso elevado de ancho de banda, por lo que este método se utilizará normalmente en lugar de [**UpdatePicture**](ikeyframecontrol-updatepicture.md).

Si se llama al método cuando la secuencia está activa, el temporizador se iniciará inmediatamente. Si la secuencia no está activa, el temporizador se iniciará cuando la secuencia entre en el estado activo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PeriodicUpdatePicture(
  [in] BOOL  fEnable,
  [in] DWORD dwInterval
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fEnable* \[ de\]
</dt> <dd>

**True** habilita el temporizador. **False** lo deshabilita.

</dd> <dt>

*dwInterval* \[ de\]
</dt> <dd>

El intervalo del temporizador, en segundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                            | Descripción                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>   | El método se realizó correctamente.<br/>              |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | No se pudo realizar por motivos inesperados.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>H323priv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[H323 MSP](h323-msp.md)
</dt> </dl>

 

 




