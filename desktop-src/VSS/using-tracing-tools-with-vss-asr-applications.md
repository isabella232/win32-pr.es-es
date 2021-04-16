---
description: Puede usar la herramienta Logman para recopilar información de seguimiento de las aplicaciones VSS que usan la recuperación automática del sistema (ASR).
ms.assetid: 872609c8-a123-40a8-96ca-58f34d37f3d8
title: Usar herramientas de seguimiento con aplicaciones ASR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c13eee1c62cd6636eebe5bcfd35bd5abb119645
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696487"
---
# <a name="using-tracing-tools-with-asr-applications"></a>Usar herramientas de seguimiento con aplicaciones ASR

Puede usar la herramienta Logman para recopilar información de seguimiento de las aplicaciones VSS que usan la [recuperación automática del sistema (ASR)](using-vss-automated-system-recovery-for-disaster-recovery.md). Logman (logman.exe) es un controlador de seguimiento para los eventos de seguimiento y los contadores de rendimiento. Se incluye en Windows XP y en versiones posteriores de Windows. O bien, si lo prefiere, puede usar la herramienta tracelog para recopilar la misma información de seguimiento de ASR. Tracelog se incluye en el kit de controladores de Windows (WDK).

Para usar las herramientas de seguimiento con VSS, consulte [uso de herramientas de seguimiento con VSS](using-tracing-tools-with-vss.md).

## <a name="using-logman"></a>Usar Logman

En el procedimiento siguiente se describe cómo usar Logman con la aplicación ASR.

**Para usar Logman con la aplicación ASR**

1.  Use el siguiente comando para iniciar el seguimiento:

    **Logman Start ASR-o** *x: \\ * * * ASR. ETL-ETS-p {6407345b-94f2-44c8-b3db-4e076be46816} 0xFF 0xFF**

    > [!Note]  
    > Reemplace "x: \\ " con la ruta de acceso al directorio donde desea que se almacene el archivo de registro de seguimiento. Para obtener el mejor rendimiento, el archivo de registro de seguimiento debe encontrarse en un volumen que no forma parte de la instantánea.

     

2.  Use el siguiente comando para detener el seguimiento:

    **Logman detener ASR-ETS**

El archivo de registro de seguimiento es *x: \\* ASR. ETL.

Para obtener más información acerca de la herramienta Logman, consulte [Logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).

## <a name="using-tracelog"></a>Usar tracelog

En el procedimiento siguiente se describe cómo usar tracelog.

**Para usar tracelog**

1.  Cree un archivo de texto denominado ASR. CTL que contenga solo el siguiente texto:

    **6407345b-94f2-44c8-b3db-4e076be46816 ASR**

2.  Use el siguiente comando para iniciar el seguimiento:

    **tracelog-Start ASR-f** *x: \\ * * * ASR. ETL-GUID ASR. CTL-Flag 0xFF-LEVEL 0xFF**

    > [!Note]  
    > Reemplace "x: \\ " con la ruta de acceso al directorio donde desea que se almacene el archivo de registro de seguimiento. Para obtener el mejor rendimiento, el archivo de registro de seguimiento debe encontrarse en un volumen que no forma parte de la instantánea.

     

3.  Use el siguiente comando para detener el seguimiento:

    **tracelog: detener ASR**

El archivo de registro de seguimiento es *x: \\* ASR. ETL.

Para obtener más información acerca de la herramienta tracelog, consulte [tracelog](https://msdn.microsoft.com/library/ms797927.aspx).

 

 
