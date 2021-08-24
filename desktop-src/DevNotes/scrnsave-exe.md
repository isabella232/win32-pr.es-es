---
description: HKCU \\ Panel de control \\ Desktop.
ms.assetid: e18ea3c8-ddac-4214-83be-106c28c3c327
title: SCRNSAVE.EXE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e1ac7c0f2ee9d87911c0db195df89e2c27dcf1b19c0e9dac70d1517b0ad30ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571355"
---
# <a name="scrnsaveexe"></a>SCRNSAVE.EXE

**HKCU \\ Panel de control \\ Desktop**



| Tipo de datos | Intervalo       | Valor predeterminado |
|-----------|-------------|---------------|
| REG \_ SZ   | *Nombre de archivo* | (Ninguna)        |



 

## <a name="description"></a>Descripción

Especifica el nombre del archivo ejecutable del protector de pantalla.

## <a name="change-method"></a>Cambiar método

Para cambiar el valor de esta entrada, en Panel de control doble  clic en Mostrar **,** haga clic en la pestaña Protector de pantalla y, a continuación, seleccione un protector de pantalla en la lista Protector **de** pantalla.

También puede cambiar esta entrada con la función **installScreenSaver** de la interfaz de programación de aplicaciones (API), que exporta Desk.cpl. Puede acceder a esta función con la línea de **comandosrundll32.exe desk.cpl,InstallScreenSaver** file *,* donde *file* es el nombre de un archivo ejecutable de protector de pantalla.

## <a name="activation-method"></a>Método de activación

Los cambios realizados en esta entrada se hacen efectivos la próxima vez que el sistema inicie un protector de pantalla. Los cambios realizados en esta entrada mientras se ejecuta un protector de pantalla no tienen ningún efecto en el protector de pantalla en ejecución.

## <a name="notes"></a>Notas

-   Windows sistemas operativos agregan esta entrada al Registro cuando se usa **Mostrar** en Panel de control para seleccionar un protector de pantalla. Si deshabilita todos los protectores de pantalla eligiendo **(Ninguno)** en la lista de protectores de pantalla, el sistema operativo elimina esta entrada del Registro y llama a la función [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) con *uiAction* igual a SPI \_ SETSCREENSAVEACTIVE y *uiParam* igual a **FALSE.**
-   Esta entrada se puede sustituir por una configuración directiva de grupo en sistemas que admiten directiva de grupo. Mientras el **valor del archivo ejecutable** directiva de grupo pantalla está habilitado, el sistema omite esta entrada. La configuración de esta configuración de directiva se almacena en **laSCRNSAVE.EXE,** que se encuentra en la subclave **Policies.**

 

 
