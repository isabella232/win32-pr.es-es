---
title: AxWindowsMediaPlayer. newMedia, método
description: El método newMedia devuelve una interfaz IWMPMedia para un nuevo elemento multimedia.
ms.assetid: d10a517e-b4da-4f0b-9d51-9d387578d7dd
keywords:
- método newMedia de Windows Media Player
- método newMedia de Windows Media Player, clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Windows Media Player, método newMedia
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.newMedia
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 093a4e2b8181aac9148686108ad2c5c318a4d0cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699831"
---
# <a name="axwindowsmediaplayernewmedia-method"></a>AxWindowsMediaPlayer. newMedia, método

El método newMedia devuelve una interfaz IWMPMedia para un nuevo elemento multimedia.

## <a name="syntax"></a>Sintaxis


```CSharp
public IWMPMedia newMedia(
  System.String bstrURL
);
```


```VB

Public Function newMedia( _
  ByVal bstrURL As System.String _
) As IWMPMedia
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrURL* 
</dt> <dd>

**System. String** que es la dirección URL del archivo multimedia digital que se usa para inicializar el nuevo elemento multimedia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una interfaz WMPLib. IWMPMedia que representa el elemento multimedia que se acaba de crear.

## <a name="remarks"></a>Observaciones

El parámetro *bstrURL* no debe ser una cadena de longitud cero ("") o null.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPMedia (VB y C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





