---
title: Descripción de la información de error extendida
description: La información de error extendida es una matriz de registros, cada uno de los cuales indica el paso del código de error a través de una capa determinada en el sistema o aplicación.
ms.assetid: 1b112e49-bdb2-4014-b86d-3c6d8ebe4fcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2918caa446f7cee9c4eaa609a5713c9cb385e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076083"
---
# <a name="understanding-extended-error-information"></a>Descripción de la información de error extendida

La información de error extendida es una matriz de registros, cada uno de los cuales indica el paso del código de error a través de una capa determinada en el sistema o aplicación. Si se produce un error en un equipo C, ya que se llama desde el equipo B, que a su vez se llama desde el equipo A, el tiempo de ejecución de RPC en el equipo C genera uno o varios registros que describen el error y los pasa al equipo B. el equipo B puede agregar uno o varios registros al encabezado de la cadena existente y pasa la cadena completa a. Puede agregar uno o varios registros y mostrar o registrar la información. Esencialmente, la cadena de errores extendidos representa el historial del error.

La información de error extendida no reemplaza el código de error (el código de estado de RPC \_ S \_ \* ). Independientemente de la cantidad o de si se genera información de error extendida, el código de error permanece inalterado.

Cada registro de información de error extendido contiene lo siguiente. Para obtener más información, consulte la información de [**error de RPC \_ extendida \_ \_**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_extended_error_info) :

-   ComputerName: nombre DNS no calificado del equipo en el que se originó el error. Solo los registros de los límites del equipo tienen esta información. Por ejemplo, en el escenario descrito anteriormente con los equipos A, B y C, el ComputerName se define para los siguientes campos:

    | Registro                            | Campo NombreDeEquipo |
    |-----------------------------------|--------------------|
    | Registro \# 1 generado por el equipo C | \-                 |
    | Registro \# 2 generado por el equipo C | \-                 |
    | Registro \# 3 generado por el equipo C | C                  |
    | Registro \# 1 generado por el equipo B | \-                 |
    | Registro \# 2 generado por el equipo B | \-                 |
    | Registro \# 3 generado por el equipo B | B                  |
    | Registro \# 1 generado por el equipo A | \-                 |
    | Registro \# 2 generado por el equipo A | \-                 |
    | Registro \# 3 generado por el equipo A | \-                 |
    | Encabezado de la cadena                 |                    |

    

     

<!-- -->

-   ProcessID: el identificador de proceso del proceso que generó el error.
-   Marca de tiempo: hora en que se produjo el error, expresada en formato UTC.
-   Generando componente: definición de código entero del componente lógico que generó el error. Los siguientes componentes están definidos actualmente:

    | Código | Nombre              | Descripción                                                                                                                                                                           |
    |------|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | 1    | Application       | Componente propietario de la rutina de administrador para la llamada RPC determinada                                                                                                                  |
    | 2    | Tiempo de ejecución           | El tiempo de ejecución de RPC                                                                                                                                                                      |
    | 3    | Security Provider | Proveedor de seguridad para esta llamada.                                                                                                                                                  |
    | 4    | NPFS              | El sistema de archivos NPFS                                                                                                                                                                  |
    | 5    | RDR               | El redirector                                                                                                                                                                        |
    | 6    | NNOMBRE               | Sistema de canalización con nombre. Puede ser NPFS o RDR, pero en muchos casos el tiempo de ejecución de RPC no sabe quién realizó la operación solicitada y, en estos casos, se devuelve NNOMBRE. |
    | 7    | IO                | El sistema de e/s o un controlador usado por el sistema de e/s. Puede ser NPFS, RDR o un proveedor Winsock.                                                                                 |
    | 8    | Winsock           | El proveedor Winsock                                                                                                                                                                  |
    | 9    | Código de authz        | Las API de autorización.                                                                                                                                                               |
    | 10   | LPC               | La función de llamada a procedimiento local.                                                                                                                                                    |

    

     

<!-- -->

-   Status: código de error generado o devuelto por la capa
-   DetectionLocation: número único que identifica la ubicación del código donde se detectó el error. Este campo está vinculado al código y cambiará de versión a versión. Se publicará una lista independiente de las ubicaciones de detección más frecuentes.
-   Marcas: marcas que especifican información sobre el registro. Las marcas definidas actualmente son EEInfoPreviousRecordsMissing y EEInfoNextRecordsMissing, correspondientes a los valores numéricos 1 y 2, respectivamente. Si EEInfoPreviousRecordsMissing está establecido, faltan uno o más registros antes de ese registro. Si EEInfoNextRecordsMissing está establecido, faltan uno o varios registros después del registro. Para obtener una descripción de por qué pueden faltar registros, consulte [confiabilidad de la información de error extendida](reliability-of-extended-error-information.md).
-   Hasta cuatro parámetros de error. Un parámetro de error es una estructura de variante ligera que proporciona información adicional sobre el error. La información adicional depende del error y de la ubicación de detección. Los parámetros pueden ser de tipo cadena ANSI (LPSTR), cadena Unicode (LPWSTR), valor largo (Long), valor corto (short), puntero (Int64) o ninguno.

 

 




