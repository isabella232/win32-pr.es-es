---
description: El método Message del objeto Session realiza cualquier operación de registro habilitada y pospone la ejecución al objeto de controlador de interfaz de usuario asociado al motor. Es posible que el registro esté habilitado de forma selectiva para los distintos tipos de mensajes. Vea el método EnableLog.
ms.assetid: 09053700-a641-4970-bf55-d7c81f345257
title: Session. Message (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Message
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e20cfebe0a3359a99770cbd242501649bf93f86e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653980"
---
# <a name="sessionmessage-method"></a>Session. Message (método)

El método **Message** del objeto [**Session**](session-object.md) realiza cualquier operación de registro habilitada y pospone la ejecución al objeto de controlador de interfaz de usuario asociado al motor. Es posible que el registro esté habilitado de forma selectiva para los distintos tipos de mensajes. Vea el método [**EnableLog**](installer-enablelog.md) .

Si el campo de registro 0 contiene una cadena de formato, se utiliza para dar formato a los datos de los demás campos. De lo contrario, si el mensaje es un error, una advertencia o un mensaje de usuario, se realiza un intento de buscar una plantilla de mensaje en la tabla de errores de la base de datos actual con el número de error encontrado en el campo 1 del registro para los tipos de mensaje y los valores devueltos.

## <a name="syntax"></a>Sintaxis


```JScript
Session.Message(
  kind,
  record
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*tipo* 
</dt> <dd>

El parámetro *Kind* debe ser uno de los valores siguientes. Para mostrar un cuadro de mensaje con botones e iconos de inserciones, calcule el valor de *Kind* agregando los estilos de cuadro de mensaje estándar usados por [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) y [**MessageBoxEx**](/windows/win32/api/winuser/nf-winuser-messageboxexa) a **msiMessageTypeError**, **msiMessageTypeWarning** o **msiMessageTypeUser**. Para obtener más información, vea la sección Comentarios a continuación.



| Constante                                                                                                                                                                                                                                                                                                                 | Significado                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiMessageTypeFatalExit"></span><span id="msimessagetypefatalexit"></span><span id="MSIMESSAGETYPEFATALEXIT"></span><dl> <dt>**msiMessageTypeFatalExit**</dt> <dt>&H00000000</dt> </dl>                     | Finalización prematura, posible falta de memoria.<br/>                                                                              |
| <span id="msiMessageTypeError"></span><span id="msimessagetypeerror"></span><span id="MSIMESSAGETYPEERROR"></span><dl> <dt>**msiMessageTypeError**</dt> <dt>&H01000000</dt> </dl>                                     | Mensaje de error con formato, \[ 1 \] es el número de mensaje en la [tabla de errores](error-table.md).<br/>                                               |
| <span id="msiMessageTypeWarning"></span><span id="msimessagetypewarning"></span><span id="MSIMESSAGETYPEWARNING"></span><dl> <dt>**msiMessageTypeWarning**</dt> <dt>&H02000000</dt> </dl>                             | Mensaje de advertencia con formato, \[ 1 \] es el número de mensaje en la [tabla de errores](error-table.md).<br/>                                             |
| <span id="msiMessageTypeUser_"></span><span id="msimessagetypeuser_"></span><span id="MSIMESSAGETYPEUSER_"></span><dl> <dt> **msiMessageTypeUser**</dt> <dt>&H03000000</dt> </dl>                                     | Mensaje de solicitud de usuario, \[ 1 \] es el número de mensaje en la [tabla de errores](error-table.md).<br/>                                                  |
| <span id="msiMessageTypeInfo"></span><span id="msimessagetypeinfo"></span><span id="MSIMESSAGETYPEINFO"></span><dl> <dt>**msiMessageTypeInfo**</dt> <dt>&H04000000</dt> </dl>                                         | Mensaje informativo para el registro; no se mostrará.<br/>                                                                                 |
| <span id="msiMessageTypeFilesInUse"></span><span id="msimessagetypefilesinuse"></span><span id="MSIMESSAGETYPEFILESINUSE"></span><dl> <dt>**msiMessageTypeFilesInUse**</dt> <dt>&H05000000</dt> </dl>                 | Lista de archivos en uso que se deben reemplazar.<br/>                                                                                    |
| <span id="msiMessageTypeResolveSource"></span><span id="msimessagetyperesolvesource"></span><span id="MSIMESSAGETYPERESOLVESOURCE"></span><dl> <dt>**msiMessageTypeResolveSource**</dt> <dt>&H06000000</dt> </dl>     | Solicitud para determinar una ubicación de origen válida.<br/>                                                                                     |
| <span id="msiMessageTypeOutOfDiskSpace"></span><span id="msimessagetypeoutofdiskspace"></span><span id="MSIMESSAGETYPEOUTOFDISKSPACE"></span><dl> <dt>**msiMessageTypeOutOfDiskSpace**</dt> <dt>&H07000000</dt> </dl> | Mensaje de espacio en disco insuficiente.<br/>                                                                                                  |
| <span id="msiMessageTypeActionStart"></span><span id="msimessagetypeactionstart"></span><span id="MSIMESSAGETYPEACTIONSTART"></span><dl> <dt>**msiMessageTypeActionStart**</dt> <dt>&H08000000</dt> </dl>             | Inicio de la acción, \[ 1 \] nombre de acción, \[ 2 \] Descripción, \[ 3 \] plantilla para mensajes ACTIONDATA.<br/>                                    |
| <span id="msiMessageTypeActionData"></span><span id="msimessagetypeactiondata"></span><span id="MSIMESSAGETYPEACTIONDATA"></span><dl> <dt>**msiMessageTypeActionData**</dt> <dt>&H09000000</dt> </dl>                 | Datos de la acción. Los campos de registro corresponden a la plantilla del mensaje ACTIONSTART.<br/>                                                     |
| <span id="msiMessageTypeProgress"></span><span id="msimessagetypeprogress"></span><span id="MSIMESSAGETYPEPROGRESS"></span><dl> <dt>**msiMessageTypeProgress**</dt> <dt>&H0A000000</dt> </dl>                         | Información de la barra de progreso. Vea la descripción de los campos de registro a continuación.<br/>                                                             |
| <span id="msiMessageTypeCommonData_"></span><span id="msimessagetypecommondata_"></span><span id="MSIMESSAGETYPECOMMONDATA_"></span><dl> <dt> **msiMessageTypeCommonData**</dt> <dt>&H0B000000</dt> </dl>             | Para habilitar el botón Cancelar \[ , establezca 1 \] en 2 y \[ 2 \] en 1. <br/> Para deshabilitar el botón Cancelar \[ establecido \] en 1 a 2 y \[ 2 \] en 0<br/> |



 

</dd> <dt>

*record* 
</dt> <dd>

Objeto de [**registro**](record-object.md) necesario que contiene un campo específico del mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto



| Constante                                                                                              | Value         |
|-------------------------------------------------------------------------------------------------------|---------------|
| <dl> <dt>**msiMessageStatusError**</dt> </dl>  | -1<br/> |
| <dl> <dt>**msiMessageStatusNone**</dt> </dl>   | 0<br/>  |
| <dl> <dt>**msiMessageStatusOk**</dt> </dl>     | 1<br/>  |
| <dl> <dt>**msiMessageStatusCancel**</dt> </dl> | 2<br/>  |
| <dl> <dt>**msiMessageStatusAbort**</dt> </dl>  | 3<br/>  |
| <dl> <dt>**msiMessageStatusRetry**</dt> </dl>  | 4<br/>  |
| <dl> <dt>**msiMessageStatusIgnore**</dt> </dl> | 5<br/>  |
| <dl> <dt>**msiMessageStatusYes**</dt> </dl>    | 6<br/>  |
| <dl> <dt>**msiMessageStatusNo**</dt> </dl>     | 7<br/>  |



 

## <a name="remarks"></a>Observaciones

**Campos de registro de mensajes**

A continuación se describen las definiciones de campos de registro cuando se pasa msiMessageTypeProgress como el tipo de mensaje.

El campo 1 especifica el tipo de mensaje de progreso. El significado de los demás campos depende del valor de este campo. Los valores posibles que se pueden establecer en el campo 1 son los siguientes.



| Nombre del mensaje     | Value | Descripción del campo 1                                                                                                 |
|------------------|-------|---------------------------------------------------------------------------------------------------------------------|
| MasterReset      | 0     | Restablece la barra de progreso y establece el número total esperado de TICs en la barra.                                         |
| ActionInfo       | 1     | Proporciona información relacionada con los mensajes de progreso que va a enviar la acción actual.                                 |
| ProgressReport   | 2     | Incrementa la barra de progreso.                                                                                        |
| ProgressAddition | 3     | Habilita una acción (como CustomAction) para agregar TICs al número total esperado de progreso de la barra de progreso. |



 

El significado del campo 2 depende del valor del campo 1 como se indica a continuación.



| Valor del campo 1 | Descripción del campo 2                                                                                        |
|---------------|------------------------------------------------------------------------------------------------------------|
| 0             | Se esperaba el número total de TICs en la barra de progreso.                                                        |
| 1             | Número de pasos que la barra de progreso mueve para cada mensaje de ActionData. Este campo se omite si el campo 3 es 0. |
| 2             | Número de pasos que se ha desplace la barra de progreso.                                                                |
| 3             | Número de pasos que se van a agregar al progreso total esperado.                                                         |



 

El significado del campo 3 depende del valor del campo 1 como se indica a continuación.



| Valor del campo 1 | Valor del campo 3 | Descripción del campo 3                                                                                             |
|---------------|---------------|-----------------------------------------------------------------------------------------------------------------|
| 0             | 0             | Barra de progreso de avance (de izquierda a derecha)                                                                            |
|               | 1             | Barra de progreso hacia atrás (de derecha a izquierda)                                                                           |
| 1             | 0             | La acción actual enviará mensajes ProgressReport explícitos.                                                  |
|               | 1             | Incremente la barra de progreso en función del número de pasos especificados en el campo 2 cada vez que se envíe un mensaje de ActionData. |
| 2             | No utilizado        |                                                                                                                 |
| 3             | No utilizado        |                                                                                                                 |



 

El significado del campo 4 depende del valor del campo 1 como se indica a continuación.



| Valor del campo 1 | Valor del campo 4 | Descripción del campo 4                                                                                                                                 |
|---------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| 0             | 0             | La ejecución está en curso. En este caso, la interfaz de usuario podría calcular y mostrar el tiempo restante.                                                      |
|               | 1             | Crear el script de ejecución. En este caso, la interfaz de usuario podría mostrar un mensaje para esperar mientras el instalador termina de preparar la instalación. |
| 1             | No utilizado        |                                                                                                                                                     |
| 2             | No utilizado        |                                                                                                                                                     |
| 3             | No utilizado        |                                                                                                                                                     |



 

**Mostrar cuadros de mensaje**

Para mostrar un cuadro de mensaje con botones e iconos de inserciones, calcule el valor de *Kind* agregando los estilos de cuadro de mensaje estándar usados por **MessageBox** y **MessageBoxEx** a **msiMessageTypeError**, **msiMessageTypeWarning** o **msiTypeUser**. Las opciones disponibles del botón de opción para VBScript son vbOKOnly (MB \_ OK), vbOKCancel (MB \_ OKCANCEL), VBABORTRETRYIGNORE (MB \_ ABORTRETRYIGNORE), vbYesNoCancel (MB \_ YESNOCANCEL), vbYesNo (MB \_ SÍNO) y vbRetryCancel (MB \_ RETRYCANCEL). Las opciones de icono disponibles para VBScript son vbCritical (MB \_ ICONERROR), vbQuestion (MB \_ ICONQUESTION), VBEXCLAMATION (MB \_ ICONWARNING) y vbInformation (MB \_ ICONINFORMATION).

Por ejemplo, la siguiente llamada envía un mensaje **msiMessageTypeError** con los botones VbExclamation y vbYesNo.


```VB
Session.Message &H01000034, record
```



Si una acción personalizada llama al método de **mensaje** , la acción personalizada debe ser capaz de controlar una cancelación por parte del usuario y debe devolver **msiDoActionStatusUserExit**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 
