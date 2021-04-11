---
title: Mensaje de SB_SETTEXT (commctrl. h)
description: Establece el texto de la parte especificada de una ventana de estado.
ms.assetid: 6039a61c-6ec6-42cd-94d5-5f1cf2998586
keywords:
- SB_SETTEXT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SB_SETTEXT
- SB_SETTEXTA
- SB_SETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a466187b4ccd00a974b992eacec11938f45001da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150748"
---
# <a name="sb_settext-message"></a>Mensaje de SETTEXT de SB \_

Establece el texto de la parte especificada de una ventana de estado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

El [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) de la palabra de orden inferior especifica el índice de base cero del elemento que se va a establecer. Si **LOBYTE** se establece en SB \_ SIMPLEID, se supone que la ventana de estado es una barra de estado de modo simple; es decir, una barra de estado con una sola parte.

El [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) de la palabra de orden inferior especifica el tipo de la operación de dibujo. Este parámetro puede ser uno de los valores siguientes.

Se omite la palabra de orden superior de *wParam* .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="0"></span><dl> <dt><strong>0,1</strong></dt> </dl></td>
<td>El texto se dibuja con un borde para que aparezca inferior al plano de la ventana.<br/></td>
</tr>
<tr class="even">
<td><span id="SBT_NOBORDERS"></span><span id="sbt_noborders"></span><dl> <dt><strong>SBT_NOBORDERS</strong></dt> </dl></td>
<td>El texto se dibuja sin bordes.<br/></td>
</tr>
<tr class="odd">
<td><span id="SBT_OWNERDRAW"></span><span id="sbt_ownerdraw"></span><dl> <dt><strong>SBT_OWNERDRAW</strong></dt> </dl></td>
<td>El texto se dibuja mediante la ventana primaria. <br/>
<blockquote>
[!Note]<br />
Una barra de estado de modo simple no admite el dibujo del propietario.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="SBT_POPOUT"></span><span id="sbt_popout"></span><dl> <dt><strong>SBT_POPOUT</strong></dt> </dl></td>
<td>El texto se dibuja con un borde para que aparezca más arriba que el plano de la ventana.<br/></td>
</tr>
<tr class="odd">
<td><span id="SBT_RTLREADING"></span><span id="sbt_rtlreading"></span><dl> <dt><strong>SBT_RTLREADING</strong></dt> </dl></td>
<td>El texto se mostrará en la dirección opuesta al texto de la ventana primaria.<br/></td>
</tr>
<tr class="even">
<td><span id="SBT_NOTABPARSING"></span><span id="sbt_notabparsing"></span><dl> <dt><strong>SBT_NOTABPARSING</strong></dt> </dl></td>
<td>Se omiten los caracteres de tabulación.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una cadena terminada en null que especifica el texto que se va a establecer. Si *wParam* es SBT \_ OWNERDRAW, este parámetro representa 32 bits de datos. La ventana primaria debe interpretar los datos y dibujar el texto cuando recibe el mensaje [**de \_ DRAWITEM de WM**](wm-drawitem.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

El mensaje invalida la parte de la ventana que ha cambiado, lo que hace que muestre el nuevo texto cuando la ventana siguiente recibe el mensaje [**de \_ dibujo de WM**](/windows/desktop/gdi/wm-paint) .

Texto normal de la pantalla de Windows de izquierda a derecha (LTR). Las ventanas se pueden *reflejar* para mostrar idiomas como el hebreo o el árabe que se leen de derecha a izquierda (RTL). Si \_ se establece SBT RTLREADING, la cadena *lParam* leerá en la dirección opuesta del texto de la ventana primaria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **SB \_ SETTEXTW** (Unicode) y **SB \_ SETTEXTA** (ANSI)<br/>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GETTEXT de SB \_**](sb-gettext.md)
</dt> </dl>

 

