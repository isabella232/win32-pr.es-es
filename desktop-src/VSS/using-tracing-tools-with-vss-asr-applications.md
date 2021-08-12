---
description: Puede usar la herramienta Logman para recopilar información de seguimiento para aplicaciones VSS que usan Recuperación del sistema automatizado (ASR).
ms.assetid: 872609c8-a123-40a8-96ca-58f34d37f3d8
title: Uso de herramientas de seguimiento con aplicaciones de ASR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e2d22dbb1488b5fd60836926d3c5ef2de5913ff1cc1529fdb278773b2ccd8b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590874"
---
# <a name="using-tracing-tools-with-asr-applications"></a>Uso de herramientas de seguimiento con aplicaciones de ASR

Puede usar la herramienta Logman para recopilar información de seguimiento para aplicaciones VSS que usan [automated Recuperación del sistema (ASR).](using-vss-automated-system-recovery-for-disaster-recovery.md) Logman (logman.exe) es un controlador de seguimiento para eventos de seguimiento y contadores de rendimiento. Se incluye en Windows XP y versiones posteriores de Windows. O bien, si lo prefiere, puede usar la herramienta Tracelog para recopilar la misma información de seguimiento de ASR. Tracelog se incluye en Windows Driver Kit (WDK).

Para usar herramientas de seguimiento con VSS, vea [Usar herramientas de seguimiento con VSS.](using-tracing-tools-with-vss.md)

## <a name="using-logman"></a>Uso de Logman

En el procedimiento siguiente se describe cómo usar Logman con la aplicación ASR.

**Para usar Logman con la aplicación ASR**

1.  Use el siguiente comando para iniciar el seguimiento:

    **logman start asr -o** *x: \\ {asr.etl -ets -p {6407345b-94f2-44c8-b3db-4e076be46816} 0xff 0xff**

    > [!Note]  
    > Reemplace "x: " por la ruta de acceso al directorio donde desea almacenar el archivo de \\ registro de seguimiento. Para obtener el mejor rendimiento, el archivo de registro de seguimiento debe estar ubicado en un volumen que no forma parte de la instantánea.

     

2.  Use el siguiente comando para detener el seguimiento:

    **logman stop asr -ets**

El archivo de registro de seguimiento *es x: \\* asr.etl.

Para obtener más información sobre la herramienta Logman, vea [Logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).

## <a name="using-tracelog"></a>Uso de Tracelog

En el procedimiento siguiente se describe cómo usar Tracelog.

**Para usar Tracelog**

1.  Cree un archivo de texto denominado asr.ctl que contenga solo el texto siguiente:

    **6407345b-94f2-44c8-b3db-4e076be46816 asr**

2.  Use el siguiente comando para iniciar el seguimiento:

    **tracelog -start asr -f** *x: \\ %(asr.etl -guid asr.ctl -flag 0xff -level 0xff**

    > [!Note]  
    > Reemplace "x: " por la ruta de acceso al directorio donde desea almacenar el archivo de \\ registro de seguimiento. Para obtener el mejor rendimiento, el archivo de registro de seguimiento debe estar ubicado en un volumen que no forma parte de la instantánea.

     

3.  Use el siguiente comando para detener el seguimiento:

    **tracelog -stop asr**

El archivo de registro de seguimiento *es x: \\* asr.etl.

Para obtener más información sobre la herramienta Tracelog, vea [Tracelog](https://msdn.microsoft.com/library/ms797927.aspx).

 

 
