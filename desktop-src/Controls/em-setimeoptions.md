---
title: EM_SETIMEOPTIONS mensaje (Richedit.h)
description: Establece las opciones del Editor de métodos de entrada (IME).
ms.assetid: 8a72ee1c-f6b8-44eb-b8df-57cd834db326
keywords:
- EM_SETIMEOPTIONS controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETIMEOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83ffae9586c3ee05f951672f0927c4f10ad2115684643af8418062bb7724c7b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048395"
---
# <a name="em_setimeoptions-message"></a>Mensaje \_ EM SETIMEOPTIONS

Establece las opciones del Editor de métodos de entrada (IME).

> [!Note]  
> Este mensaje solo se admite en las versiones en idioma asiático de Microsoft Rich Edit 1.0. No se admite en versiones posteriores.

 

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica uno de los siguientes valores.



| Value                                                                                                                                             | Significado                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="ECOOP_SET"></span><span id="ecoop_set"></span><dl> <dt>**ECOOP \_ SET**</dt> </dl> | Establece las opciones en las especificadas por *lParam*.<br/>                             |
| <span id="ECOOP_OR"></span><span id="ecoop_or"></span><dl> <dt>**ECOOP \_ OR**</dt> </dl>    | Combina las opciones especificadas con las opciones actuales.<br/>                     |
| <span id="ECOOP_AND"></span><span id="ecoop_and"></span><dl> <dt>**ECOOP \_ AND**</dt> </dl> | Conserva solo las opciones actuales que también se especifican mediante *lParam*.<br/>      |
| <span id="ECOOP_XOR"></span><span id="ecoop_xor"></span><dl> <dt>**ECOOP \_ XOR**</dt> </dl> | O excluye lógicamente las opciones actuales con las especificadas por *lParam.*<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica uno de los valores siguientes.



| Value                                                                                                                                                                                 | Significado                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="IMF_CLOSESTATUSWINDOW"></span><span id="imf_closestatuswindow"></span><dl> <dt>**LA \_ VENTANA CLOSESTATUSWINDOW DE LA LONCIENA**</dt> </dl> | Cierra la ventana de estado de IME cuando el control recibe el foco de entrada.<br/>                                                                                                               |
| <span id="IMF_FORCEACTIVE"></span><span id="imf_forceactive"></span><dl> <dt>**LA \_ FORCEACTIVE DE LA TOBA**</dt> </dl>                   | Activa el IME cuando el control recibe el foco de entrada.<br/>                                                                                                                          |
| <span id="IMF_FORCEDISABLE"></span><span id="imf_forcedisable"></span><dl> <dt>**\_FORCEDISABLE DE LA FUERZA DE LA CONFIDÍA**</dt> </dl>                | Deshabilita el IME cuando el control recibe el foco de entrada.<br/>                                                                                                                           |
| <span id="IMF_FORCEENABLE"></span><span id="imf_forceenable"></span><dl> <dt>**FORCEENABLE DE LA \_ TORTINA**</dt> </dl>                   | Habilita el IME cuando el control recibe el foco de entrada.<br/>                                                                                                                            |
| <span id="IMF_FORCEINACTIVE"></span><span id="imf_forceinactive"></span><dl> <dt>**LA \_ FUERZA DE LA RÁBADA**</dt> </dl>             | Inactiva el IME cuando el control recibe el foco de entrada.<br/>                                                                                                                        |
| <span id="IMF_FORCENONE"></span><span id="imf_forcenone"></span><dl> <dt>**\_FORCENONE DE LA ZONA DE LA CONSOÍA**</dt> </dl>                         | Deshabilita el control de IME.<br/>                                                                                                                                                                |
| <span id="IMF_FORCEREMEMBER"></span><span id="imf_forceremember"></span><dl> <dt>**LA \_ FORCEREMEMBER DE LA FUERZA DE LA FUERZA DE LA FUERZA DE**</dt> </dl>             | Restaura el estado de IME anterior cuando el control recibe el foco de entrada.<br/>                                                                                                           |
| <span id="IMF_MULTIPLEEDIT"></span><span id="imf_multipleedit"></span><dl> <dt>**\_MULTIPLEEDITAR LUGAR**</dt> </dl>                | Especifica que los cambios de foco no cancelarán ni determinarán la cadena de composición. Esto permite que una aplicación tenga cadenas de composición independientes en cada control de edición enriquecido.<br/> |
| <span id="IMF_VERTICAL"></span><span id="imf_vertical"></span><dl> <dt>**VERTICAL DE \_ ALDABA**</dt> </dl>                            | Nota usada en Rich Edit 2.0 y versiones posteriores. <br/>                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si se produce un error en la operación, el valor devuelto es cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EM \_ GETIMEOPTIONS**](em-getimeoptions.md)
</dt> </dl>

 

 





