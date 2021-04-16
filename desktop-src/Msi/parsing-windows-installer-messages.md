---
description: Un controlador de interfaz de usuario externo puede procesar la lista de mensajes de instalador especificados por el parámetro dwMessagedFilter de la función MsiSetExternalUI.
ms.assetid: c4405803-9abd-40f4-9090-c075e7dcf293
title: Analizar mensajes de Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65cf96c85499b44accd0e01548ca184a030775d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276166"
---
# <a name="parsing-windows-installer-messages"></a>Analizar mensajes de Windows Installer

Un controlador de interfaz de usuario externo puede procesar la lista de mensajes de instalador especificados por el parámetro *dwMessagedFilter* de la función [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) . Algunos de estos mensajes contienen cadenas que se pueden usar directamente, y es posible que el controlador de la interfaz de usuario externa deba analizar y procesar otros mensajes para que sean útiles. Es posible que el controlador de la interfaz de usuario externa solo necesite supervisar Windows Installer mensajes sin realizar ninguna operación que afecte a la instalación.

Los siguientes mensajes de Windows Installer contienen cadenas que se pueden mostrar en un cuadro de diálogo y no necesitan ningún procesamiento adicional. Estos mensajes contienen una lista de botones e iconos que se mostrarán en un cuadro de diálogo. Puede usar los valores **MB \_ ICONMASK**, **MB \_ DEFMASK** y **MB \_ TYPEMASK** para especificar iconos y botones.

<dl> <dt>

<span id="INSTALLMESSAGE_FATALEXIT"></span><span id="installmessage_fatalexit"></span>**INSTALLMESSAGE \_ FATALEXIT**
</dt> <dd>

Se ha producido una terminación prematura de la instalación.

</dd> <dt>

<span id="INSTALLMESSAGE_ERROR"></span><span id="installmessage_error"></span>**\_error INSTALLMESSAGE**
</dt> <dd>

Mensaje de error con formato.

</dd> <dt>

<span id="INSTALLMESSAGE_WARNING"></span><span id="installmessage_warning"></span>**ADVERTENCIA de INSTALLMESSAGE \_**
</dt> <dd>

Mensaje de advertencia con formato.

</dd> <dt>

<span id="INSTALLMESSAGE_INFO"></span><span id="installmessage_info"></span>**información de INSTALLMESSAGE \_**
</dt> <dd>

Mensaje de registro con formato.

</dd> <dt>

<span id="INSTALLMESSAGE_USER"></span><span id="installmessage_user"></span>**\_usuario INSTALLMESSAGE**
</dt> <dd>

Mensaje de usuario con formato.

</dd> <dt>

<span id="INSTALLMESSAGE_OUTOFDISKSPACE"></span><span id="installmessage_outofdiskspace"></span>**INSTALLMESSAGE \_ OUTOFDISKSPACE**
</dt> <dd>

Mensaje con formato que indica una condición de espacio insuficiente en disco

</dd> </dl>

El controlador de usuario externo puede usar los siguientes mensajes de Windows Installer para supervisar una secuencia de la interfaz de usuario de Windows Installer. El instalador envía estos mensajes al principio de una secuencia de interfaz de usuario Windows Installer, como se muestra cada cuadro de diálogo, y al final de la secuencia de interfaz de usuario. No se requiere ningún procesamiento para usar estos mensajes.

<dl> <dt>

<span id="INSTALLMESSAGE_TERMINATE"></span><span id="installmessage_terminate"></span>\_Finalizar INSTALLMESSAGE
</dt> <dd>

Este mensaje indica el final de la secuencia de la interfaz de usuario. La cadena es una cadena nula.

</dd> <dt>

<span id="INSTALLMESSAGE_INITIALIZE"></span><span id="installmessage_initialize"></span>INSTALLMESSAGE \_ inicializar
</dt> <dd>

Este mensaje indica que se ha iniciado la secuencia de la interfaz de usuario. La cadena es una cadena nula.

</dd> <dt>

<span id="INSTALLMESSAGE_SHOWDIALOG"></span><span id="installmessage_showdialog"></span>INSTALLMESSAGE \_ SHOWDIALOG
</dt> <dd>

La cadena contiene el nombre del cuadro de diálogo actual.

</dd> </dl>

Los siguientes mensajes de Windows Installer requieren un procesamiento adicional por parte del controlador de la interfaz de usuario externa.

<dl> <dt>

<span id="INSTALLMESSAGE_RESOLVESOURCE"></span><span id="installmessage_resolvesource"></span>**INSTALLMESSAGE \_ RESOLVESOURCE**
</dt> <dd>

El controlador de la interfaz de usuario externa debe devolver 0 y permitir que Windows Installer controle el mensaje. El controlador de la interfaz de usuario externa puede supervisar este mensaje, pero no debe realizar ninguna acción que afecte a la instalación.

</dd> <dt>

<span id="INSTALLMESSAGE_FILESINUSE"></span><span id="installmessage_filesinuse"></span>**INSTALLMESSAGE \_ FILESINUSE**
</dt> <dd>

La interfaz de usuario externa debería mostrar un [cuadro de diálogo FilesInUse](filesinuse-dialog.md) en respuesta a este mensaje.

</dd> <dt>

<span id="INSTALLMESSAGE_RMFILESINUSE"></span><span id="installmessage_rmfilesinuse"></span>**INSTALLMESSAGE \_ RMFILESINUSE**
</dt> <dd>

La interfaz de usuario externa debería mostrar un [cuadro de diálogo MsiRMFilesInUse](msirmfilesinuse-dialog.md) en respuesta a este mensaje. Disponible a partir de Windows Installer versión 4,0. Para obtener más información sobre este mensaje, consulte [uso del administrador de reinicio con una interfaz de usuario externa](using-restart-manager-with-an-external-ui-.md).

