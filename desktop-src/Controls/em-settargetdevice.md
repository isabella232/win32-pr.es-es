---
title: EM_SETTARGETDEVICE mensaje (Richedit.h)
description: Establece el dispositivo de destino y el ancho de línea que se usa para \ 0034; lo que ve es lo que obtiene \ 0034; (WYSIWYG) formato en un control de edición enriquecido.
ms.assetid: dfc829f5-e711-419e-abb5-c1e8df994c4a
keywords:
- EM_SETTARGETDEVICE controles de Windows mensaje
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
ms.openlocfilehash: 2d9a3cd4e59f3800b91fedee446e927ab0ec39988474752561a04dace5572ef0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697595"
---
# <a name="em_settargetdevice-message"></a>Mensaje \_ EM SETTARGETDEVICE

Establece el dispositivo de destino y el ancho de línea usados para el formato "lo que se ve es lo que se obtiene" (WYSIWYG) en un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

HDC para el dispositivo de destino.

</dd> <dt>

*lParam* 
</dt> <dd>

Ancho de línea que se usará para el formato.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es cero si se produce un error en la operación o distinto de cero si se realiza correctamente.

## <a name="remarks"></a>Comentarios

El HDC de la impresora predeterminada se puede obtener como se muestra a continuación.


```
PRINTDLG pd = { sizeof(pd) };
pd.Flags = PD_RETURNDC | PD_RETURNDEFAULT;
if (PrintDlg(&pd))
{
    HDC hdc = pd.hDC;
    ...
}
```



Si *lParam es* cero, no se crea ningún salto de línea.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 





