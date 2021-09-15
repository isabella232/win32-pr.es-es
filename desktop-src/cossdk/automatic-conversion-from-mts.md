---
description: Conversión automática desde MTS
ms.assetid: 0848639a-26ce-47ad-8384-8969a7c3bcde
title: Conversión automática desde MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d424a443995c9fff9073878a43543d4c029a2445
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568061"
---
# <a name="automatic-conversion-from-mts"></a>Conversión automática desde MTS

La conversión automática se produce en dos pasos, como se muestra a continuación:

1.  Durante Windows configuración. La conversión se controla mediante el proceso Windows instalación mediante la utilidad MTSTOCOM.
    > [!Note]  
    > Si se produce un error en el paso 1, es posible que algunos o todos los paquetes MTS se hayan convertido realmente, pero que falte ciertas propiedades. En este caso, use la herramienta administrativa Servicios de componentes para comprobar todos los atributos. Los atributos mts seguirán estando presentes en el equipo (en el registro del sistema en HKEY LOCAL MACHINE Microsoft Transaction Server), pero solo será accesible a través de la \_ \_ utilidad regedit.exe \\ \\ sistema.

     

2.  Después del último reinicio antes de que Windows cuadro de diálogo iniciar sesión. El paso 2 controla las acciones de conversión que requieren acceso a la red (principalmente la creación de miembros de rol).
    > [!Note]  
    > Si se produce un error en el paso 2 (debido a errores temporales de la red o del controlador de dominio), es posible volver a ejecutar la utilidad de conversión MTSTOCOM varias veces. Para ello, en el símbolo del  sistema  o después de seleccionar Ejecutar en el menú Inicio, escriba lo siguiente: **%windir% \\ system32 \\mtstocom.exe**.

     

## <a name="mtstocom-log-file"></a>Archivo de registro MTSTOCOM

La utilidad MTSTOCOM genera un archivo de registro (Mtstocom.log) en el directorio Windows. Este archivo de registro mantiene un registro de la conversión de paquetes MTS a aplicaciones COM+. Si hubo errores durante el proceso de conversión, siempre es una buena idea comprobar el archivo de registro para obtener más información. El archivo de registro detecta problemas comunes, como un usuario o una contraseña no válidos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Resultados y problemas de conversión de COM+](com--conversion-results-and-issues.md)
</dt> <dt>

[Conversión manual desde MTS](manual-conversion-from-mts.md)
</dt> <dt>

[Biblioteca de administración de MTS](mts-administration-library.md)
</dt> </dl>

 

 



