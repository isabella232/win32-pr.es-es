---
title: HKM_SETRULES mensaje (Commctrl.h)
description: Define las combinaciones no válidas y la combinación de modificadores predeterminada para un control de tecla de acceso.
ms.assetid: de3dd463-a534-4c7c-ae04-da80a3bff2ab
keywords:
- HKM_SETRULES controles de Windows mensaje
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
ms.openlocfilehash: 4ec47450ca0d67854d7be413d8a3eb3e5fec3eac49e18f6bcf96f86b563c8906
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958714"
---
# <a name="hkm_setrules-message"></a>Mensaje \_ SETRULES de HKM

Define las combinaciones no válidas y la combinación de modificadores predeterminada para un control de tecla de acceso.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Matriz de marcas que especifican combinaciones de claves no válidas. Este parámetro puede ser una combinación de los valores siguientes:



| Valor                                                                                                                                                   | Significado                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span id="HKCOMB_A"></span><span id="hkcomb_a"></span><dl> <dt>**HKCOMB \_ A**</dt> </dl>          | ALT<br/>             |
| <span id="HKCOMB_C"></span><span id="hkcomb_c"></span><dl> <dt>**HKCOMB \_ C**</dt> </dl>          | CTRL<br/>            |
| <span id="HKCOMB_CA"></span><span id="hkcomb_ca"></span><dl> <dt>**HKCOMB \_ CA**</dt> </dl>       | CTRL+ALT<br/>        |
| <span id="HKCOMB_NONE"></span><span id="hkcomb_none"></span><dl> <dt>**HKCOMB \_ NONE**</dt> </dl> | Claves sin modificar<br/> |
| <span id="HKCOMB_S"></span><span id="hkcomb_s"></span><dl> <dt>**HKCOMB \_ S**</dt> </dl>          | Mayús<br/>           |
| <span id="HKCOMB_SA"></span><span id="hkcomb_sa"></span><dl> <dt>**HKCOMB \_ SA**</dt> </dl>       | MAYÚS+ALT<br/>       |
| <span id="HKCOMB_SC"></span><span id="hkcomb_sc"></span><dl> <dt>**HKCOMB \_ SC**</dt> </dl>       | MAYÚS+CTRL<br/>      |
| <span id="HKCOMB_SCA"></span><span id="hkcomb_sca"></span><dl> <dt>**HKCOMB \_ SCA**</dt> </dl>    | MAYÚS+CTRL+ALT<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Matriz de marcas que especifican la combinación de claves que se usará cuando el usuario escriba una combinación no válida. Para obtener una lista de valores de marca modificadora, vea la descripción del [**mensaje \_ GETHOTKEY de HKM.**](hkm-gethotkey.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Cuando un usuario escribe una combinación de claves no válida, tal como se define en las marcas especificadas en *wParam*, el sistema usa el operador OR bit a bit para combinar las claves especificadas por el usuario con las marcas especificadas en *lParam*. La combinación de teclas resultante se convierte en una cadena y, a continuación, se muestra en el control de tecla de acceso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





