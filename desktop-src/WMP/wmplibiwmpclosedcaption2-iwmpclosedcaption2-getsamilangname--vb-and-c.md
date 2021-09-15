---
title: Método IWMPClosedCaption2 getSAMILangName
description: El método getSAMILangName devuelve el nombre de un idioma admitido por el archivo SAMI actual.
ms.assetid: 52aaf1cc-89ef-4c4c-af43-3f88dc4a9539
keywords:
- Método getSAMILangName Reproductor de Windows Media
- Método getSAMILangName Reproductor de Windows Media , interfaz IWMPClosedCaption2
- Interfaz IWMPClosedCaption2 Reproductor de Windows Media , método getSAMILangName
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMILangName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e50df643fdd6b665de1275873fb8de9d5d094a42
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473316"
---
# <a name="iwmpclosedcaption2getsamilangname-method"></a>IWMPClosedCaption2::getSAMILangName (método)

El **método getSAMILangName** devuelve el nombre de un idioma admitido por el archivo SAMI actual.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String getSAMILangName(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMILangName( _
  ByVal nIndex As System.Int32 _
) As System.String
Implements IWMPClosedCaption2.getSAMILangName
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*nIndex* \[ En\]
</dt> <dd>

**System.Int32 que** es el índice de base cero del nombre de lenguaje que se va a recuperar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System.String que** es el nombre del idioma especificado en el archivo SAMI.

## <a name="remarks"></a>Observaciones

Los idiomas de un archivo SAMI se indexa en el orden que se muestra en el archivo, empezando por cero.

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

[**IWMPClosedCaption.SAMILang (VB y C#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPClosedCaption2 (VB y C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





