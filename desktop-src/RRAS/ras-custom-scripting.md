---
title: Scripting personalizado de RAS
description: Los programadores pueden crear un archivo DLL de scripting personalizado que resida en un equipo cliente RAS. Este archivo DLL puede comunicarse con el servidor durante el proceso de establecer una conexión.
ms.assetid: c27b8b02-6018-4441-a355-1fb890b9001c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c625f020d9dafcb352c5f1b382014f9dba189330
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995363"
---
# <a name="ras-custom-scripting"></a>Scripting personalizado de RAS

Los programadores pueden crear un archivo DLL de scripting personalizado que resida en un equipo cliente RAS. Este archivo DLL puede comunicarse con el servidor durante el proceso de establecer una conexión.

**Windows NT:** El scripting personalizado no está disponible.

## <a name="setting-up-the-dll"></a>Configurar el archivo DLL

Para configurar el archivo DLL, cree un valor con el nombre **CustomScriptDllPath** en la siguiente clave del registro:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               Parameters
```

Este valor debe ser de tipo **reg \_ Expand \_**. El valor debe contener la ruta de acceso al archivo DLL de scripting personalizado. Solo se admite un archivo DLL de scripting personalizado para cada equipo cliente RAS.

## <a name="interaction-between-the-server-ras-and-the-custom-scripting-dll"></a>Interacción entre el servidor, el RAS y el Custom-Scripting DLL

El archivo DLL de scripting personalizado debe exportar un único punto de entrada: [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn). RAS llama a esta función durante el \_ Estado interactivo RASCS del proceso de conexión. El \_ Estado interactivo de RASCS es un estado de pausa, que permite al usuario interactuar con una interfaz de usuario presentada por el archivo dll de scripting personalizado. Consulte [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) para obtener más información sobre los Estados de conexión.

RAS pasará como parámetros a la función [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) :

-   Identificador del puerto en el equipo cliente que se utiliza para la conexión.
-   Cadenas que identifican la libreta de teléfonos y la entrada para la conexión.
-   RAS también pasa un identificador a una ventana para permitir que el archivo DLL presente una interfaz de usuario.
-   Un conjunto de punteros de función que el archivo DLL puede utilizar para comunicarse con el servidor.

Vea [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) para obtener más información sobre estos parámetros.

RAS pasa un puntero a una estructura [**RASCUSTOMSCRIPTEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa376738(v=vs.85)) como el último parámetro a [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn). Esta estructura contiene un puntero a una función de tipo [**PFNRASSETCOMMSETTINGS**](/windows/desktop/api/Ras/nc-ras-pfnrassetcommsettings). La DLL de scripting personalizado llama a esta función para modificar la configuración de comunicación en el puerto utilizado por la conexión.

RAS media la interacción entre el servidor y el archivo DLL de scripting personalizado. Normalmente, el servidor inicia el cuadro de diálogo. Por ejemplo, el servidor puede solicitar el nombre de usuario y la contraseña del usuario.

Al utilizar el script personalizado para establecer una conexión, el servidor no necesita ejecutar Windows NT 4,0 o Windows 2000.

## <a name="custom-scripting-user-interface-must-support-idcancel"></a>La interfaz de usuario de scripting personalizado debe ser compatible con IDCANCEL

Si el marcador personalizado muestra una interfaz de usuario, la interfaz de usuario debe admitir \_ mensajes de comandos de WM en los que LOWORD (*wParam*) es igual a IDCANCEL.

## <a name="configuring-the-connection"></a>Configuración de la conexión

El punto de entrada [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) se puede invocar desde [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) o, en Windows XP, desde [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala).

Para invocar [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) desde [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga), establezca la \_ opción RASEO CustomScript en la entrada de la libreta de teléfonos para la conexión. Vea el miembro **dwfOptions** de [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) para obtener una descripción de las opciones de entrada de la libreta de teléfonos. Use las funciones [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) y [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) para establecer esta opción mediante programación.

**Windows XP:** Para invocar [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) desde [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala), la llamada a **rasdial** debe especificar una estructura [**RASDIALEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)) y esta estructura debe especificar la \_ marca RDEOPT UseCustomScripting. Además, la entrada de la libreta de teléfonos para la conexión debe especificar la \_ opción RASEO CustomScript, tal como se describe en el párrafo anterior.

## <a name="invoking-the-custom-scripting-dll"></a>Invocar el archivo DLL de scripting personalizado

Si el usuario activa una conexión para una entrada de libreta de teléfonos que tiene RASEO \_ CustomScript establecido, Ras invoca el archivo dll de scripting personalizado. En este escenario, RAS invoca la DLL de scripting personalizado desde [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga).

Para invocar el archivo DLL de scripts personalizados mediante programación, establezca la conexión con la función [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) . En Windows XP, la función [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) también invoca el archivo dll de scripting personalizado.

 

 