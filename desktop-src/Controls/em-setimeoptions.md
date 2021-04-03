---
title: Mensaje EM_SETIMEOPTIONS (RichEdit. h)
description: Establece las opciones del editor de métodos de entrada (IME).
ms.assetid: 8a72ee1c-f6b8-44eb-b8df-57cd834db326
keywords:
- EM_SETIMEOPTIONS controles de mensajes de Windows
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
ms.openlocfilehash: 59be3148bd00abd998af200368f2ed77ad3ff911
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905363"
---
# <a name="em_setimeoptions-message"></a>\_Mensaje SETIMEOPTIONS em

Establece las opciones del editor de métodos de entrada (IME).

> [!Note]  
> Este mensaje solo se admite en las versiones en idioma asiático de Microsoft Rich Edit 1,0. No se admite en las versiones posteriores.

 

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica uno de los valores siguientes.



| Value                                                                                                                                             | Significado                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="ECOOP_SET"></span><span id="ecoop_set"></span><dl> <dt>**conjunto de ECOOP \_**</dt> </dl> | Establece las opciones en las especificadas por *lParam*.<br/>                             |
| <span id="ECOOP_OR"></span><span id="ecoop_or"></span><dl> <dt>**ECOOP \_ o**</dt> </dl>    | Combina las opciones especificadas con las opciones actuales.<br/>                     |
| <span id="ECOOP_AND"></span><span id="ecoop_and"></span><dl> <dt>**ECOOP \_ y**</dt> </dl> | Conserva solo las opciones actuales que también especifica *lParam*.<br/>      |
| <span id="ECOOP_XOR"></span><span id="ecoop_xor"></span><dl> <dt>**ECOOP \_ XOR**</dt> </dl> | Lógicamente exclusivas o las opciones actuales con las especificadas por *lParam.*<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica uno o más de los valores siguientes.



| Value                                                                                                                                                                                 | Significado                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="IMF_CLOSESTATUSWINDOW"></span><span id="imf_closestatuswindow"></span><dl> <dt>**CLOSESTATUSWINDOW de IMF \_**</dt> </dl> | Cierra la ventana de estado de IME cuando el control recibe el foco de entrada.<br/>                                                                                                               |
| <span id="IMF_FORCEACTIVE"></span><span id="imf_forceactive"></span><dl> <dt>**FORCEACTIVE de IMF \_**</dt> </dl>                   | Activa el IME cuando el control recibe el foco de entrada.<br/>                                                                                                                          |
| <span id="IMF_FORCEDISABLE"></span><span id="imf_forcedisable"></span><dl> <dt>**FORCEDISABLE de IMF \_**</dt> </dl>                | Deshabilita el IME cuando el control recibe el foco de entrada.<br/>                                                                                                                           |
| <span id="IMF_FORCEENABLE"></span><span id="imf_forceenable"></span><dl> <dt>**FORCEENABLE de IMF \_**</dt> </dl>                   | Habilita el IME cuando el control recibe el foco de entrada.<br/>                                                                                                                            |
| <span id="IMF_FORCEINACTIVE"></span><span id="imf_forceinactive"></span><dl> <dt>**FORCEINACTIVE de IMF \_**</dt> </dl>             | Desactiva el IME cuando el control recibe el foco de entrada.<br/>                                                                                                                        |
| <span id="IMF_FORCENONE"></span><span id="imf_forcenone"></span><dl> <dt>**FORCENONE de IMF \_**</dt> </dl>                         | Deshabilita el control de IME.<br/>                                                                                                                                                                |
| <span id="IMF_FORCEREMEMBER"></span><span id="imf_forceremember"></span><dl> <dt>**FORCEREMEMBER de IMF \_**</dt> </dl>             | Restaura el estado anterior del IME cuando el control recibe el foco de entrada.<br/>                                                                                                           |
| <span id="IMF_MULTIPLEEDIT"></span><span id="imf_multipleedit"></span><dl> <dt>**MULTIPLEEDIT de IMF \_**</dt> </dl>                | Especifica que la cadena de composición no se cancelará o determinará por los cambios de foco. Esto permite que una aplicación tenga cadenas de composición independientes en cada control Rich Edit.<br/> |
| <span id="IMF_VERTICAL"></span><span id="imf_vertical"></span><dl> <dt>**IMF \_ vertical**</dt> </dl>                            | Nota utilizada en la edición enriquecida 2,0 y versiones posteriores. <br/>                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si se produce un error en la operación, el valor devuelto es cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_GETIMEOPTIONS em**](em-getimeoptions.md)
</dt> </dl>

 

 





