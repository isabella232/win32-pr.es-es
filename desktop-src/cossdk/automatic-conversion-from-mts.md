---
description: Conversión automática desde MTS
ms.assetid: 0848639a-26ce-47ad-8384-8969a7c3bcde
title: Conversión automática desde MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e02cc3889c479d829290b22b71edf13cc4ebc8f419c333d5e99390d47c01da65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118549492"
---
# <a name="automatic-conversion-from-mts"></a>Conversión automática desde MTS

La conversión automática se produce en dos pasos, como se muestra a continuación:

1.  Durante Windows configuración. La conversión se controla mediante el proceso de configuración Windows a través de la utilidad MTSTOCOM.
    > [!Note]  
    > Si se produce un error en el paso 1, es posible que algunos o todos los paquetes MTS se hayan convertido, pero que falte ciertas propiedades. En este caso, use la herramienta administrativa Servicios de componentes para comprobar todos los atributos. Los atributos MTS seguirán estando presentes en el equipo (en el registro del sistema en HKEY LOCAL MACHINE Microsoft Transaction Server), pero solo serán accesibles a través de la \_ \_ utilidad \\ \\ regedit.exe.

     

2.  Después del último reinicio antes de que Windows cuadro de diálogo inicio de sesión. El paso 2 controla las acciones de conversión que requieren acceso a la red (principalmente la creación de miembros de rol).
    > [!Note]  
    > Si se produce un error en el paso 2 (debido a errores temporales de la red o del controlador de dominio), es posible volver a ejecutar la utilidad de conversión MTSTOCOM varias veces. Para ello, en el símbolo del  sistema  o después de seleccionar Ejecutar en el menú Inicio, escriba lo **siguiente: %windir% \\ system32 \\mtstocom.exe**.

     

## <a name="mtstocom-log-file"></a>Archivo de registro MTSTOCOM

La utilidad MTSTOCOM genera un archivo de registro (Mtstocom.log) en el Windows registro. Este archivo de registro mantiene un registro de la conversión de paquetes MTS a aplicaciones COM+. Si hubo errores durante el proceso de conversión, siempre es una buena idea comprobar el archivo de registro para obtener más información. El archivo de registro detecta problemas comunes, como un usuario o una contraseña no válidos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Resultados y problemas de conversión de COM+](com--conversion-results-and-issues.md)
</dt> <dt>

[Conversión manual desde MTS](manual-conversion-from-mts.md)
</dt> <dt>

[Biblioteca de administración de MTS](mts-administration-library.md)
</dt> </dl>

 

 



