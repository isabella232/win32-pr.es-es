---
title: Método IWMPClosedCaption2 getSAMIStyleName
description: El método getSAMIStyleName devuelve el nombre de un estilo admitido por el archivo SAMI actual.
ms.assetid: e7678ca6-f52f-45f4-bd1c-7fbcdf1cc47c
keywords:
- Método getSAMIStyleName Reproductor de Windows Media
- Método getSAMIStyleName Reproductor de Windows Media , interfaz IWMPClosedCaption2
- Interfaz IWMPClosedCaption2 Reproductor de Windows Media , método getSAMIStyleName
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
ms.openlocfilehash: cd599370afb9029a481fbae33264796232e4f129c1a5da0d2658452b785a870c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031355"
---
# <a name="iwmpclosedcaption2getsamistylename-method"></a>IWMPClosedCaption2::getSAMIStyleName (método)

El **método getSAMIStyleName** devuelve el nombre de un estilo admitido por el archivo SAMI actual.

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

*nIndex* \[ En\]
</dt> <dd>

**System.Int32 que** es el índice de base cero del nombre de estilo que se va a recuperar

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System.String que** es el nombre del estilo especificado en el archivo SAMI.

## <a name="remarks"></a>Comentarios

Los estilos de un archivo SAMI se indexa en el orden que se muestra en el archivo, empezando por cero.

Este método devuelve una cadena de longitud cero ("") a menos que un archivo multimedia digital esté abierto (AxWindowsMediaPlayer.openState es igual a 13).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Adición de subtítulos a medios digitales**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Interfaz IWMPClosedCaption (VB y C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption.SAMIStyle (VB y C#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-samistyle--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPClosedCaption2 (VB y C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





