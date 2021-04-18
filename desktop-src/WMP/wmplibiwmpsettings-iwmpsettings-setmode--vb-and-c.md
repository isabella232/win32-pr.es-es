---
title: IWMPSettings setMode, método
description: El método setMode establece el modo de bucle o el modo de orden aleatorio en activo o inactivo.
ms.assetid: e9d3765e-6edb-47a5-ac97-5e00b62498c2
keywords:
- método setMode de Windows Media Player
- método setMode Windows Media Player, interfaz IWMPSettings
- Interfaz IWMPSettings Windows Media Player, método setMode
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
ms.openlocfilehash: f8dffede5e634c5c4f726cff1631b79781ed5179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718633"
---
# <a name="iwmpsettingssetmode-method"></a>IWMPSettings:: setMode (método)

El método **setMode** establece el modo de bucle o el modo de orden aleatorio en activo o inactivo.

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

*bstrMode* \[ de\]
</dt> <dd>

**System. String** que es el nombre del modo que se va a cambiar, que contiene uno de los valores siguientes.



| Value      | Descripción                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| autoRewind | Las pistas se reinician desde el principio después de la reproducción hasta el final.                                |
| bucle       | La secuencia de pistas se repite.                                                           |
| showFrame  | El fotograma clave más cercano se muestra cuando no se reproduce. Este modo no es relevante para las pistas de audio. |
| shuffle    | Las pistas se reproducen en orden aleatorio.                                                               |



 

</dd> <dt>

*varfMode* \[ de\]
</dt> <dd>

Un valor **System. Boolean** que especifica si el nuevo modo especificado está activo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Cuando el modo showFrame está activo, Windows Media Player debe tener acceso al contenido de Track para recuperar el fotograma de vídeo. Utilice este modo con precaución al reproducir contenido que no sea local.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPSettings (VB y C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. getMode (VB y C#)**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> </dl>

 

 





