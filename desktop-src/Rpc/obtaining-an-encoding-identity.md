---
title: Obtener una identidad de codificación
description: Una aplicación que está descodificando datos codificados puede obtener la identidad de la rutina utilizada para codificar los datos, antes de llamar a una rutina para descodificarlo. La rutina MesInqProcEncodingId proporciona esta identidad.
ms.assetid: 53cbd6c5-b267-4ff1-a45b-7e22093f41a5
keywords:
- RPC llamada a procedimiento remoto, tareas, obtener identidad de codificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8591e030913d659fb48034e4c386295773227f7f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778607"
---
# <a name="obtaining-an-encoding-identity"></a>Obtener una identidad de codificación

Una aplicación que está descodificando datos codificados puede obtener la identidad de la rutina utilizada para codificar los datos, antes de llamar a una rutina para descodificarlo. La rutina [**MesInqProcEncodingId**](/windows/desktop/api/Midles/nf-midles-mesinqprocencodingid) proporciona esta identidad.

A cada procedimiento de una interfaz se le asigna un número de identificación entero, denominado *identificador de procedimiento* o *identificador de proceso*, por el compilador de MIDL. La numeración empieza por cero. Las bibliotecas en tiempo de ejecución de RPC no implican traducir el identificador de procedimiento en una llamada a procedimiento real. Dado un identificador de procedimiento, la aplicación debe proporcionar un medio para llamar al procedimiento correcto. Normalmente, los desarrolladores de aplicaciones usan una serie de instrucciones **If** o (cuando se usa C/C++) una instrucción **Switch** con este fin.

 

 




