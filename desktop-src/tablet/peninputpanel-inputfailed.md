---
description: Desusado. PenInputPanel se ha reemplazado por el Panel de entrada de texto (TIP). Se produce cuando el foco de entrada cambia antes de que el objeto PenInputPanel pueda insertar la entrada del usuario en el control adjunto.
ms.assetid: a5928f78-29d6-40e8-8f87-17c188e51ba9
title: Evento PenInputPanel.InputFailed (Mspanel.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cc3234c73fc8ba47faa7d1f2ec89477a1bfb86b7c2abda263aff227c5961f1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934765"
---
# <a name="peninputpanelinputfailed-event"></a>PenInputPanel.InputFailed, evento

En desuso. [**PenInputPanel se**](peninputpanel-class.md) ha reemplazado por el [Panel de entrada de texto (TIP).](text-input-panel-reference.md)

Se produce cuando el foco de entrada cambia antes [**de que el objeto PenInputPanel**](peninputpanel-class.md) fuera capaz de insertar la entrada del usuario en el control adjunto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT InputFailed(
  [in] long  hWnd,
  [in] long  Key,
  [in] BSTR  Text,
  [in] short ShiftKey
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hWnd* \[ En\]
</dt> <dd>

Identificador de ventana del control que invocó el [**objeto PenInputPanel.**](peninputpanel-class.md)

</dd> <dt>

*Clave* \[ En\]
</dt> <dd>

Tecla virtual correspondiente a la tecla presionada.

</dd> <dt>

*Texto* \[ En\]
</dt> <dd>

Cadena que se va a insertar en el control representado por el *parámetro hWnd* cuando se presentó el evento **InputFailed.**

Para obtener más información sobre el tipo de datos BSTR, vea [Uso de la biblioteca COM](using-the-com-library.md).

</dd> <dt>

*MayúsKey* \[ En\]
</dt> <dd>

Estado de los modificadores de teclado, incluidos MAYÚS, CAPS, CTRL y ALT.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este evento se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

El **evento InputFailed** tiene lugar cuando cambia el foco de entrada antes de insertar la entrada del usuario en el control adjunto. Por ejemplo, si el usuario escribe entrada de lápiz en el panel de escritura, pulsa otro control de edición antes de que el reconocedor haya tenido la oportunidad de finalizar, se produce este evento.

Con el identificador de ventana pasado a este evento, puede elegir insertar el texto usted mismo cuando se produzca este evento.

> [!Note]  
> A partir de Microsoft Windows XP Tablet PC Edition 2005, el **evento InputFailed** ya no se aplica. El texto siempre se inserta antes de que cambie el foco.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PenInputPanel**](peninputpanel-class.md)
</dt> </dl>

 

 




