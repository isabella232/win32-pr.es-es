---
description: Desusado. El PenInputPanel se ha reemplazado por el panel de entrada de texto (TIP). Se produce cuando el foco de entrada cambia antes de que el objeto PenInputPanel pudiera insertar la entrada del usuario en el control adjunto.
ms.assetid: a5928f78-29d6-40e8-8f87-17c188e51ba9
title: Evento PenInputPanel. InputFailed (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 198c2b466dc03357d9851d7c8a6b7f44c6bf6884
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697818"
---
# <a name="peninputpanelinputfailed-event"></a>Evento PenInputPanel. InputFailed

En desuso. El [**PenInputPanel**](peninputpanel-class.md) se ha reemplazado por el [Panel de entrada de texto (TIP)](text-input-panel-reference.md).

Se produce cuando el foco de entrada cambia antes de que el objeto [**PenInputPanel**](peninputpanel-class.md) pudiera insertar la entrada del usuario en el control adjunto.

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

*hWnd* \[ de\]
</dt> <dd>

Identificador de ventana del control que invocó el objeto [**PenInputPanel**](peninputpanel-class.md) .

</dd> <dt>

*Clave* \[ de de\]
</dt> <dd>

La clave virtual correspondiente a la tecla presionada.

</dd> <dt>

*Texto* \[ de de\]
</dt> <dd>

Cadena que se va a insertar en el control representado por el parámetro *hWnd* cuando se generó el evento **InputFailed** .

Para obtener más información sobre el tipo de datos BSTR, vea [usar la biblioteca com](using-the-com-library.md).

</dd> <dt>

*ShiftKey* \[ de\]
</dt> <dd>

El estado de los modificadores de teclado, incluidos Mayús, Mayús, CTRL y ALT.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este evento se realiza correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

El evento **InputFailed** se produce cuando el foco de entrada cambia antes de que se insertara la entrada del usuario en el control adjunto. Por ejemplo, si el usuario escribe la entrada manuscrita en el panel de escritura y, a continuación, pulsa en otro control de edición antes de que el reconocedor haya tenido la oportunidad de finalizar, este evento se desencadena.

Con el identificador de ventana que se pasa a este evento, puede optar por insertar el texto usted mismo cuando se produce este evento.

> [!Note]  
> A partir de Microsoft Windows XP Tablet PC Edition 2005, el evento **InputFailed** ya no se aplica. El texto se inserta siempre antes de que cambie el foco.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PenInputPanel**](peninputpanel-class.md)
</dt> </dl>

 

 




