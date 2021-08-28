---
title: Método getMode de IWMPSettings
description: El método getMode devuelve un valor que indica si el modo de bucle o el modo aleatorio están activos.
ms.assetid: a2e4bf74-017f-4c54-a3a1-a03b75a87a59
keywords:
- Método getMode Reproductor de Windows Media
- Método getMode Reproductor de Windows Media , interfaz IWMPSettings
- Interfaz IWMPSettings Reproductor de Windows Media , método getMode
topic_type:
- apiref
api_name:
- IWMPSettings.getMode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fae5d910dbbdf1fc2241a63dcf6c61c94e968cf0f2b36316407aafc8fc5f2dcf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119246305"
---
# <a name="iwmpsettingsgetmode-method"></a>IWMPSettings::getMode (método)

El **método getMode** devuelve un valor que indica si el modo de bucle o el modo aleatorio están activos.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Boolean getMode(
  System.String bstrMode
);
```


```VB

Public Function getMode( _
  ByVal bstrMode As System.String _
) As System.Boolean
Implements IWMPSettings.getMode
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrMode* \[ En\]
</dt> <dd>

**System.String que** es uno de los valores siguientes.



| Value      | Descripción                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| autoRewind | Las pistas se reinician desde el principio después de reproducir hasta el final.                                |
| bucle       | La secuencia de pistas se repite a sí misma.                                                           |
| showFrame  | Cuando no se reproduce, se muestra el fotograma clave más cercano. Este modo no es relevante para las pistas de audio. |
| shuffle    | Las pistas se reproducen en orden aleatorio.                                                               |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Valor **System.Boolean** que indica si el modo especificado está activo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPSettings (VB y C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.setMode (VB y C#)**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> </dl>

 

 





