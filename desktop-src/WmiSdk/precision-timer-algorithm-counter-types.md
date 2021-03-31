---
description: Los tipos de contador del algoritmo del temporizador de precisión obtienen lecturas más precisas que los temporizadores del sistema.
ms.assetid: f7159645-6287-47a3-895e-20dae6e0892a
ms.tgt_platform: multiple
title: Tipos de contador del algoritmo de temporizador de precisión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a8864587fedc915678dfa4a9e578ca051e1262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818051"
---
# <a name="precision-timer-algorithm-counter-types"></a>Tipos de contador del algoritmo de temporizador de precisión

Los tipos de contador del algoritmo del temporizador de precisión obtienen lecturas más precisas que los temporizadores del sistema. El servicio que proporciona los datos también proporciona una marca de tiempo, que elimina los errores que pueden producirse debido a la hora pequeña y variable que transcurre entre la captura de la marca de tiempo del sistema y la recopilación de los datos del archivo DLL de rendimiento. Esta marca de tiempo base para los temporizadores de precisión es una \_ propiedad timestamp de precisión de rendimiento \_ , que debe seguir inmediatamente a la \_ propiedad temporizador de precisión de rendimiento \_ .



| Contratipo (constante)                                                                                         | Descripción                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [Rendimiento \_ de Decimal \_ del \_ temporizador de precisión](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))541525248<br/> | Similar al \_ temporizador de contadores de rendimiento \_ , salvo que usa una base de tiempo definida por el contador en lugar de la marca de tiempo del sistema.             |
| [Rendimiento \_ de Decimal \_ \_ del temporizador de precisión de 100](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))542573824<br/>  | Similar al temporizador de 100NSEC de rendimiento \_ \_ , salvo que usa una base de tiempo definida por un contador de 100 NS en lugar de la marca de tiempo de 100 ns del sistema. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de contador de rendimiento de WMI](wmi-performance-counter-types.md)
</dt> </dl>

 

