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
ms.openlocfilehash: 8f82d6ee5df86572564cffcf192395ccee1fbd05
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062059"
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

## <a name="remarks"></a>Observaciones

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



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 





