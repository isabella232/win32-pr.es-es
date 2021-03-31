---
description: Conversión automática desde MTS
ms.assetid: 0848639a-26ce-47ad-8384-8969a7c3bcde
title: Conversión automática desde MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d424a443995c9fff9073878a43543d4c029a2445
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153270"
---
# <a name="automatic-conversion-from-mts"></a>Conversión automática desde MTS

La conversión automática se produce en dos pasos, como se indica a continuación:

1.  Durante la instalación de Windows. El proceso de instalación de Windows controla la conversión a través de la utilidad MTSTOCOM.
    > [!Note]  
    > Si se produce un error en el paso 1, es posible que algunos o todos los paquetes MTS se hayan convertido realmente, pero que falten algunas propiedades. En este caso, use la herramienta administrativa Servicios de componentes para comprobar todos los atributos. Los atributos MTS seguirán presentes en el equipo (en el registro del sistema en HKEY \_ local \_ Machine \\ Microsoft \\ Transaction Server), pero solo serán accesibles a través de la utilidad regedit.exe.

     

2.  Después del último reinicio antes de que se muestre el cuadro de diálogo Inicio de sesión de Windows. En el paso 2 se tratan las acciones de conversión que requieren acceso a la red (principalmente, creación de miembros de rol).
    > [!Note]  
    > Si se produce un error en el paso 2 (debido a errores temporales de la red o del controlador de dominio), es posible volver a ejecutar la utilidad de conversión MTSTOCOM cualquier número de veces. Para ello, en el símbolo del sistema o después de seleccionar **Ejecutar** en el menú **Inicio** , escriba lo siguiente: **% WINDIR \\ % system32 \\mtstocom.exe**.

     

## <a name="mtstocom-log-file"></a>Archivo de registro de MTSTOCOM

La utilidad MTSTOCOM genera un archivo de registro (mtstocom. log) en el directorio de Windows. Este archivo de registro mantiene un registro de la conversión de paquetes MTS a aplicaciones COM+. Si se produjeron errores durante el proceso de conversión, siempre es una buena idea comprobar el archivo de registro para obtener más información. El archivo de registro detecta problemas comunes, como un usuario o una contraseña no válidos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Resultados y problemas de la conversión de COM+](com--conversion-results-and-issues.md)
</dt> <dt>

[Conversión manual desde MTS](manual-conversion-from-mts.md)
</dt> <dt>

[Biblioteca de administración de MTS](mts-administration-library.md)
</dt> </dl>

 

 



