---
title: WM_APPCOMMAND mensaje (Winuser.h)
description: Notifica a una ventana que el usuario generó un evento de comando de aplicación, por ejemplo, haciendo clic en un botón de comando de aplicación con el mouse o escribiendo una tecla de comando de aplicación en el teclado.
ms.assetid: ffcdfc44-dbfa-42d4-8749-b33bf0e4de0c
keywords:
- WM_APPCOMMAND entrada de teclado y mouse
topic_type:
- apiref
api_name:
- WM_APPCOMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7f5e71f9a443e12ea56cb8ca23daea148da92aa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580025"
---
# <a name="wm_appcommand-message"></a>Mensaje \_ APPCOMMAND de WM

Notifica a una ventana que el usuario generó un evento de comando de aplicación, por ejemplo, haciendo clic en un botón de comando de aplicación con el mouse o escribiendo una tecla de comando de aplicación en el teclado.


```C++
#define WM_APPCOMMAND                   0x0319
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana en la que el usuario hizo clic en el botón o presionó la tecla. Puede ser una ventana secundaria de la ventana que recibe el mensaje. Para obtener más información sobre el procesamiento de este mensaje, vea la sección Comentarios.

</dd> <dt>

*lParam* 
</dt> <dd>

Use el código siguiente para obtener la información contenida en el *parámetro lParam.*


```
cmd  = GET_APPCOMMAND_LPARAM(lParam);

uDevice = GET_DEVICE_LPARAM(lParam);

