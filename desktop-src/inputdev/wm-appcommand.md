---
title: Mensaje de WM_APPCOMMAND (Winuser. h)
description: Notifica a una ventana que el usuario ha generado un evento de comando de aplicación, por ejemplo, haciendo clic en un botón de comando de la aplicación mediante el mouse o escribiendo una tecla de comando de la aplicación en el teclado.
ms.assetid: ffcdfc44-dbfa-42d4-8749-b33bf0e4de0c
keywords:
- Entrada de mouse y teclado de mensaje de WM_APPCOMMAND
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422199"
---
# <a name="wm_appcommand-message"></a>Mensaje de APPCOMMAND de WM \_

Notifica a una ventana que el usuario ha generado un evento de comando de aplicación, por ejemplo, haciendo clic en un botón de comando de la aplicación mediante el mouse o escribiendo una tecla de comando de la aplicación en el teclado.


```C++
#define WM_APPCOMMAND                   0x0319
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana en la que el usuario hizo clic en el botón o presionó la tecla. Puede tratarse de una ventana secundaria de la ventana que recibe el mensaje. Para obtener más información sobre el procesamiento de este mensaje, consulte la sección Comentarios.

</dd> <dt>

*lParam* 
</dt> <dd>

Use el código siguiente para obtener la información contenida en el parámetro *lParam* .


```
cmd  = GET_APPCOMMAND_LPARAM(lParam);

uDevice = GET_DEVICE_LPARAM(lParam);

