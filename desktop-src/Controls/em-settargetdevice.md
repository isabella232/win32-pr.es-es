---
title: Mensaje EM_SETTARGETDEVICE (RichEdit. h)
description: Establece el dispositivo de destino y el ancho de línea usados para \ 0034; lo que se ve es lo que se obtiene \ 0034; (WYSIWYG) formato en un control Rich Edit.
ms.assetid: dfc829f5-e711-419e-abb5-c1e8df994c4a
keywords:
- EM_SETTARGETDEVICE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETTARGETDEVICE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f82d6ee5df86572564cffcf192395ccee1fbd05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150464"
---
# <a name="em_settargetdevice-message"></a>\_Mensaje SETTARGETDEVICE em

Establece el dispositivo de destino y el ancho de línea que se usan para el formato de "lo que se ve es lo que se obtiene" (WYSIWYG) en un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

HDC para el dispositivo de destino.

</dd> <dt>

*lParam* 
</dt> <dd>

Ancho de línea que se va a usar para dar formato.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es cero si se produce un error en la operación, o es distinto de cero si se realiza correctamente.

## <a name="remarks"></a>Observaciones

La HDC para la impresora predeterminada se puede obtener como se indica a continuación.


```
PRINTDLG pd = { sizeof(pd) };
pd.Flags = PD_RETURNDC | PD_RETURNDEFAULT;
if (PrintDlg(&pd))
{
    HDC hdc = pd.hDC;
    ...
}
```



Si *lParam* es cero, no se crean saltos de línea.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





