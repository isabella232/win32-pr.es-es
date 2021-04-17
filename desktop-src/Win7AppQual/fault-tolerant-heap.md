---
description: .
ms.assetid: f1ac375a-3f08-49cd-8752-6f55db24a60c
title: Montón tolerante a errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349c8c3d6d066de3d563880c169c8dde2e062370
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697781"
---
# <a name="fault-tolerant-heap"></a>Montón tolerante a errores

## <a name="affected-platforms"></a>Plataformas afectadas

**Clientes-** Windows 7  

## <a name="feature-impact"></a>Impacto en las características

 **Gravedad:** Medio  
**Frecuencia:** Habilita  


## <a name="description"></a>Descripción

El montón tolerante a errores (FTH) es un subsistema de Windows 7 responsable de supervisar los bloqueos de la aplicación y aplicar de forma autónoma mitigaciones para evitar bloqueos futuros en cada aplicación. Para la gran mayoría de los usuarios, FTH funcionará sin necesidad de intervención o cambio por su parte. Sin embargo, en algunos casos, es posible que los desarrolladores de aplicaciones y los evaluadores de software deban invalidar el comportamiento predeterminado de este sistema.

## <a name="solution"></a>Solución

**Ver la actividad del montón tolerante a errores**

El montón de tolerancia a errores registra información cuando el servicio se inicia, detiene o inicia la mitigación de problemas de una nueva aplicación. Para ver la información, siga estos pasos:

1.  Haga clic en el menú Inicio.
2.  Haga clic con el botón secundario en **equipo** y haga clic en **administrar**.
3.  Haga clic en **visor de eventos**  >  **registros de aplicaciones y servicios**  >  **Microsoft**  >  **Windows > tolerante a errores-montón**
4.  Ver eventos de FTH.

Los eventos de detención e inicio del servicio no contienen datos adicionales. El evento habilitado para FTH contiene el identificador de proceso (PID), el nombre de la imagen de proceso y la hora de inicio de la instancia de proceso.

**Deshabilitar el montón tolerante a errores**

**PRECAUCIÓN** Pueden producirse problemas graves si modifica incorrectamente el registro mediante el editor del registro o mediante otro método. Estos problemas pueden requerir la reinstalación del sistema operativo. Microsoft no brinda ninguna garantía de que se puedan solucionar estos problemas. Modifique el registro bajo su responsabilidad.  
 Para deshabilitar completamente el montón tolerante a errores en un sistema, establezca el valor de REG \_ DWORD **HKLM \\ software \\ Microsoft \\ FTH \\ habilitado** en **0**.

Después de cambiar este valor, reinicie el sistema. FTH ya no se activará para las nuevas aplicaciones.

**Restablecer la lista de aplicaciones a las que hace seguimiento FTH**

El montón tolerante a errores se administra automáticamente y se detiene de forma autónoma en caso de que las mitigaciones no sean eficaces para una aplicación determinada. Sin embargo, si necesita restablecer la lista de aplicaciones para las que FTH está mitigando problemas (por ejemplo, si está probando una aplicación y necesita reproducir un bloqueo que FTH está mitigando), puede ejecutar el siguiente comando desde un símbolo del sistema con privilegios elevados:  **Rundll32.exe fthsvc.dll, FthSysprepSpecialize**  
**PRECAUCIÓN** Al ejecutar este comando, se borrarán todas las aplicaciones de FTH, por lo que las aplicaciones que actualmente funcionan correctamente pueden empezar a bloquearse de nuevo después de ejecutar este comando.  

 

 



