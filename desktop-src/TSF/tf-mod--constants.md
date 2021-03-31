---
title: Constantes de TF_MOD_ (msctf. h)
description: Las \_ constantes TF mod \_ \ especifican modificadores de clave en la \_ estructura TF PRESERVEDKEY.
ms.assetid: 4642ef17-34bd-4482-a9e9-0fbed7b574b1
topic_type:
- apiref
api_name:
- TF_MOD_ALT
- TF_MOD_CONTROL
- TF_MOD_SHIFT
- TF_MOD_RALT
- TF_MOD_RCONTROL
- TF_MOD_RSHIFT
- TF_MOD_LALT
- TF_MOD_LCONTROL
- TF_MOD_LSHIFT
- TF_MOD_ON_KEYUP
- TF_MOD_IGNORE_ALL_MODIFIER
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e67e081d9a0f8714410861c7c36f9f751bad8d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079333"
---
# <a name="tf_mod_-constants"></a>TF \_ mod ( \_ \* constantes)

Las \_ constantes TF mod \_ \* especifican modificadores de clave en la estructura [TF \_ PRESERVEDKEY](/windows/desktop/api/Msctf/ns-msctf-tf_preservedkey) .



| Constante o valor                                                                                                                                                                                                                                                      | Descripción                                                                                                                                                                          |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_MOD_ALT"></span><span id="tf_mod_alt"></span><dl> <dt>**TF \_ MOD \_ Alt**</dt> <dt>0x0001</dt> </dl>                                                   | Se presionó cualquiera de las teclas ALT<br/>                                                                                                                                         |
| <span id="TF_MOD_CONTROL"></span><span id="tf_mod_control"></span><dl> <dt>**TF \_ \_Control mod**</dt> <dt>0x0002</dt> </dl>                                       | Se presionó cualquiera de las teclas CTRL<br/>                                                                                                                                        |
| <span id="TF_MOD_SHIFT"></span><span id="tf_mod_shift"></span><dl> <dt>**TF \_ MOD \_ Shift**</dt> <dt>0x0004</dt> </dl>                                             | Se presionó cualquiera de las teclas Mayús<br/>                                                                                                                                       |
| <span id="TF_MOD_RALT"></span><span id="tf_mod_ralt"></span><dl> <dt>**TF \_ MOD \_ Ralt**</dt> <dt>0x0008</dt> </dl>                                                | Se presiona la tecla ALT derecha<br/>                                                                                                                                              |
| <span id="TF_MOD_RCONTROL"></span><span id="tf_mod_rcontrol"></span><dl> <dt>**TF \_ MOD \_ RCONTROL**</dt> <dt>0x0010</dt> </dl>                                    | Se presiona la tecla CTRL derecha<br/>                                                                                                                                             |
| <span id="TF_MOD_RSHIFT"></span><span id="tf_mod_rshift"></span><dl> <dt>**TF \_ MOD \_ RSHIFT**</dt> <dt>0x0020</dt> </dl>                                          | Se presiona la tecla Mayús derecha<br/>                                                                                                                                            |
| <span id="TF_MOD_LALT"></span><span id="tf_mod_lalt"></span><dl> <dt>**TF \_ MOD \_ LALT**</dt> <dt>0x0040</dt> </dl>                                                | Se presiona la tecla ALT izquierda<br/>                                                                                                                                               |
| <span id="TF_MOD_LCONTROL"></span><span id="tf_mod_lcontrol"></span><dl> <dt>**TF \_ MOD \_ LCONTROL**</dt> <dt>0x0080</dt> </dl>                                    | Se presiona la tecla CTRL izquierda<br/>                                                                                                                                              |
| <span id="TF_MOD_LSHIFT"></span><span id="tf_mod_lshift"></span><dl> <dt>**TF \_ MOD \_ LSHIFT**</dt> <dt>0x0100</dt> </dl>                                          | Se presiona la tecla Mayús izquierda<br/>                                                                                                                                             |
| <span id="TF_MOD_ON_KEYUP"></span><span id="tf_mod_on_keyup"></span><dl> <dt>**TF \_ MOD \_ en \_ KEYUP**</dt> <dt>0x0200</dt> </dl>                                   | El evento se desencadenará cuando se libere la tecla. Sin esta marca, el evento se desencadena cuando se presiona la tecla.<br/>                                                          |
| <span id="TF_MOD_IGNORE_ALL_MODIFIER"></span><span id="tf_mod_ignore_all_modifier"></span><dl> <dt>**TF \_ MOD \_ omitir \_ todos los \_ Modificadores**</dt> <dt>0x0400</dt> </dl> | Se omite el estado de las teclas ALT, CTRL y Mayús. Esto significa que el evento se desencadenará cuando se presione la tecla virtual, independientemente de las teclas modificadoras que se presionen.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Redistribuible<br/>          | TSF 1,0 en Windows 2000 Professional<br/>                                      |
| Encabezado<br/>                   | <dl> <dt>Msctf. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msctf. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[TF \_ PRESERVEDKEY](/windows/desktop/api/Msctf/ns-msctf-tf_preservedkey)
</dt> </dl>

 

 