dwKeys = GET_KEYSTATE_LPARAM(lParam);
```



El comando de aplicación es *cmd*, que puede tener uno de los valores siguientes.



| Value                                                                                                                                                                                                                                                                                                                  | Significado                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPCOMMAND_BASS_BOOST"></span><span id="appcommand_bass_boost"></span><dl> <dt>**APPCOMMAND \_ \_Aumento de graves**</dt> <dt>20</dt> </dl>                                                                         | Activar y desactivar el aumento de graves.<br/>                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_BASS_DOWN"></span><span id="appcommand_bass_down"></span><dl> <dt>**APPCOMMAND \_ GRAVES \_ bajo**</dt> <dt>19</dt> </dl>                                                                            | Disminuya el graves.<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_BASS_UP"></span><span id="appcommand_bass_up"></span><dl> <dt>**APPCOMMAND \_ GRAVES \_**</dt> <dt>21</dt> </dl>                                                                                  | Aumente el graves.<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_BROWSER_BACKWARD"></span><span id="appcommand_browser_backward"></span><dl> <dt>**APPCOMMAND \_ EXPLORADOR \_ hacia atrás**</dt> <dt>1</dt> </dl>                                                        | Navegar hacia atrás.<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_BROWSER_FAVORITES"></span><span id="appcommand_browser_favorites"></span><dl> <dt>**APPCOMMAND \_ \_Favoritos del explorador**</dt> <dt>6</dt> </dl>                                                     | Abra favoritos.<br/>                                                                                                                                                                                                                                                                 |
| <span id="APPCOMMAND_BROWSER_FORWARD"></span><span id="appcommand_browser_forward"></span><dl> <dt>**APPCOMMAND \_ \_Reenvío del explorador**</dt> <dt>2</dt> </dl>                                                           | Navegar hacia delante.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_BROWSER_HOME"></span><span id="appcommand_browser_home"></span><dl> <dt>**APPCOMMAND \_ \_Inicio del explorador**</dt> <dt>7</dt> </dl>                                                                    | Navegar a la Página principal.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_BROWSER_REFRESH"></span><span id="appcommand_browser_refresh"></span><dl> <dt>**APPCOMMAND \_ \_Actualización del explorador**</dt> <dt>3</dt> </dl>                                                           | Actualizar página.<br/>                                                                                                                                                                                                                                                                   |
| <span id="APPCOMMAND_BROWSER_SEARCH"></span><span id="appcommand_browser_search"></span><dl> <dt>**APPCOMMAND \_ \_Búsqueda en explorador**</dt> <dt>5</dt> </dl>                                                              | Abra buscar.<br/>                                                                                                                                                                                                                                                                    |
| <span id="APPCOMMAND_BROWSER_STOP"></span><span id="appcommand_browser_stop"></span><dl> <dt>**APPCOMMAND \_ \_Detención del explorador**</dt> <dt>4</dt> </dl>                                                                    | Detener la descarga.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_CLOSE"></span><span id="appcommand_close"></span><dl> <dt>**APPCOMMAND \_ CERRAR**</dt> <dt>31</dt> </dl>                                                                                         | Cierre la ventana (no la aplicación).<br/>                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_COPY"></span><span id="appcommand_copy"></span><dl> <dt>**APPCOMMAND \_ COPIAR**</dt> <dt>36</dt> </dl>                                                                                            | Copiar la selección.<br/>                                                                                                                                                                                                                                                             |
| <span id="APPCOMMAND_CORRECTION_LIST"></span><span id="appcommand_correction_list"></span><dl> <dt>**APPCOMMAND \_ \_Lista de corrección**</dt> <dt>45</dt> </dl>                                                          | Muestra la lista de correcciones cuando una palabra se identifica incorrectamente durante la entrada de voz. <br/>                                                                                                                                                                                       |
| <span id="APPCOMMAND_CUT"></span><span id="appcommand_cut"></span><dl> <dt>**APPCOMMAND \_ CORTAR**</dt> <dt>37</dt> </dl>                                                                                               | Cortar la selección.<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_DICTATE_OR_COMMAND_CONTROL_TOGGLE"></span><span id="appcommand_dictate_or_command_control_toggle"></span><dl> <dt>**APPCOMMAND \_ DICTAr \_ o \_ \_ \_ alternar control de comandos**</dt> <dt>43</dt> </dl> | Alterna entre dos modos de entrada de voz: dictado y comando/control (proporcionar comandos a una aplicación o tener acceso a los menús). <br/>                                                                                                                                               |
| <span id="APPCOMMAND_FIND"></span><span id="appcommand_find"></span><dl> <dt>**APPCOMMAND \_ BUSCAR**</dt> <dt>28</dt> </dl>                                                                                            | Abra el cuadro de diálogo **Buscar** .<br/>                                                                                                                                                                                                                                                       |
| <span id="APPCOMMAND_FORWARD_MAIL"></span><span id="appcommand_forward_mail"></span><dl> <dt>**APPCOMMAND \_ \_Correo directo**</dt> <dt>40</dt> </dl>                                                                   | Reenviar un mensaje de correo.<br/>                                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_HELP"></span><span id="appcommand_help"></span><dl> <dt>**APPCOMMAND \_ AYUDA**</dt> <dt>27</dt> </dl>                                                                                            | Abra el cuadro de diálogo **ayuda** .<br/>                                                                                                                                                                                                                                                       |
| <span id="APPCOMMAND_LAUNCH_APP1"></span><span id="appcommand_launch_app1"></span><dl> <dt>**APPCOMMAND \_ INICIAR \_ app1**</dt> <dt>17</dt> </dl>                                                                      | Inicie app1.<br/>                                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_LAUNCH_APP2"></span><span id="appcommand_launch_app2"></span><dl> <dt>**APPCOMMAND \_ INICIAR \_ APP2**</dt> <dt>18</dt> </dl>                                                                      | Inicie App2.<br/>                                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_LAUNCH_MAIL"></span><span id="appcommand_launch_mail"></span><dl> <dt>**APPCOMMAND \_ INICIAR \_ mail**</dt> <dt>15</dt> </dl>                                                                      | Abra mail.<br/>                                                                                                                                                                                                                                                                      |
| <span id="APPCOMMAND_LAUNCH_MEDIA_SELECT"></span><span id="appcommand_launch_media_select"></span><dl> <dt>**APPCOMMAND \_ INICIAR \_ \_ selección de medio**</dt> <dt>16</dt> </dl>                                             | Vaya al modo de selección de medios.<br/>                                                                                                                                                                                                                                                        |
| <span id="APPCOMMAND_MEDIA_CHANNEL_DOWN"></span><span id="appcommand_media_channel_down"></span><dl> <dt>**APPCOMMAND \_ Canal de medios \_ \_ inactivo**</dt> <dt>52</dt> </dl>                                                | Disminuya el valor del canal, por ejemplo, para un sintonizador de TV o radio. <br/>                                                                                                                                                                                                             |
| <span id="APPCOMMAND_MEDIA_CHANNEL_UP"></span><span id="appcommand_media_channel_up"></span><dl> <dt>**APPCOMMAND \_ \_Canal \_ de medios up**</dt> <dt>51</dt> </dl>                                                      | Incremente el valor del canal, por ejemplo, para un sintonizador de TV o radio. <br/>                                                                                                                                                                                                             |
| <span id="APPCOMMAND_MEDIA_FAST_FORWARD"></span><span id="appcommand_media_fast_forward"></span><dl> <dt>**APPCOMMAND \_ \_ \_ Avance rápido de medios**</dt> <dt>49</dt> </dl>                                                | Aumentar la velocidad de reproducción de la secuencia. Esto se puede implementar de muchas maneras, por ejemplo, utilizando una velocidad fija o alternando una serie de velocidades crecientes. <br/>                                                                                                               |
| <span id="APPCOMMAND_MEDIA_NEXTTRACK"></span><span id="appcommand_media_nexttrack"></span><dl> <dt>**APPCOMMAND \_ MEDIA \_ NEXTTRACK**</dt> <dt>11</dt> </dl>                                                          | Vaya a la pista siguiente.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_MEDIA_PAUSE"></span><span id="appcommand_media_pause"></span><dl> <dt>**APPCOMMAND \_ \_Pausa de medios**</dt> <dt>47</dt> </dl>                                                                      | Pausar. Si ya está en pausa, no realice ninguna acción. Se trata de un comando de pausa directa que no tiene ningún Estado. Si hay botones de reproducción y pausa discretos, las aplicaciones deben tomar medidas en este comando, así como **APPCOMMAND \_ media \_ Play \_ PAUSE**. <br/>                               |
| <span id="APPCOMMAND_MEDIA_PLAY"></span><span id="appcommand_media_play"></span><dl> <dt>**APPCOMMAND \_ MEDIA \_ PLAY**</dt> <dt>46</dt> </dl>                                                                         | Comienza a reproducirse en la posición actual. Si ya está en pausa, se reanudará. Se trata de un comando de reproducción directa que no tiene ningún Estado. Si hay botones de **reproducción** y **pausa** discretos, las aplicaciones deben tomar medidas en este comando, así como **APPCOMMAND \_ media \_ Play \_ PAUSE**.<br/> |
| <span id="APPCOMMAND_MEDIA_PLAY_PAUSE"></span><span id="appcommand_media_play_pause"></span><dl> <dt>**APPCOMMAND \_ \_ \_ Pausa de reproducción multimedia**</dt> <dt>14</dt> </dl>                                                      | Reproducir o pausar la reproducción. Si hay botones de **reproducción** y **pausa** discretos, las aplicaciones deben tomar medidas en este comando, así como **APPCOMMAND \_ media \_ Play** y **APPCOMMAND \_ media \_ PAUSE**.<br/>                                                                          |
| <span id="APPCOMMAND_MEDIA_PREVIOUSTRACK"></span><span id="appcommand_media_previoustrack"></span><dl> <dt>**APPCOMMAND \_ MEDIA \_ PREVIOUSTRACK**</dt> <dt>12</dt> </dl>                                              | Vaya a la pista anterior.<br/>                                                                                                                                                                                                                                                           |
| <span id="APPCOMMAND_MEDIA_RECORD"></span><span id="appcommand_media_record"></span><dl> <dt>**APPCOMMAND \_ \_Registro de medios**</dt> <dt>48</dt> </dl>                                                                   | Inicia la grabación de la secuencia actual.<br/>                                                                                                                                                                                                                                             |
| <span id="APPCOMMAND_MEDIA_REWIND"></span><span id="appcommand_media_rewind"></span><dl> <dt>**APPCOMMAND \_ \_REbobinado de medios**</dt> <dt>50</dt> </dl>                                                                   | Retroceder en un flujo a una velocidad mayor de velocidad. Esto se puede implementar de muchas maneras, por ejemplo, utilizando una velocidad fija o alternando una serie de velocidades crecientes. <br/>                                                                                                   |
| <span id="APPCOMMAND_MEDIA_STOP"></span><span id="appcommand_media_stop"></span><dl> <dt>**APPCOMMAND \_ \_Detención de medios**</dt> <dt>13</dt> </dl>                                                                         | Detenga la reproducción.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_MIC_ON_OFF_TOGGLE"></span><span id="appcommand_mic_on_off_toggle"></span><dl> <dt>**APPCOMMAND \_ \_Alternancia MIC \_ OFF \_**</dt> <dt>44</dt> </dl>                                                  | Alternar el micrófono.<br/>                                                                                                                                                                                                                                                          |
| <span id="APPCOMMAND_MICROPHONE_VOLUME_DOWN"></span><span id="appcommand_microphone_volume_down"></span><dl> <dt>**APPCOMMAND \_ Volumen de micrófono por \_ \_ debajo**</dt> del <dt>25</dt> </dl>                                    | Reducir el volumen del micrófono.<br/>                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_MICROPHONE_VOLUME_MUTE"></span><span id="appcommand_microphone_volume_mute"></span><dl> <dt>**APPCOMMAND \_ \_ \_ Silenciar volumen de micrófono**</dt> <dt>24</dt> </dl>                                    | Silenciar el micrófono.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_MICROPHONE_VOLUME_UP"></span><span id="appcommand_microphone_volume_up"></span><dl> <dt>**APPCOMMAND \_ \_Volumen \_ de micrófono hasta**</dt> <dt>26</dt> </dl>                                          | Aumentar el volumen del micrófono.<br/>                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_NEW"></span><span id="appcommand_new"></span><dl> <dt>**APPCOMMAND \_ NUEVO**</dt> <dt>29</dt> </dl>                                                                                               | Cree una nueva ventana.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_OPEN"></span><span id="appcommand_open"></span><dl> <dt>**APPCOMMAND \_ Abra**</dt> <dt>30</dt> </dl>                                                                                            | Abra una ventana.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_PASTE"></span><span id="appcommand_paste"></span><dl> <dt>**APPCOMMAND \_ PEGAR**</dt> <dt>38</dt> </dl>                                                                                         | Pegar<br/>                                                                                                                                                                                                                                                                           |
| <span id="APPCOMMAND_PRINT"></span><span id="appcommand_print"></span><dl> <dt>**APPCOMMAND \_ IMPRIMIR**</dt> <dt>33</dt> </dl>                                                                                         | Imprime el documento actual.<br/>                                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_REDO"></span><span id="appcommand_redo"></span><dl> <dt>**APPCOMMAND \_ Rehacer**</dt> <dt>35</dt> </dl>                                                                                            | Rehacer la última acción.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_REPLY_TO_MAIL"></span><span id="appcommand_reply_to_mail"></span><dl> <dt>**APPCOMMAND \_ RESPONDER \_ al \_ correo electrónico**</dt> <dt>39</dt> </dl>                                                               | Responder a un mensaje de correo.<br/>                                                                                                                                                                                                                                                        |
| <span id="APPCOMMAND_SAVE"></span><span id="appcommand_save"></span><dl> <dt>**APPCOMMAND \_ Ahorre**</dt> <dt>32</dt> </dl>                                                                                            | Guardar documento actual.<br/>                                                                                                                                                                                                                                                          |
| <span id="APPCOMMAND_SEND_MAIL"></span><span id="appcommand_send_mail"></span><dl> <dt>**APPCOMMAND \_ ENVIAR \_ correo**</dt> <dt>41</dt> </dl>                                                                            | Envíe un mensaje de correo.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_SPELL_CHECK"></span><span id="appcommand_spell_check"></span><dl> <dt>**APPCOMMAND \_ Corrector \_ ortográfico**</dt> <dt>42</dt> </dl>                                                                      | Inicie una revisión ortográfica.<br/>                                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_TREBLE_DOWN"></span><span id="appcommand_treble_down"></span><dl> <dt>**APPCOMMAND \_ AGUDOs \_**</dt> <dt>22</dt> </dl>                                                                      | Reduzca el agudo.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_TREBLE_UP"></span><span id="appcommand_treble_up"></span><dl> <dt>**APPCOMMAND \_ AGUDOs \_**</dt> <dt>23</dt> </dl>                                                                            | Aumente el agudo.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_UNDO"></span><span id="appcommand_undo"></span><dl> <dt>**APPCOMMAND \_ Deshacer**</dt> <dt>34</dt> </dl>                                                                                            | Deshacer la última acción.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_VOLUME_DOWN"></span><span id="appcommand_volume_down"></span><dl> <dt>**APPCOMMAND \_ VOLUMEN \_ inferior**</dt> <dt>9</dt> </dl>                                                                       | Baje el volumen.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_VOLUME_MUTE"></span><span id="appcommand_volume_mute"></span><dl> <dt>**APPCOMMAND \_ \_Silenciar volumen**</dt> <dt>8</dt> </dl>                                                                       | Silenciar el volumen.<br/>                                                                                                                                                                                                                                                                |
| <span id="APPCOMMAND_VOLUME_UP"></span><span id="appcommand_volume_up"></span><dl> <dt>**APPCOMMAND \_ VOLUMEN \_ hasta**</dt> <dt>10</dt> </dl>                                                                            | Eleve el volumen.<br/>                                                                                                                                                                                                                                                               |



 

El componente *uDevice* indica el dispositivo de entrada que generó el evento de entrada y puede tener uno de los valores siguientes.



| Value                                                                                                                                                                                                                                 | Significado                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span id="FAPPCOMMAND_KEY"></span><span id="fappcommand_key"></span><dl> <dt>**FAPPCOMMAND \_ CLAVE**</dt> <dt>0</dt> </dl>            | El usuario presionó una tecla.<br/>                                                                           |
| <span id="FAPPCOMMAND_MOUSE"></span><span id="fappcommand_mouse"></span><dl> <dt>**FAPPCOMMAND \_ MOUSE**</dt> <dt>0x8000</dt> </dl> | El usuario hizo clic en un botón del mouse.<br/>                                                                  |
| <span id="FAPPCOMMAND_OEM"></span><span id="fappcommand_oem"></span><dl> <dt>**FAPPCOMMAND \_**</dt> <dt>0x1000</dt> OEM </dl>       | Un origen de hardware no identificado generó el evento. Podría ser un mouse o un evento de teclado.<br/> |



 

El componente *dwKeys* indica si varias claves virtuales están inactivas y puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                                                               | Significado                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_**</dt> <dt>0X0008</dt> de control </dl>    | La tecla CTRL está presionada.<br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt> </dl>    | El botón primario del mouse está inactivo.<br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt> </dl>    | El botón central del mouse está presionado.<br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt> </dl>    | El botón secundario del mouse está inactivo.<br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt> </dl>          | La tecla Mayús está presionada.<br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt> </dl> | El primer botón X está inactivo.<br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt> </dl> | El segundo botón X está inactivo.<br/>     |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver **true**. Para obtener más información sobre cómo procesar el valor devuelto, vea la sección Comentarios.

## <a name="remarks"></a>Observaciones

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) genera el mensaje de **\_ APPCOMMAND de WM** cuando procesa el mensaje de [**WM \_ XBUTTONUP**](wm-xbuttonup.md) o [**WM \_ NCXBUTTONUP**](wm-ncxbuttonup.md) , o cuando el usuario escribe una tecla de comando de aplicación.

Si una ventana secundaria no procesa este mensaje y, en su lugar, llama a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), **DefWindowProc** enviará el mensaje a su ventana primaria. Si una ventana de nivel superior no procesa este mensaje y, en su lugar, llama a **DefWindowProc**, **DefWindowProc** llamará a un enlace de Shell con el código de enlace igual a **HSHELL \_ APPCOMMAND**.

Para obtener las coordenadas del cursor si el mensaje se ha generado con un clic del mouse, la aplicación puede llamar a [**GetMessagePos**](/windows/desktop/api/winuser/nf-winuser-getmessagepos). Una aplicación puede comprobar si el mensaje fue generado por el mouse comprobando si *lParam* contiene **FAPPCOMMAND \_ mouse**.

A diferencia de otros mensajes de Windows, una aplicación debe devolver **true** desde este mensaje si lo procesa. Esto permitirá que el software que simula este mensaje en sistemas Windows anteriores a Windows 2000 determine si el procedimiento de ventana procesó el mensaje o llamó a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para procesarlo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**OBTENER \_ APPCOMMAND \_ lParam**](/windows/win32/api/winuser/nf-winuser-get_appcommand_lparam)
</dt> <dt>

[**OBTENCIÓN del \_ dispositivo \_ lParam**](/windows/win32/api/winuser/nf-winuser-get_device_lparam)
</dt> <dt>

[**OBTENER \_ KEYSTATE \_ lParam**](/windows/win32/api/winuser/nf-winuser-get_keystate_lparam)
</dt> <dt>

[**ShellProc**](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85))
</dt> <dt>

[**XBUTTONUP de WM \_**](wm-xbuttonup.md)
</dt> <dt>

[**NCXBUTTONUP de WM \_**](wm-ncxbuttonup.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Entrada del mouse](mouse-input.md)
</dt> </dl>

 

