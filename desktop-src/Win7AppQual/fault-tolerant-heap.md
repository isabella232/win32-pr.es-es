---
description: Montón tolerante a errores
ms.assetid: f1ac375a-3f08-49cd-8752-6f55db24a60c
title: Montón tolerante a errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17ab2630e6dc28cb84604e48be1aa60bf208a97
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088403"
---
# <a name="fault-tolerant-heap"></a>Montón tolerante a errores

## <a name="affected-platforms"></a>Plataformas afectadas

**Clientes:** Windows 7  

## <a name="feature-impact"></a>Impacto en las características

 **Gravedad:** Medio  
**Frecuencia:** Bajo  


## <a name="description"></a>Descripción

El montón tolerante a errores (FTH) es un subsistema de Windows 7 responsable de supervisar los bloqueos de aplicaciones y aplicar de forma autónoma mitigaciones para evitar futuros bloqueos por aplicación. Para la gran mayoría de los usuarios, FTH funcionará sin necesidad de intervención ni cambio por su parte. Sin embargo, en algunos casos, es posible que los desarrolladores de aplicaciones y evaluadores de software necesiten invalidar el comportamiento predeterminado de este sistema.

## <a name="solution"></a>Solución

**Visualización de la actividad del montón tolerante a errores**

El montón tolerante a errores registra información cuando el servicio se inicia, detiene o inicia la mitigación de problemas de una nueva aplicación. Para ver la información, siga estos pasos:

1.  Haga clic en el menú Inicio.
2.  Haga clic con el botón **derecho en Equipo** y haga clic en **Administrar.**
3.  Haga **clic Visor de eventos** registros de aplicaciones y  >  **servicios** de  >  **Microsoft** Windows > montón  >  **tolerante a errores**
4.  Ver eventos FTH.

Los eventos de detención e inicio del servicio no contienen datos adicionales. El evento FTH Enabled contiene el identificador de proceso (PID), el nombre de la imagen de proceso y la hora de inicio de la instancia de proceso.

**Deshabilitar el montón tolerante a errores**

**Precaución** Pueden producirse problemas graves si modifica incorrectamente el Registro mediante el Editor del Registro o mediante otro método. Estos problemas pueden requerir que vuelva a instalar el sistema operativo. Microsoft no brinda ninguna garantía de que se puedan solucionar estos problemas. Modifique el registro bajo su responsabilidad.  
 Para deshabilitar el montón tolerante a errores completamente en un sistema, establezca el valor REG \_ DWORD **HKLM \\ Software Microsoft \\ \\ FTH \\ Enabled** en **0**.

Después de cambiar este valor, reinicie el sistema. FTH ya no se activará para las nuevas aplicaciones.

**Restablecer la lista de aplicaciones de las que realiza un seguimiento FTH**

El montón tolerante a errores se administra automáticamente y dejará de aplicarse de forma autónoma en caso de que las mitigaciones no sean eficaces para una aplicación determinada. Sin embargo, si necesita restablecer la lista de aplicaciones para las que FTH está mitigando problemas (por ejemplo, si está probando una aplicación y necesita reproducir un bloqueo que FTH está mitigando), puede ejecutar el siguiente comando desde un símbolo del sistema con privilegios elevados:  **Rundll32.exe fthsvc.dll,FthSysprepSpecialize**  
**Precaución** Al ejecutar este comando se borrarán todas las aplicaciones FTH, por lo que las aplicaciones que funcionan correctamente pueden empezar a bloquearse de nuevo después de ejecutar este comando.  

 

 



