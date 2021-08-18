---
title: Método AxWindowsMediaPlayer.newMedia
description: El método newMedia devuelve una interfaz IWMPMedia para un nuevo elemento multimedia.
ms.assetid: d10a517e-b4da-4f0b-9d51-9d387578d7dd
keywords:
- Método newMedia Reproductor de Windows Media
- Método newMedia Reproductor de Windows Media clase , AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Reproductor de Windows Media método , newMedia
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
ms.openlocfilehash: cdde19a6cb5da5113cb580c1916052c7ae0d38756bbc120368ffdfd464105591
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119618745"
---
# <a name="axwindowsmediaplayernewmedia-method"></a>Método AxWindowsMediaPlayer.newMedia

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

**System.String que** es la dirección URL del archivo multimedia digital que se usa para inicializar el nuevo elemento multimedia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Interfaz WMPLib.IWMPMedia que representa el elemento multimedia recién creado.

## <a name="remarks"></a>Comentarios

El *parámetro bstrURL* no debe ser una cadena de longitud cero ("") ni null.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPMedia (VB y C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





