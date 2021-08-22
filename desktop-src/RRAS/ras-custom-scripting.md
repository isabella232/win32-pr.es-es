---
title: Scripting personalizado de RAS
description: Los desarrolladores pueden crear un archivo DLL de scripting personalizado que resida en un equipo cliente ras. Este archivo DLL puede comunicarse con el servidor durante el proceso de establecimiento de una conexión.
ms.assetid: c27b8b02-6018-4441-a355-1fb890b9001c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66ac0bd83b8d7c48ee8b0468d89a70d19a5e5e6555b9a8bc8ac86d66c8cd666e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673285"
---
# <a name="ras-custom-scripting"></a>Scripting personalizado de RAS

Los desarrolladores pueden crear un archivo DLL de scripting personalizado que resida en un equipo cliente ras. Este archivo DLL puede comunicarse con el servidor durante el proceso de establecimiento de una conexión.

**Windows NT:** El scripting personalizado no está disponible.

## <a name="setting-up-the-dll"></a>Configuración del archivo DLL

Para configurar el archivo DLL, cree un valor con el nombre **CustomScriptDllPath** en la siguiente clave del Registro:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               Parameters
```

Este valor debe ser de tipo **REG \_ EXPAND \_ SZ.** El valor debe contener la ruta de acceso al archivo DLL de scripting personalizado. Solo se admite un archivo DLL de scripting personalizado para cada equipo cliente RAS.

## <a name="interaction-between-the-server-ras-and-the-custom-scripting-dll"></a>Interacción entre el servidor, RAS y Custom-Scripting DLL

El archivo DLL de scripting personalizado debe exportar un único punto de entrada: [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn). RAS llama a esta función durante el estado interactivo de RASCS \_ del proceso de conexión. El estado interactivo de RASCS es un estado en pausa, que permite al usuario interactuar con una interfaz de usuario presentada por el archivo \_ DLL de scripting personalizado. Consulte [**RASCONNSTATE para**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) obtener más información sobre los estados de conexión.

RAS pasará como parámetros a la [**función RasCustomScriptExecute:**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn)

-   Identificador del puerto del equipo cliente que se usa para la conexión.
-   Cadenas que identifican la libreta de teléfonos y la entrada de la conexión.
-   RAS también pasa un identificador a una ventana para permitir que el archivo DLL presente una interfaz de usuario.
-   Conjunto de punteros de función que el archivo DLL puede usar para comunicarse con el servidor.

Vea [**RasCustomScriptExecute para**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) obtener más información sobre estos parámetros.

RAS pasa un puntero a una [**estructura RASCUSTOMSCRIPTEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa376738(v=vs.85)) como último parámetro a [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn). Esta estructura contiene un puntero a una función de tipo [**PFNRASSETCOMMSETTINGS**](/windows/desktop/api/Ras/nc-ras-pfnrassetcommsettings). El archivo DLL de scripting personalizado llama a esta función para modificar la configuración de comunicación en el puerto utilizado por la conexión.

RAS media la interacción entre el servidor y el archivo DLL de scripting personalizado. Normalmente, el servidor inicia el cuadro de diálogo. Por ejemplo, el servidor puede solicitar el nombre de usuario y la contraseña del usuario.

Cuando se usa scripting personalizado para establecer una conexión, el servidor no necesita ejecutarse Windows NT 4.0 o Windows 2000.

## <a name="custom-scripting-user-interface-must-support-idcancel"></a>Custom Scripting Interfaz de usuario debe admitir IDCANCEL

Si el marcador personalizado muestra una interfaz de usuario, la interfaz de usuario debe admitir mensajes WM COMMAND donde \_ LOWORD(*wParam*) es igual a IDCANCEL.

## <a name="configuring-the-connection"></a>Configuración de la conexión

El [**punto de entrada RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) se puede invocar desde [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) o, Windows XP, desde [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala).

Para invocar [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) desde [**RasDialDlg,**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga)establezca la opción RasEO CustomScript en la entrada de la libreta de \_ teléfonos de la conexión. Consulte el **miembro dwfOptions** de [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) para obtener una descripción de las opciones de entrada de la libreta de teléfonos. Use las [**funciones RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) y [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) para establecer esta opción mediante programación.

**Windows XP:** Para invocar [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) desde [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala), la llamada a **RasDial** debe especificar una estructura [**RASDIALEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)) y esta estructura debe especificar la marca RDEOPT \_ UseCustomScripting. Además, la entrada de la libreta de teléfonos para la conexión debe especificar la opción RASEO CustomScript como se \_ describe en el párrafo anterior.

## <a name="invoking-the-custom-scripting-dll"></a>Invocación del archivo DLL de scripting personalizado

Si el usuario activa una conexión para una entrada de la libreta de teléfonos que tiene establecido RASEO CustomScript, RAS invoca el archivo DLL de \_ scripting personalizado. En este escenario, RAS invoca el archivo DLL de scripting personalizado de [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga).

Para invocar el archivo DLL de scripting personalizado mediante programación, establezca la conexión mediante la [**función RasDialDlg.**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) En Windows XP, la [**función RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) también invoca el archivo DLL de scripting personalizado.

 

 