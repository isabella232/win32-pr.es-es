---
title: Obtención de una identidad de codificación
description: Una aplicación que descodifica datos codificados puede obtener la identidad de la rutina utilizada para codificar los datos, antes de llamar a una rutina para descodificarlo. La rutina MesInqProcEncodingId proporciona esta identidad.
ms.assetid: 53cbd6c5-b267-4ff1-a45b-7e22093f41a5
keywords:
- Llamada a procedimiento remoto RPC, tareas, obtención de la identidad de codificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8591e030913d659fb48034e4c386295773227f7f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169062"
---
# <a name="obtaining-an-encoding-identity"></a>Obtención de una identidad de codificación

Una aplicación que descodifica datos codificados puede obtener la identidad de la rutina utilizada para codificar los datos, antes de llamar a una rutina para descodificarlo. La [**rutina MesInqProcEncodingId**](/windows/desktop/api/Midles/nf-midles-mesinqprocencodingid) proporciona esta identidad.

El compilador MIDL asigna *a* cada procedimiento de una interfaz un número de identificación entero, denominado identificador de procedimiento o identificador de procedimiento. La numeración comienza con cero. Las bibliotecas rpc en tiempo de ejecución no participan en la traducción del identificador de procedimiento en una llamada a procedimiento real. Dado un identificador de procedimiento, la aplicación debe proporcionar un medio para llamar al procedimiento correcto. Normalmente, los desarrolladores de aplicaciones usan una serie de instrucciones **if** o (cuando se usa C/C++) una **instrucción switch** para este propósito.

 

 




