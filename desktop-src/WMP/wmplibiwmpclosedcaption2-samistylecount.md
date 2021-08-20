---
title: Propiedad SAMIStyleCount de IWMPClosedCaption2
description: La propiedad SAMIStyleCount obtiene el número de estilos admitidos por el archivo SAMI actual.
ms.assetid: e2a0d194-6fa2-48c9-9fc7-0b60029d2e5d
keywords:
- Propiedad SAMIStyleCount Reproductor de Windows Media
- Propiedad SAMIStyleCount Reproductor de Windows Media , interfaz IWMPClosedCaption2
- Interfaz IWMPClosedCaption2 Reproductor de Windows Media , propiedad SAMIStyleCount
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.SAMIStyleCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f73ab4e252386f790f74741053012239d0219b1e296e392146894f906e1556f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115922"
---
# <a name="iwmpclosedcaption2samistylecount-property"></a>Propiedad IWMPClosedCaption2::SAMIStyleCount

La **propiedad SAMIStyleCount** obtiene el número de estilos admitidos por el archivo SAMI actual.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 SAMIStyleCount {get; set;}
```


```VB

Public ReadOnly Property SAMIStyleCount As System.Int32
```





## <a name="property-value"></a>Valor de propiedad

**System.Int32** que es el número de estilos.

## <a name="remarks"></a>Comentarios

Esta propiedad devuelve 0 a menos que un archivo multimedia digital esté abierto (AxWindowsMediaPlayer.openState es igual a 13).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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
</dt> <dt>

[**IWMPClosedCaption2.getSAMIStyleName (VB y C#)**](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamistylename--vb-and-c.md)
</dt> </dl>

 

 





