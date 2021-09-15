---
title: Método IWMPClosedCaption2 getSAMILangID
description: El método getSAMILangID devuelve el identificador de configuración regional (LCID) de un idioma admitido por el archivo SAMI actual.
ms.assetid: 41aca317-6182-47c3-8bd9-ba42b92b10f4
keywords:
- Método getSAMILangID Reproductor de Windows Media
- Método getSAMILangID Reproductor de Windows Media , interfaz IWMPClosedCaption2
- Interfaz IWMPClosedCaption2 Reproductor de Windows Media método , getSAMILangID
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMILangID
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb9aaebecf8e86c056fa9c91141042facc6bcc18
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473319"
---
# <a name="iwmpclosedcaption2getsamilangid-method"></a>IWMPClosedCaption2::getSAMILangID (método)

El **método getSAMILangID** devuelve el identificador de configuración regional (LCID) de un idioma admitido por el archivo SAMI actual.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Int32 getSAMILangID(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMILangID( _
  ByVal nIndex As System.Int32 _
) As System.Int32
Implements IWMPClosedCaption2.getSAMILangID
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*nIndex* \[ En\]
</dt> <dd>

**System.Int32 que** es el índice de base cero del LCID que se va a recuperar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System.Int32** que es el LCID del idioma con el índice especificado.

## <a name="remarks"></a>Observaciones

Los idiomas de un archivo SAMI se indexa en el orden que se muestra en el archivo, empezando por cero.

Este método devuelve 0 a menos que un archivo multimedia digital esté abierto (AxWindowsMediaPlayer.openState es igual a 13).

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

[**Interfaz IWMPClosedCaption2 (VB y C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





