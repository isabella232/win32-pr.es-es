---
description: Los certificados se pueden solicitar y distribuir a través de cualquier mecanismo de transporte.
ms.assetid: 2cbd0cdb-eefa-4434-893d-20e8b34f4cfe
title: Independencia de transporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed8d68b8f6312495c242f6b2bd2ea75301f802c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648233"
---
# <a name="transport-independence"></a>Independencia de transporte

Los certificados se pueden solicitar y distribuir a través de cualquier mecanismo de transporte. Los servicios de Certificate Server aceptan [*solicitudes de certificado*](../secgloss/c-gly.md) de un solicitante a través de http, DCOM, RPC, un archivo de disco o un transporte personalizado. Servicios de Certificate Server envía certificados al solicitante a través de HTTP, DCOM, RPC, un archivo de disco o un transporte personalizado.

Los transportes son compatibles con las aplicaciones intermediarios y los archivos DLL del módulo de salida, que normalmente se escriben en C/C++. Las aplicaciones intermediarios y los módulos de salida aíslan las funciones de servicios de Certificate Server de comunicarse con cualquier transporte específico.

 

 
