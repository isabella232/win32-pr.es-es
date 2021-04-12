---
title: Determinar el estado de la corrección de compatibilidad
description: Determinar el estado de la corrección de compatibilidad
ms.assetid: 8D0B633F-9117-4F90-BF8C-AC5F57FCD30B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b830cbb4579aa2e523dfe2ec1129ed9cd10f37
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357535"
---
# <a name="determining-shim-status"></a>Determinar el estado de la corrección de compatibilidad

## <a name="platforms"></a>Plataformas

<dl> Clientes: Windows 8  
Servidores: Windows Server 2012  
</dl>

## <a name="description"></a>Descripción

Windows 8 registra eventos cuando las aplicaciones se corregido por varias razones. La forma más fácil de determinar si la aplicación se está corregido es comprobar el visor de eventos. Vaya a registros de aplicaciones y servicios \\ Microsoft Windows Application-Experience \\ telemetría de programas.

## <a name="mitigation"></a>Mitigación

La mejor manera de obtener acceso a SHIMMING es cambiar el nombre del archivo ejecutable o aumentar la versión principal en 1 (volver a compilar el archivo ejecutable).

 

 




