---
description: '\\Panel de control HKCU \\ escritorio.'
ms.assetid: e18ea3c8-ddac-4214-83be-106c28c3c327
title: SCRNSAVE.EXE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d6a5d50b002299fe38508b387926b0eed11141
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423427"
---
# <a name="scrnsaveexe"></a>SCRNSAVE.EXE

**\\Panel de control HKCU \\ escritorio**



| Tipo de datos | Intervalo       | Valor predeterminado |
|-----------|-------------|---------------|
| Registro \_ SZ   | *Nombre de archivo* | (Ninguna)        |



 

## <a name="description"></a>Descripción

Especifica el nombre del archivo ejecutable del protector de pantalla.

## <a name="change-method"></a>Cambiar método

Para cambiar el valor de esta entrada, en el panel de control, haga doble clic en **pantalla**, haga clic en la pestaña **protector de pantalla** y, a continuación, seleccione un protector de pantalla de la lista **protector de pantalla** .

También puede cambiar esta entrada con la función de la interfaz de programación de aplicaciones (API) **InstallScreenSaver**, que se exporta mediante Desk.cpl. Puede tener acceso a esta función con la línea de comandos **rundll32.exe desk.cpl,** *archivo* InstallScreenSaver, donde *archivo* es el nombre de un archivo ejecutable del protector de pantalla.

## <a name="activation-method"></a>Método de activación

Los cambios que se realicen en esta entrada entrarán en vigor la próxima vez que el sistema inicie un protector de pantalla. Los cambios realizados en esta entrada mientras se está ejecutando un protector de pantalla no tienen ningún efecto en el protector de pantalla en ejecución.

## <a name="notes"></a>Notas

-   Los sistemas operativos Windows agregan esta entrada al registro cuando se usa **Mostrar** en el panel de control para seleccionar un protector de pantalla. Si deshabilita todos los protectores de pantalla eligiendo **(ninguno)** en la lista de protectores de pantalla, el sistema operativo elimina esta entrada del registro y llama a la función [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) con *uiAction* igual a SPI \_ SETSCREENSAVEACTIVE y *uiParam* igual a **false**.
-   Esta entrada se puede sustituir por un valor de directiva de grupo en los sistemas que admiten directiva de grupo. Mientras el **nombre del archivo ejecutable del protector de pantalla** Directiva de grupo está habilitado, el sistema omite esta entrada. La configuración de esta configuración de Directiva se almacena en la entrada **SCRNSAVE.EXE** , que se encuentra en la subclave de **directivas** .

 

 
