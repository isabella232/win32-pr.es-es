---
title: Método setMode de IWMPSettings
description: El método setMode establece el modo de bucle o el modo aleatorio en activo o inactivo.
ms.assetid: e9d3765e-6edb-47a5-ac97-5e00b62498c2
keywords:
- Método setMode Reproductor de Windows Media
- Método setMode Reproductor de Windows Media , interfaz IWMPSettings
- Interfaz IWMPSettings Reproductor de Windows Media método , setMode
topic_type:
- apiref
api_name:
- IWMPSettings.setMode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 529aadf412cdae869ae3c308d82dcd08a7dfd581aeb7ecc711052f6acd54b962
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568412"
---
# <a name="iwmpsettingssetmode-method"></a>IWMPSettings::setMode (método)

El **método setMode** establece el modo de bucle o el modo aleatorio en activo o inactivo.

## <a name="syntax"></a>Sintaxis


```CSharp
public void setMode(
  System.String bstrMode,
  System.Boolean varfMode
);
```


```VB

Public Sub setMode( _
  ByVal bstrMode As System.String, _
  ByVal varfMode As System.Boolean _
)
Implements IWMPSettings.setMode
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrMode* \[ En\]
</dt> <dd>

**System.String que** es el nombre del modo que se va a cambiar y que contiene uno de los valores siguientes.



| Valor      | Descripción                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| autoRewind | Las pistas se reinician desde el principio después de reproducir hasta el final.                                |
| bucle       | La secuencia de pistas se repite a sí misma.                                                           |
| showFrame  | Cuando no se reproduce, se muestra el fotograma clave más cercano. Este modo no es relevante para las pistas de audio. |
| shuffle    | Las pistas se reproducen en orden aleatorio.                                                               |



 

</dd> <dt>

*varfMode* \[ En\]
</dt> <dd>

Valor **System.Boolean** que especifica si el nuevo modo especificado está activo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Cuando el modo showFrame está activo, Reproductor de Windows Media acceder al contenido de la pista para recuperar el fotograma de vídeo. Use este modo con precaución al reproducir contenido que no es local.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaz IWMPSettings (VB y C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.getMode (VB y C#)**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> </dl>

 

 





