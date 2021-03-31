---
title: Mensaje de HKM_SETRULES (commctrl. h)
description: Define las combinaciones no válidas y la combinación de modificadores predeterminados para un control de tecla de acceso rápido.
ms.assetid: de3dd463-a534-4c7c-ae04-da80a3bff2ab
keywords:
- HKM_SETRULES controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HKM_SETRULES
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c33c0918a7bb44fdac9a1f2c60fdde8e06b5e679
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491188"
---
# <a name="hkm_setrules-message"></a>HKM \_ SETRULES

Define las combinaciones no válidas y la combinación de modificadores predeterminados para un control de tecla de acceso rápido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Matriz de marcas que especifican combinaciones de teclas no válidas. Este parámetro puede ser una combinación de los siguientes valores:



| Value                                                                                                                                                   | Significado                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span id="HKCOMB_A"></span><span id="hkcomb_a"></span><dl> <dt>**HKCOMB \_ A**</dt> </dl>          | ALT<br/>             |
| <span id="HKCOMB_C"></span><span id="hkcomb_c"></span><dl> <dt>**HKCOMB \_ C**</dt> </dl>          | CTRL<br/>            |
| <span id="HKCOMB_CA"></span><span id="hkcomb_ca"></span><dl> <dt>**HKCOMB \_ CA**</dt> </dl>       | CTRL + ALT<br/>        |
| <span id="HKCOMB_NONE"></span><span id="hkcomb_none"></span><dl> <dt>**HKCOMB \_ ninguno**</dt> </dl> | Claves sin modificar<br/> |
| <span id="HKCOMB_S"></span><span id="hkcomb_s"></span><dl> <dt>**HKCOMB \_ S**</dt> </dl>          | Mayús<br/>           |
| <span id="HKCOMB_SA"></span><span id="hkcomb_sa"></span><dl> <dt>**SA de HKCOMB \_**</dt> </dl>       | MAYÚS+ALT<br/>       |
| <span id="HKCOMB_SC"></span><span id="hkcomb_sc"></span><dl> <dt>**HKCOMB \_ SC**</dt> </dl>       | MAYÚS + CTRL<br/>      |
| <span id="HKCOMB_SCA"></span><span id="hkcomb_sca"></span><dl> <dt>**HKCOMB \_ SCA**</dt> </dl>    | MAYÚS + CTRL + ALT<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Matriz de marcas que especifican la combinación de teclas que se va a usar cuando el usuario especifica una combinación no válida. Para obtener una lista de valores de marcador de modificador, vea la descripción del mensaje [**\_ GETHOTKEY de HKM**](hkm-gethotkey.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Cuando un usuario especifica una combinación de teclas no válida, tal y como se define en las marcas especificadas en *wParam*, el sistema utiliza el operador OR bit a bit para combinar las claves especificadas por el usuario con las marcas especificadas en *lParam*. La combinación de teclas resultante se convierte en una cadena y, a continuación, se muestra en el control de tecla de acceso rápido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





