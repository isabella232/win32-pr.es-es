---
title: IWMPClosedCaption2 getSAMIStyleName, método
description: El método getSAMIStyleName devuelve el nombre de un estilo compatible con el archivo SAMI actual.
ms.assetid: e7678ca6-f52f-45f4-bd1c-7fbcdf1cc47c
keywords:
- método getSAMIStyleName de Windows Media Player
- método getSAMIStyleName Windows Media Player, interfaz IWMPClosedCaption2
- Interfaz IWMPClosedCaption2 Windows Media Player, método getSAMIStyleName
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMIStyleName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ceb3f598ae603d478af5cad9c78333952530a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690895"
---
# <a name="iwmpclosedcaption2getsamistylename-method"></a>IWMPClosedCaption2:: getSAMIStyleName (método)

El método **getSAMIStyleName** devuelve el nombre de un estilo compatible con el archivo Sami actual.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String getSAMIStyleName(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMIStyleName( _
  ByVal nIndex As System.Int32 _
) As System.String
Implements IWMPClosedCaption2.getSAMIStyleName
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*NINDEX* \[ de\]
</dt> <dd>

**System. Int32** que es el índice de base cero del nombre de estilo que se va a recuperar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System. String** que es el nombre del estilo tal y como se especifica en el archivo Sami.

## <a name="remarks"></a>Observaciones

Los estilos de un archivo SAMI se indizan en el orden mostrado en el archivo, empezando por cero.

Este método devuelve una cadena de longitud cero ("") a menos que haya un archivo multimedia digital abierto (AxWindowsMediaPlayer. openState es igual a 13).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Agregar subtítulos a medios digitales**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Interfaz IWMPClosedCaption (VB y C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption. SAMIStyle (VB y C#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-samistyle--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPClosedCaption2 (VB y C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





