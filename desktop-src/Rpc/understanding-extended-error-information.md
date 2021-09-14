---
title: Descripción de la información de error extendida
description: La información de error extendida es una matriz de registros, cada uno de los que indica el paso del código de error a través de una capa determinada en el sistema o la aplicación.
ms.assetid: 1b112e49-bdb2-4014-b86d-3c6d8ebe4fcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2918caa446f7cee9c4eaa609a5713c9cb385e4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071389"
---
# <a name="understanding-extended-error-information"></a>Descripción de la información de error extendida

La información de error extendida es una matriz de registros, cada uno de los que indica el paso del código de error a través de una capa determinada en el sistema o la aplicación. Si se produce un error en una máquina C, como se llama desde la máquina B, a la que a su vez se llama desde la máquina A, el tiempo de ejecución rpc en la máquina C genera uno o varios registros que describen el error y los pasa a la máquina B. La máquina B puede agregar uno o varios registros al responsable de la cadena existente.  y pasa la cadena completa a A. Un puede agregar uno o varios registros y mostrar o registrar la información. Básicamente, entonces, la cadena de errores extendida representa el historial del error.

La información de error extendida no reemplaza el código de error (el código de estado de RPC \_ \_ \* S). Independientemente de la cantidad o de si se genera información de error extendida, el código de error permanece sin cambios.

Cada registro de información de error extendido contiene lo siguiente. Consulte [**RPC \_ EXTENDED ERROR INFO \_ \_ para**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_extended_error_info) obtener más información:

-   ComputerName: es el nombre DNS no calificado del equipo en el que se originó el error. Solo los registros en los límites de la máquina tienen esta información. Por ejemplo, en el escenario descrito anteriormente con las máquinas A, B y C, computerName se define para los campos siguientes:

    | Registro                            | Campo ComputerName |
    |-----------------------------------|--------------------|
    | Registro \# 1 generado por la máquina C | \-                 |
    | Registro \# 2 generado por la máquina C | \-                 |
    | Registro \# 3 generado por la máquina C | C                  |
    | Registro \# 1 generado por la máquina B | \-                 |
    | Registro \# 2 generado por la máquina B | \-                 |
    | Registro \# 3 generado por la máquina B | B                  |
    | Registro \# 1 generado por la máquina A | \-                 |
    | Registro \# 2 generado por la máquina A | \-                 |
    | Registro \# 3 generado por la máquina A | \-                 |
    | Jefe de la cadena                 |                    |

    

     

<!-- -->

-   ProcessID: identificador de proceso del proceso que generó el error.
-   TimeStamp: hora en la que se produjo el error, expresada en formato UTC.
-   Componente de generación: definición de código entero del componente lógico que generó el error. Actualmente se definen los siguientes componentes:

    | Código | Nombre              | Descripción                                                                                                                                                                           |
    |------|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | 1    | Application       | Componente propietario de la rutina de administrador para la llamada RPC determinada                                                                                                                  |
    | 2    | Tiempo de ejecución           | El tiempo de ejecución de RPC                                                                                                                                                                      |
    | 3    | Security Provider | Proveedor de seguridad para esta llamada.                                                                                                                                                  |
    | 4    | NPFS              | El sistema de archivos NPFS                                                                                                                                                                  |
    | 5    | RDR               | The Redirector                                                                                                                                                                        |
    | 6    | NMP               | Sistema de canalización con nombre. Puede ser NPFS o RDR, pero en muchos casos el tiempo de ejecución de RPC no sabe quién realizó la operación solicitada y, en tales casos, se devuelve NMP. |
    | 7    | IO                | El sistema de E/S o un controlador usado por el sistema de E/S. Puede ser NPFS, RDR o un proveedor winsock.                                                                                 |
    | 8    | Winsock           | El proveedor winsock                                                                                                                                                                  |
    | 9    | Código de autenticación        | Api de autorización.                                                                                                                                                               |
    | 10   | LPC               | La instalación Llamada a procedimiento local.                                                                                                                                                    |

    

     

<!-- -->

-   Estado: código de error generado o devuelto por la capa
-   DetectionLocation: número único que identifica la ubicación del código donde se detectó el error. Este campo está vinculado al código y cambiará de versión a versión. Se publicará una lista independiente de las ubicaciones de detección más frecuentes.
-   Marcas: marcas que especifican información sobre el registro. Las marcas definidas actualmente son EEInfoPreviousRecordsMissing y EEInfoNextRecordsMissing, correspondientes a los valores numéricos 1 y 2, respectivamente. Si se establece EEInfoPreviousRecordsMissing, falta uno o varios registros antes de ese registro. Si se establece EEInfoNextRecordsMissing, faltan uno o varios registros después de ese registro. Para obtener una descripción de por qué pueden faltar registros, vea [Confiabilidad de la información de error extendida.](reliability-of-extended-error-information.md)
-   Hasta cuatro parámetros de error. Un parámetro de error es una estructura variante ligera que proporciona información adicional sobre el error. La información adicional depende del error y de la ubicación de detección. Los parámetros pueden ser de tipo cadena ANSI (LPSTR), cadena Unicode (LPWSTR), valor largo (long), valor corto (short), puntero (int64) o ninguno.

 

 




