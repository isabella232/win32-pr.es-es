---
title: Determinar el estado de corrección de compatibilidad (shim)
description: Determinar el estado de corrección de compatibilidad (shim)
ms.assetid: 8D0B633F-9117-4F90-BF8C-AC5F57FCD30B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcac24017dc4bc4de1f9eddb1919cc8190ccf7d98cda2f127428f1d227ef1d42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117672063"
---
# <a name="determining-shim-status"></a>Determinar el estado de corrección de compatibilidad (shim)

## <a name="platforms"></a>Plataformas

<dl> Clientes: Windows 8  
Servidores: Windows Server 2012  
</dl>

## <a name="description"></a>Descripción

Windows 8 registra eventos cuando las aplicaciones se están recortando por diversos motivos. La manera más fácil de determinar si la aplicación se está recortando es comprobar el visor de eventos. Vaya a Applications and Services Logs Microsoft Windows Application-Experience Program Telemetry (Telemetría del programa de aplicaciones \\ y \\ servicios de Microsoft).

## <a name="mitigation"></a>Mitigación

La mejor manera de salir de la corrección de compatibilidad es cambiar el nombre del archivo ejecutable o aumentar la versión principal en 1 (volver a compilar el ejecutable).

 

 




