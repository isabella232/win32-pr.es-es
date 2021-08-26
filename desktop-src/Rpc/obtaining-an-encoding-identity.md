---
title: Obtener una identidad de codificación
description: Una aplicación que descodifica datos codificados puede obtener la identidad de la rutina utilizada para codificar los datos, antes de llamar a una rutina para descodificarlo. La rutina MesInqProcEncodingId proporciona esta identidad.
ms.assetid: 53cbd6c5-b267-4ff1-a45b-7e22093f41a5
keywords:
- Llamada a procedimiento remoto RPC, tareas, obtención de la identidad de codificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7a0883a1a032a76f13cfeeb6c5d6a8923146b7ee9e8184d37d5994fb5e328bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019452"
---
# <a name="obtaining-an-encoding-identity"></a>Obtener una identidad de codificación

Una aplicación que descodifica datos codificados puede obtener la identidad de la rutina utilizada para codificar los datos, antes de llamar a una rutina para descodificarlo. La [**rutina MesInqProcEncodingId**](/windows/desktop/api/Midles/nf-midles-mesinqprocencodingid) proporciona esta identidad.

El compilador MIDL asigna *a* cada procedimiento de una interfaz un número de identificación de entero, denominado identificador de procedimiento o identificador de procedimiento. La numeración comienza con cero. Las bibliotecas rpc en tiempo de ejecución no participan en la traducción del identificador de procedimiento en una llamada a procedimiento real. Dado un identificador de procedimiento, la aplicación debe proporcionar un medio para llamar al procedimiento correcto. Normalmente, los desarrolladores de aplicaciones usan una serie de instrucciones **if** o (cuando se usa C/C++) una **instrucción switch** para este propósito.

 

 




