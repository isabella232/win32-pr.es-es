---
description: Especifica una función de devolución de llamada definida por la aplicación a la que llama el Administrador de archivos para comunicarse con una extensión del Administrador de archivos.
title: Función de devolución de llamada FMExtensionProc (Wfext.h)
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
ms.openlocfilehash: 7cd13fe534f3bb121a4056f67ceff47ddfa71fa5506c2020a243ab340768ce35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032663"
---
# <a name="fmextensionproc-callback-function"></a>Función de devolución de llamada FMExtensionProc

Especifica una función de devolución de llamada definida por la aplicación a la que llama el Administrador de archivos para comunicarse con una extensión del Administrador de archivos.

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

*Hwnd* 
</dt> <dd>

Tipo: **HWND**

Identificador de ventana para el Administrador de archivos. Una extensión usa este identificador para especificar la ventana primaria de cualquier cuadro de diálogo o cuadro de mensaje que debe mostrar y para enviar mensajes de consulta al Administrador de archivos.

</dd> <dt>

*wMsg* 
</dt> <dd>

Tipo: **WORD**

Uno de los siguientes mensajes del Administrador de archivos.

<dt>

<span id="1_through_99"></span><span id="1_THROUGH_99"></span>

<span id="1_through_99"></span><span id="1_THROUGH_99"></span>**De 1 a 99**


</dt> <dd>

El usuario ha seleccionado un elemento en el menú proporcionado por la extensión. El valor es el identificador del elemento de menú seleccionado.

</dd> <dt>

<span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>

<span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>**FMEVENT \_ HELPMENUITEM**


</dt> <dd>

El usuario presionó F1 al seleccionar un menú de extensión o un elemento de comando de la barra de herramientas. Indica que la extensión debe llamar a **WinHelp correctamente** para el elemento de comando.

</dd> <dt>

<span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>

<span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>**FMEVENT \_ HELPSTRING**


</dt> <dd>

El usuario seleccionó un menú de extensión o un elemento de comando de la barra de herramientas. Indica que la extensión debe proporcionar una cadena de Ayuda.

</dd> <dt>

<span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>

<span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>**FMEVENT \_ INITMENU**


</dt> <dd>

El usuario ha seleccionado el menú de la extensión. La extensión debe inicializar elementos en el menú.

</dd> <dt>

<span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>

<span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>**CARGA DE \_ FMEVENT**


</dt> <dd>

El Administrador de archivos carga el archivo DLL de extensión y solicita al archivo DLL información sobre el menú que proporciona el archivo DLL.

</dd> <dt>

<span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>

<span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>**FMEVENT \_ SELCHANGE**


</dt> <dd>

La selección en la **ventana del directorio del Administrador** de archivos o en la ventana **Resultados de** la búsqueda ha cambiado.

</dd> <dt>

<span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>

<span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>**FMEVENT \_ TOOLBARLOAD**


</dt> <dd>

El Administrador de archivos crea la barra de herramientas y solicita al archivo DLL de extensión información sobre los botones que el archivo DLL agrega a la barra de herramientas.

</dd> <dt>

<span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>

<span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>**FMEVENT \_ UNLOAD**


</dt> <dd>

El Administrador de archivos está descargando el archivo DLL de extensión.

</dd> <dt>

<span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>

<span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>**ACTUALIZACIÓN DE USUARIO \_ DE \_ FMEVENT**


</dt> <dd>

El usuario **seleccionó el comando** Actualizar en el **menú** Ventana. La extensión debe actualizar los elementos del menú, si es necesario.

</dd> </dl> </dd> <dt>

*lParam* 
</dt> <dd>

Tipo: **LONG**

Valor específico del mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LONG**

Devuelve un valor que depende del mensaje del parámetro *wMsg.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **FMExtensionProcW** (Unicode)<br/>                                          |



 

 