</dd> <dt>

<span id="INSTALLMESSAGE_ACTIONSTART"></span><span id="installmessage_actionstart"></span>**INSTALLMESSAGE \_ ACTIONSTART**
</dt> <dd>

Este mensaje proporciona información acerca de la acción actual. El formato es la acción \[ 1 \] : \[ 2 \] . \[3 \] , donde se usa un signo de dos puntos para separar el campo 1 y el campo 2 y se utiliza un punto para separar el campo 2 y el campo 3. El campo \[ 1 \] contiene la hora a la que se inició la acción mediante el formato de la propiedad [**Time**](time.md) . El campo \[ 2 \] contiene el nombre de la acción de la tabla de secuencia. El campo \[ 3 \] proporciona la descripción de la acción de la [tabla ActionText](actiontext-table.md) o de la función [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) .

</dd> <dt>

<span id="INSTALLMESSAGE_ACTIONDATA"></span><span id="installmessage_actiondata"></span>**INSTALLMESSAGE \_ ACTIONDATA**
</dt> <dd>

El formato de esta cadena se especifica mediante el valor de [plantilla](template.md) proporcionado en la [tabla ActionText](actiontext-table.md) o la función [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) . Puede haber un número ilimitado de mensajes de **INSTALLMESSAGE \_ ACTIONDATA** después del mensaje **\_ ACTIONSTART de INSTALLMESSAGE** .

</dd> <dt>

<span id="INSTALLMESSAGE_COMMONDATA"></span><span id="installmessage_commondata"></span>**INSTALLMESSAGE \_ COMMONDATA**
</dt> <dd>

Este mensaje tiene tres subtipos: Language, Caption y CancelShow. La cadena puede tener tres campos delimitados por un número seguido de un signo de dos puntos. No todos los campos son obligatorios. El mensaje puede ser una cadena nula o vacía ("").

<dl> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Módulo
</dt> <dd>

El campo 1 contiene el valor 0 para indicar que esta cadena contiene información de idioma. El campo 2 contiene un valor de [idioma](language.md) que es un identificador de idioma numérico (LANGID). El campo 3 es un valor que representa una página de códigos ANSI.

</dd> <dt>

<span id="Caption"></span><span id="caption"></span><span id="CAPTION"></span>Hayan
</dt> <dd>

El campo 1 contiene el valor 1 para indicar que esta cadena contiene el texto de una leyenda o título. El campo 2 contiene texto que puede usar un controlador de interfaz de usuario externo como título de título de un cuadro de diálogo. El campo 3 es NULL o una cadena vacía (""). El campo 3 puede no estar presente en el mensaje de leyenda.

</dd> <dt>

<span id="CancelShow"></span><span id="cancelshow"></span><span id="CANCELSHOW"></span>CancelShow
</dt> <dd>

El campo 1 contiene el valor 2 para indicar que esta cadena contiene información sobre si se debe mostrar el botón Cancelar. Si se debe ocultar el botón Cancelar, el campo 2 contiene el valor 0. Si el botón Cancelar debe estar visible, el campo 2 contiene el valor 1.

</dd> </dl> </dd> <dt>

<span id="INSTALLMESSAGE_PROGRESS"></span><span id="installmessage_progress"></span>progreso de INSTALLMESSAGE \_
</dt> <dd>

Este mensaje tiene cuatro subtipos: RESET, ActionInfo, ProgressReport y ProgressAddition. El controlador externo no debe actuar sobre ninguno de estos mensajes hasta que se reciba el primer mensaje de progreso de restablecimiento. Esto proporciona una estimación del número total de pasos de la barra de progreso.

<dl> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>Determinado
</dt> <dd>

El campo 1 contiene el valor 0 para indicar un restablecimiento de la barra de progreso. El campo 2 contiene el número total de TICs en la barra de progreso. El campo 3 contiene el valor 0 para el movimiento de la barra de progreso. El campo 3 contiene el valor 1 para el movimiento de la barra de progreso hacia atrás. El valor 0 en el campo 4 significa que la instalación está en curso y se puede calcular el tiempo restante. El valor 1 en el campo 4 significa que se está ejecutando el script y que "espere..." se puede mostrar el mensaje. La estimación del número total de TICs es una aproximación y puede ser incorrecta.

</dd> <dt>

<span id="ActionInfo"></span><span id="actioninfo"></span><span id="ACTIONINFO"></span>ActionInfo
</dt> <dd>

El campo 1 contiene el valor 1 para indicar que esta cadena contiene información de la acción. El campo 2 contiene el número de pasos que la barra de progreso mueve para cada mensaje ActionData enviado por la acción actual. Si el campo 3 contiene el valor 0, omita el campo 2. Si el campo 3 contiene el valor 1, incremente la barra de progreso en el número de pasos en el campo 2 para cada mensaje ActionData enviado por la acción actual. El campo 4 no se usa.

</dd> <dt>

<span id="ProgressReport"></span><span id="progressreport"></span><span id="PROGRESSREPORT"></span>ProgressReport
</dt> <dd>

El campo 1 contiene el valor 2 para indicar que esta cadena contiene información de progreso. El campo 2 contiene el número de pasos que ha cambiado la barra de progreso. El campo 3 no se usa. El campo 4 no se usa.

</dd> <dt>

<span id="ProgressAddition"></span><span id="progressaddition"></span><span id="PROGRESSADDITION"></span>ProgressAddition
</dt> <dd>

El campo 1 contiene el valor 3 para indicar que una acción puede Agregar TICs en la barra de progreso. El campo 2 contiene el número de pasos que se van a agregar al recuento total esperado de TICs de progreso. El campo 3 no se usa. El campo 4 no se usa.

</dd> </dl> </dd> </dl>

 

 



