---
title: IWMPSettings getMode, método
description: El método getMode devuelve un valor que indica si el modo de bucle o el modo de orden aleatorio está activo.
ms.assetid: a2e4bf74-017f-4c54-a3a1-a03b75a87a59
keywords:
- método getMode de Windows Media Player
- método getMode Windows Media Player, interfaz IWMPSettings
- Interfaz IWMPSettings Windows Media Player, método getMode
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
ms.openlocfilehash: 229cacf629410f958a062615cd5feb22be2ab0d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718757"
---
# <a name="iwmpsettingsgetmode-method"></a>IWMPSettings:: getMode (método)

El método **getMode** devuelve un valor que indica si el modo de bucle o el modo de orden aleatorio está activo.

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

*bstrMode* \[ de\]
</dt> <dd>

**System. String** que es uno de los valores siguientes.



| Value      | Descripción                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| autoRewind | Las pistas se reinician desde el principio después de la reproducción hasta el final.                                |
| bucle       | La secuencia de pistas se repite.                                                           |
| showFrame  | El fotograma clave más cercano se muestra cuando no se reproduce. Este modo no es relevante para las pistas de audio. |
| shuffle    | Las pistas se reproducen en orden aleatorio.                                                               |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Un valor **System. Boolean** que indica si el modo especificado está activo.

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

[**IWMPSettings. setMode (VB y C#)**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> </dl>

 

 





