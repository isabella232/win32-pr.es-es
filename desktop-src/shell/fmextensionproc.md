---
description: Especifica una función de devolución de llamada definida por la aplicación llamada por el administrador de archivos para comunicarse con una extensión del administrador de archivos.
title: Función de devolución de llamada FMExtensionProc (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMExtensionProc
- FMExtensionProcW
api_type:
- UserDefined
api_location:
- Wfext.h
ms.assetid: 6e02d655-f7d8-460a-97d2-5b369493e941
ms.openlocfilehash: 40e18dfe64c6d2b24b982cdf891cbb63b091a7ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997212"
---
# <a name="fmextensionproc-callback-function"></a>Función de devolución de llamada FMExtensionProc

Especifica una función de devolución de llamada definida por la aplicación llamada por el administrador de archivos para comunicarse con una extensión del administrador de archivos.

## <a name="syntax"></a>Sintaxis


```C++
LONG CALLBACK FMExtensionProc(
   HWND hwnd,
   WORD wMsg,
   LONG lParam
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*identificador* 
</dt> <dd>

Tipo: **hWnd**

Identificador de ventana para el administrador de archivos. Una extensión usa este identificador para especificar la ventana primaria de cualquier cuadro de diálogo o cuadro de mensaje que debe mostrar, y para enviar mensajes de consulta al administrador de archivos.

</dd> <dt>

*wMsg* 
</dt> <dd>

Tipo: **Word**

Uno de los siguientes mensajes del administrador de archivos.

<dt>

<span id="1_through_99"></span><span id="1_THROUGH_99"></span>

<span id="1_through_99"></span><span id="1_THROUGH_99"></span>**de 1 a 99**


</dt> <dd>

El usuario seleccionó un elemento en el menú proporcionado por la extensión. El valor es el identificador del elemento de menú seleccionado.

</dd> <dt>

<span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>

<span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>**FMEVENT \_ HELPMENUITEM**


</dt> <dd>

El usuario presionó F1 al seleccionar un menú de extensión o un elemento de comando de barra de herramientas. Indica que la extensión debe llamar a **WinHelp** adecuadamente para el elemento de comando.

</dd> <dt>

<span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>

<span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>**FMEVENT \_ HELPSTRING**


</dt> <dd>

El usuario seleccionó un menú de extensión o un elemento de comando de barra de herramientas. Indica que la extensión debe proporcionar una cadena de ayuda.

</dd> <dt>

<span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>

<span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>**FMEVENT \_ INITMENU**


</dt> <dd>

El usuario seleccionó el menú de la extensión. La extensión debe inicializar los elementos en el menú.

</dd> <dt>

<span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>

<span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>**carga de FMEVENT \_**


</dt> <dd>

El administrador de archivos está cargando el archivo DLL de extensión y solicita al archivo DLL información sobre el menú que suministra el archivo DLL.

</dd> <dt>

<span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>

<span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>**FMEVENT \_ SELCHANGE**


</dt> <dd>

Ha cambiado la selección en la ventana Directorio del **Administrador de archivos** o en la ventana Resultados de la **búsqueda** .

</dd> <dt>

<span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>

<span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>**FMEVENT \_ TOOLBARLOAD**


</dt> <dd>

El administrador de archivos está creando la barra de herramientas y solicita al archivo DLL de extensión información sobre los botones que el archivo DLL agrega a la barra de herramientas.

</dd> <dt>

<span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>

<span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>**descarga de FMEVENT \_**


</dt> <dd>

El administrador de archivos está descargando el archivo DLL de extensión.

</dd> <dt>

<span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>

<span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>**\_actualización de usuarios de FMEVENT \_**


</dt> <dd>

El usuario seleccionó el comando **Actualizar** en el menú **ventana** . La extensión debe actualizar los elementos en el menú, si es necesario.

</dd> </dl> </dd> <dt>

*lParam* 
</dt> <dd>

Tipo: **Long**

Valor específico del mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **Long**

Devuelve un valor que depende del mensaje de parámetro *wMsg* .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **FMExtensionProcW** (Unicode)<br/>                                          |



 

 