dwKeys = GET_KEYSTATE_LPARAM(lParam);
```



El comando de aplicación *es cmd*, que puede ser uno de los valores siguientes.



| Value                                                                                                                                                                                                                                                                                                                  | Significado                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPCOMMAND_BASS_BOOST"></span><span id="appcommand_bass_boost"></span><dl> <dt>**APPCOMMAND \_ BOOST \_ BOOST**</dt> <dt>20 DE BOOST 20</dt> </dl>                                                                         | Active y desactive la potenciación de los botones.<br/>                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_BASS_DOWN"></span><span id="appcommand_bass_down"></span><dl> <dt>**APPCOMMAND \_ DOWN \_ 19 DE DOWN**</dt> <dt>19</dt> </dl>                                                                            | Reduzca el tamaño.<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_BASS_UP"></span><span id="appcommand_bass_up"></span><dl> <dt>**APPCOMMAND \_ UP \_ 21 DE NOCIONES**</dt> <dt></dt> </dl>                                                                                  | Aumente el tamaño.<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_BROWSER_BACKWARD"></span><span id="appcommand_browser_backward"></span><dl> <dt>**APPCOMMAND \_ BROWSER \_ BACKWARD**</dt> <dt>1</dt> </dl>                                                        | Vaya hacia atrás.<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_BROWSER_FAVORITES"></span><span id="appcommand_browser_favorites"></span><dl> <dt>**APPCOMMAND \_ FAVORITOS \_ DEL EXPLORADOR**</dt> <dt>6</dt> </dl>                                                     | Abrir favoritos.<br/>                                                                                                                                                                                                                                                                 |
| <span id="APPCOMMAND_BROWSER_FORWARD"></span><span id="appcommand_browser_forward"></span><dl> <dt>**APPCOMMAND \_ REENVÍO \_ DEL EXPLORADOR**</dt> <dt>2</dt> </dl>                                                           | Vaya hacia delante.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_BROWSER_HOME"></span><span id="appcommand_browser_home"></span><dl> <dt>**APPCOMMAND \_ BROWSER \_ HOME**</dt> <dt>7</dt> </dl>                                                                    | Vaya a la página principal.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_BROWSER_REFRESH"></span><span id="appcommand_browser_refresh"></span><dl> <dt>**APPCOMMAND \_ ACTUALIZACIÓN \_ DEL EXPLORADOR**</dt> <dt>3</dt> </dl>                                                           | Página de actualización.<br/>                                                                                                                                                                                                                                                                   |
| <span id="APPCOMMAND_BROWSER_SEARCH"></span><span id="appcommand_browser_search"></span><dl> <dt>**APPCOMMAND \_ BÚSQUEDA \_ DEL EXPLORADOR**</dt> <dt>5</dt> </dl>                                                              | Abra la búsqueda.<br/>                                                                                                                                                                                                                                                                    |
| <span id="APPCOMMAND_BROWSER_STOP"></span><span id="appcommand_browser_stop"></span><dl> <dt>**APPCOMMAND \_ BROWSER \_ STOP**</dt> <dt>4</dt> </dl>                                                                    | Detenga la descarga.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_CLOSE"></span><span id="appcommand_close"></span><dl> <dt>**APPCOMMAND \_ CLOSE**</dt> <dt>31</dt> </dl>                                                                                         | Cierre la ventana (no la aplicación).<br/>                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_COPY"></span><span id="appcommand_copy"></span><dl> <dt>**APPCOMMAND \_ COPY**</dt> <dt>36</dt> </dl>                                                                                            | Copie la selección.<br/>                                                                                                                                                                                                                                                             |
| <span id="APPCOMMAND_CORRECTION_LIST"></span><span id="appcommand_correction_list"></span><dl> <dt>**APPCOMMAND \_ LISTA \_ DE CORRECCIONES**</dt> <dt>45</dt> </dl>                                                          | Muestra la lista de correcciones cuando una palabra se identifica incorrectamente durante la entrada de voz. <br/>                                                                                                                                                                                       |
| <span id="APPCOMMAND_CUT"></span><span id="appcommand_cut"></span><dl> <dt>**APPCOMMAND \_ CUT**</dt> <dt>37</dt> </dl>                                                                                               | Corte la selección.<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_DICTATE_OR_COMMAND_CONTROL_TOGGLE"></span><span id="appcommand_dictate_or_command_control_toggle"></span><dl> <dt>**APPCOMMAND \_ ALTERNANCIA \_ DE DICTADO O CONTROL DE \_ \_ \_ COMANDOS**</dt> <dt>43</dt> </dl> | Alterna entre dos modos de entrada de voz: dictado y comando/control (dar comandos a una aplicación o acceder a menús). <br/>                                                                                                                                               |
| <span id="APPCOMMAND_FIND"></span><span id="appcommand_find"></span><dl> <dt>**APPCOMMAND \_ FIND**</dt> <dt>28</dt> </dl>                                                                                            | Abra el **cuadro de diálogo** Buscar.<br/>                                                                                                                                                                                                                                                       |
| <span id="APPCOMMAND_FORWARD_MAIL"></span><span id="appcommand_forward_mail"></span><dl> <dt>**APPCOMMAND \_ REENVÍO \_ DE CORREO**</dt> <dt>40</dt> </dl>                                                                   | Reenvía un mensaje de correo.<br/>                                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_HELP"></span><span id="appcommand_help"></span><dl> <dt>**APPCOMMAND \_ AYUDA**</dt> <dt>27</dt> </dl>                                                                                            | Abra el cuadro **de diálogo** Ayuda.<br/>                                                                                                                                                                                                                                                       |
| <span id="APPCOMMAND_LAUNCH_APP1"></span><span id="appcommand_launch_app1"></span><dl> <dt>**APPCOMMAND \_ INICIAR \_ APP1**</dt> <dt>17</dt> </dl>                                                                      | Inicie App1.<br/>                                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_LAUNCH_APP2"></span><span id="appcommand_launch_app2"></span><dl> <dt>**APPCOMMAND \_ INICIO \_ DE APP2**</dt> <dt>18</dt> </dl>                                                                      | Inicie App2.<br/>                                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_LAUNCH_MAIL"></span><span id="appcommand_launch_mail"></span><dl> <dt>**APPCOMMAND \_ LAUNCH \_ MAIL**</dt> <dt>15</dt> </dl>                                                                      | Abra el correo electrónico.<br/>                                                                                                                                                                                                                                                                      |
| <span id="APPCOMMAND_LAUNCH_MEDIA_SELECT"></span><span id="appcommand_launch_media_select"></span><dl> <dt>**APPCOMMAND \_ INICIAR \_ MEDIA \_ SELECT**</dt> <dt>16</dt> </dl>                                             | Vaya al modo de selección de medios.<br/>                                                                                                                                                                                                                                                        |
| <span id="APPCOMMAND_MEDIA_CHANNEL_DOWN"></span><span id="appcommand_media_channel_down"></span><dl> <dt>**APPCOMMAND \_ CANAL \_ MULTIMEDIA \_ ABAJO**</dt> <dt>52</dt> </dl>                                                | Decremento del valor del canal, por ejemplo, para un televisor o un emisora de radio. <br/>                                                                                                                                                                                                             |
| <span id="APPCOMMAND_MEDIA_CHANNEL_UP"></span><span id="appcommand_media_channel_up"></span><dl> <dt>**APPCOMMAND \_ CANAL \_ MULTIMEDIA \_ HASTA**</dt> <dt>51</dt> </dl>                                                      | Incremente el valor del canal, por ejemplo, para un televisor o un radioafinador. <br/>                                                                                                                                                                                                             |
| <span id="APPCOMMAND_MEDIA_FAST_FORWARD"></span><span id="appcommand_media_fast_forward"></span><dl> <dt>**APPCOMMAND \_ MEDIA \_ FAST \_ FORWARD**</dt> <dt>49</dt> </dl>                                                | Aumente la velocidad de reproducción de secuencias. Esto se puede implementar de muchas maneras, por ejemplo, mediante una velocidad fija o una serie de velocidades crecientes. <br/>                                                                                                               |
| <span id="APPCOMMAND_MEDIA_NEXTTRACK"></span><span id="appcommand_media_nexttrack"></span><dl> <dt>**APPCOMMAND \_ MEDIA \_ NEXTTRACK**</dt> <dt>11</dt> </dl>                                                          | Vaya a la siguiente pista.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_MEDIA_PAUSE"></span><span id="appcommand_media_pause"></span><dl> <dt>**APPCOMMAND \_ MEDIA \_ PAUSE**</dt> <dt>47</dt> </dl>                                                                      | Pausar. Si ya está en pausa, no haga ninguna otra acción. Se trata de un comando PAUSE directo que no tiene ningún estado. Si hay botones de reproducción y pausa discretos, las aplicaciones deben realizar acciones en este comando, así como **APPCOMMAND \_ MEDIA PLAY \_ \_ PAUSE**. <br/>                               |
| <span id="APPCOMMAND_MEDIA_PLAY"></span><span id="appcommand_media_play"></span><dl> <dt>**APPCOMMAND \_ MEDIA \_ PLAY**</dt> <dt>46</dt> </dl>                                                                         | Comience a reproducir en la posición actual. Si ya está en pausa, se reanudará. Se trata de un comando PLAY directo que no tiene ningún estado. Si hay botones **de reproducción** **y** pausa discretos, las aplicaciones deben realizar acciones en este comando, así como **APPCOMMAND MEDIA \_ PLAY \_ \_ PAUSE**.<br/> |
| <span id="APPCOMMAND_MEDIA_PLAY_PAUSE"></span><span id="appcommand_media_play_pause"></span><dl> <dt>**APPCOMMAND \_ MEDIA \_ PLAY \_ PAUSE**</dt> <dt>14</dt> </dl>                                                      | Reproducir o pausar la reproducción. Si hay botones  **de reproducción** y pausa discretos, las aplicaciones deben realizar acciones en este comando, así como **APPCOMMAND \_ MEDIA \_ PLAY** y **APPCOMMAND MEDIA \_ \_ PAUSE**.<br/>                                                                          |
| <span id="APPCOMMAND_MEDIA_PREVIOUSTRACK"></span><span id="appcommand_media_previoustrack"></span><dl> <dt>**APPCOMMAND \_ MEDIA \_ PREVIOUSTRACK**</dt> <dt>12</dt> </dl>                                              | Vaya a la pista anterior.<br/>                                                                                                                                                                                                                                                           |
| <span id="APPCOMMAND_MEDIA_RECORD"></span><span id="appcommand_media_record"></span><dl> <dt>**APPCOMMAND \_ REGISTRO \_ MULTIMEDIA**</dt> <dt>48</dt> </dl>                                                                   | Comience a grabar la secuencia actual.<br/>                                                                                                                                                                                                                                             |
| <span id="APPCOMMAND_MEDIA_REWIND"></span><span id="appcommand_media_rewind"></span><dl> <dt>**APPCOMMAND \_ MEDIA \_ REWIND**</dt> <dt>50</dt> </dl>                                                                   | Retroceder en una secuencia a una velocidad más alta. Esto se puede implementar de muchas maneras, por ejemplo, mediante una velocidad fija o una serie de velocidades crecientes. <br/>                                                                                                   |
| <span id="APPCOMMAND_MEDIA_STOP"></span><span id="appcommand_media_stop"></span><dl> <dt>**APPCOMMAND \_ MEDIA \_ STOP**</dt> <dt>13</dt> </dl>                                                                         | Detenga la reproducción.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_MIC_ON_OFF_TOGGLE"></span><span id="appcommand_mic_on_off_toggle"></span><dl> <dt>**APPCOMMAND \_ MIC \_ ON \_ OFF \_ TOGGLE**</dt> <dt>44</dt> </dl>                                                  | Alterne el micrófono.<br/>                                                                                                                                                                                                                                                          |
| <span id="APPCOMMAND_MICROPHONE_VOLUME_DOWN"></span><span id="appcommand_microphone_volume_down"></span><dl> <dt>**APPCOMMAND \_ VOLUMEN \_ DEL \_ MICRÓFONO 25**</dt> <dt></dt> </dl>                                    | Reduzca el volumen del micrófono.<br/>                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_MICROPHONE_VOLUME_MUTE"></span><span id="appcommand_microphone_volume_mute"></span><dl> <dt>**APPCOMMAND \_ EXCLUSIÓN \_ DE \_ VOLUMEN DE MICRÓFONO**</dt> <dt>24</dt> </dl>                                    | Silenciar el micrófono.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_MICROPHONE_VOLUME_UP"></span><span id="appcommand_microphone_volume_up"></span><dl> <dt>**APPCOMMAND \_ VOLUMEN \_ DE \_ MICRÓFONO HASTA**</dt> <dt>26</dt> </dl>                                          | Aumente el volumen del micrófono.<br/>                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_NEW"></span><span id="appcommand_new"></span><dl> <dt>**APPCOMMAND \_ NUEVO**</dt> <dt>29</dt> </dl>                                                                                               | Cree una nueva ventana.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_OPEN"></span><span id="appcommand_open"></span><dl> <dt>**APPCOMMAND \_ OPEN**</dt> <dt>30</dt> </dl>                                                                                            | Abra una ventana.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_PASTE"></span><span id="appcommand_paste"></span><dl> <dt>**APPCOMMAND \_ PEGAR**</dt> <dt>38</dt> </dl>                                                                                         | Pegar<br/>                                                                                                                                                                                                                                                                           |
| <span id="APPCOMMAND_PRINT"></span><span id="appcommand_print"></span><dl> <dt>**APPCOMMAND \_ PRINT**</dt> <dt>33</dt> </dl>                                                                                         | Imprima el documento actual.<br/>                                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_REDO"></span><span id="appcommand_redo"></span><dl> <dt>**APPCOMMAND \_ REDO**</dt> <dt>35</dt> </dl>                                                                                            | Última acción de rehacer.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_REPLY_TO_MAIL"></span><span id="appcommand_reply_to_mail"></span><dl> <dt>**APPCOMMAND \_ RESPONDER \_ AL \_ CORREO**</dt> <dt>39</dt> </dl>                                                               | Responder a un mensaje de correo.<br/>                                                                                                                                                                                                                                                        |
| <span id="APPCOMMAND_SAVE"></span><span id="appcommand_save"></span><dl> <dt>**APPCOMMAND \_ GUARDAR**</dt> <dt>32</dt> </dl>                                                                                            | Guarde el documento actual.<br/>                                                                                                                                                                                                                                                          |
| <span id="APPCOMMAND_SEND_MAIL"></span><span id="appcommand_send_mail"></span><dl> <dt>**APPCOMMAND \_ ENVIAR \_ CORREO**</dt> <dt>41</dt> </dl>                                                                            | Enviar un mensaje de correo.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_SPELL_CHECK"></span><span id="appcommand_spell_check"></span><dl> <dt>**APPCOMMAND \_ SPELL \_ CHECK**</dt> <dt>42</dt> </dl>                                                                      | Inicie una revisión ortórquea.<br/>                                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_TREBLE_DOWN"></span><span id="appcommand_treble_down"></span><dl> <dt>**APPCOMMAND \_ TREBLE \_ DOWN**</dt> <dt>22</dt> </dl>                                                                      | Reduzca el valor triple.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_TREBLE_UP"></span><span id="appcommand_treble_up"></span><dl> <dt>**APPCOMMAND \_ TREBLE \_ UP**</dt> <dt>23</dt> </dl>                                                                            | Aumente el triple.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_UNDO"></span><span id="appcommand_undo"></span><dl> <dt>**APPCOMMAND \_ DESHACER**</dt> <dt>34</dt> </dl>                                                                                            | Deshacer última acción.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_VOLUME_DOWN"></span><span id="appcommand_volume_down"></span><dl> <dt>**APPCOMMAND \_ BAJAR \_ VOLUMEN**</dt> <dt>9</dt> </dl>                                                                       | Reduzca el volumen.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_VOLUME_MUTE"></span><span id="appcommand_volume_mute"></span><dl> <dt>**APPCOMMAND \_ EXCLUSIÓN \_ MUTUA**</dt> <dt>DE VOLUMEN 8</dt> </dl>                                                                       | Silenciar el volumen.<br/>                                                                                                                                                                                                                                                                |
| <span id="APPCOMMAND_VOLUME_UP"></span><span id="appcommand_volume_up"></span><dl> <dt>**APPCOMMAND \_ AUMENTO \_ DEL VOLUMEN**</dt> <dt>10</dt> </dl>                                                                            | Elevar el volumen.<br/>                                                                                                                                                                                                                                                               |



 

El *componente uDevice* indica el dispositivo de entrada que generó el evento de entrada y puede ser uno de los siguientes valores.



| Value                                                                                                                                                                                                                                 | Significado                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span id="FAPPCOMMAND_KEY"></span><span id="fappcommand_key"></span><dl> <dt>**FAPPCOMMAND \_ KEY**</dt> <dt>0</dt> </dl>            | El usuario ha presionado una tecla.<br/>                                                                           |
| <span id="FAPPCOMMAND_MOUSE"></span><span id="fappcommand_mouse"></span><dl> <dt>**FAPPCOMMAND \_ Mouse**</dt> <dt>0x8000</dt> </dl> | El usuario hizo clic en un botón del mouse.<br/>                                                                  |
| <span id="FAPPCOMMAND_OEM"></span><span id="fappcommand_oem"></span><dl> <dt>**FAPPCOMMAND \_ Oem**</dt> <dt>0x1000</dt> </dl>       | Un origen de hardware no identificado generó el evento. Podría ser un evento de mouse o teclado.<br/> |



 

El *componente dwKeys* indica si varias claves virtuales están fuera de servicio y pueden ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                                                               | Significado                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_ Control**</dt> <dt>0x0008</dt> </dl>    | La tecla CTRL está presionada.<br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt> </dl>    | El botón izquierdo del mouse está apagado.<br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt> </dl>    | El botón central del mouse está apagado.<br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt> </dl>    | El botón derecho del mouse está apagado.<br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <dt>**MK \_ Mayús**</dt> <dt>0x0004</dt> </dl>          | La tecla MAYÚS está abajo.<br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt> </dl> | El primer botón X está apagado.<br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt> </dl> | El segundo botón X está apagado.<br/>     |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver **TRUE**. Para obtener más información sobre cómo procesar el valor devuelto, vea la sección Comentarios.

## <a name="remarks"></a>Observaciones

[**DefWindowProc genera**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) el mensaje **\_ APPCOMMAND** de WM cuando procesa el mensaje [**WM \_ XBUTTONUP**](wm-xbuttonup.md) o [**WM \_ NCXBUTTONUP,**](wm-ncxbuttonup.md) o cuando el usuario crea una clave de comando de aplicación.

Si una ventana secundaria no procesa este mensaje y, en su lugar, llama a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), **DefWindowProc** enviará el mensaje a su ventana primaria. Si una ventana de nivel superior no procesa este mensaje y en su lugar llama a **DefWindowProc**, **DefWindowProc** llamará a un enlace de shell con el código de enlace igual a **HSHELL \_ APPCOMMAND**.

Para obtener las coordenadas del cursor si el mensaje se generó con un clic del mouse, la aplicación puede llamar a [**GetMessagePos**](/windows/desktop/api/winuser/nf-winuser-getmessagepos). Una aplicación puede probar si el mouse generó el mensaje comprobando si *lParam* contiene **FAPPCOMMAND \_ MOUSE**.

A diferencia de otros mensajes de Windows, una aplicación debe devolver **TRUE** de este mensaje si la procesa. Esto permitirá que el software que simula este mensaje en sistemas de Windows anteriores Windows 2000 determine si el procedimiento de ventana procesó el mensaje o llamó a [**DefWindowProc para**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) procesarlo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GET \_ APPCOMMAND \_ LPARAM**](/windows/win32/api/winuser/nf-winuser-get_appcommand_lparam)
</dt> <dt>

[**GET \_ DEVICE \_ LPARAM**](/windows/win32/api/winuser/nf-winuser-get_device_lparam)
</dt> <dt>

[**GET \_ KEYSTATE \_ LPARAM**](/windows/win32/api/winuser/nf-winuser-get_keystate_lparam)
</dt> <dt>

[**ShellProc**](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85))
</dt> <dt>

[**WM \_ XBUTTONUP**](wm-xbuttonup.md)
</dt> <dt>

[**WM \_ NCXBUTTONUP**](wm-ncxbuttonup.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Entrada del mouse](mouse-input.md)
</dt> </dl>

 

