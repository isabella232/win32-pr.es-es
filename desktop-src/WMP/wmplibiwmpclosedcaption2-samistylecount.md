---
title: Propiedad SAMIStyleCount de IWMPClosedCaption2
description: La propiedad SAMIStyleCount obtiene el número de estilos admitidos por el archivo SAMI actual.
ms.assetid: e2a0d194-6fa2-48c9-9fc7-0b60029d2e5d
keywords:
- Propiedades de SAMIStyleCount Media Player de Windows
- Propiedad SAMIStyleCount de Windows Media Player, interfaz IWMPClosedCaption2
- Interfaz IWMPClosedCaption2 Windows Media Player, propiedad SAMIStyleCount
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
ms.openlocfilehash: ff361b4c6d34f63e86e3d8458bff4d3308cae29f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690892"
---
# <a name="iwmpclosedcaption2samistylecount-property"></a>IWMPClosedCaption2:: SAMIStyleCount (propiedad)

La propiedad **SAMIStyleCount** obtiene el número de estilos admitidos por el archivo Sami actual.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Int32 SAMIStyleCount {get; set;}
```


```VB

Public ReadOnly Property SAMIStyleCount As System.Int32
```





## <a name="property-value"></a>Valor de propiedad

**System. Int32** que es el número de estilos.

## <a name="remarks"></a>Observaciones

Esta propiedad devuelve 0 a menos que haya un archivo multimedia digital abierto (AxWindowsMediaPlayer. openState es igual a 13).

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
</dt> <dt>

[**IWMPClosedCaption2. getSAMIStyleName (VB y C#)**](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamistylename--vb-and-c.md)
</dt> </dl>

 

 





