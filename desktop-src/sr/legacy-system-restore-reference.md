---
title: Referencia de restauración del sistema heredada
description: En esta documentación se describen los detalles de implementación del repositorio que usa una versión heredada de restaurar sistema. No se aplica a la implementación de restaurar sistema en Windows Vista.
ms.assetid: d221e83d-beb0-405c-b332-a3ab8aaef688
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be8703cbf88b97458f07c616d48405708e25acec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903131"
---
# <a name="legacy-system-restore-reference"></a>Referencia de restauración del sistema heredada

\[Esta información solo se aplica a Windows XP con Service Pack 2 (SP2).\]

En esta documentación se describen los detalles de implementación del repositorio que usa una versión heredada de restaurar sistema. No se aplica a la implementación de restaurar sistema en Windows Vista.

## <a name="system-restore-repository-structure"></a>Estructura del repositorio de restauración del sistema

Windows XP con SP2 contiene un repositorio para restaurar el sistema en la siguiente carpeta:% SYSTEMDRIVE% \\ información del volumen del sistema. Este repositorio contiene información sobre los puntos de restauración, que son básicamente una instantánea del sistema en un momento dado.

El repositorio está estructurado de la manera siguiente:

**Restaurar información de volumen del sistema**    ** \_ {*GUID*}**       **RP1**       **RP2**       **RP *n*-1**       **RP * n** *     ** \_ restore {*GUID*}**       **RP1**       **RP2**       **RP *n*-1**       **RP * n***

Para determinar qué \_ carpeta de restauración {*GUID*} usar, lea el **GUID** especificado en el siguiente archivo: raízdelsistema% \\ system32 \\ restore \\MachineGUID.txt.

Dentro de cada \_ carpeta restore {*GUID*}, el \_ archivo driver. cfg contiene información de una estructura de **\_ \_ configuración persistente de Sr** definida como sigue:

``` syntax
typedef struct _SR_PERSISTENT_CONFIG
 {      
  ULONG Signature;            // Set to CPrs
  ULONG FileNameNumber;       // Number for next temp file 
                              // For example, A0000001 would be 1  
  INT64 FileSeqNumber;        // Next sequence number
  ULONG CurrentRestoreNumber; // For example, RP5 would be 5
 } SR_PERSISTENT_CONFIG, * PSR_PERSISTENT_CONFIG;
```

## <a name="files-contained-in-each-rpnfolder"></a>Archivos contenidos en cada carpeta RP *n*

Cada carpeta RP *n* contiene una carpeta de instantáneas que contiene lo siguiente:

-   Una instantánea de los subárboles del registro
-   Una carpeta de repositorio que contiene una instantánea del repositorio WMI
-   Una instantánea de la base de datos de COM+
-   Una instantánea de la base de datos de IIS

Cada carpeta RP *n* contiene un archivo RP. log que contiene información general sobre el punto de restauración de la estructura [**RESTOREPOINTINFOW**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa) .

Cada carpeta RP *n* puede contener archivos usados para realizar el seguimiento de los cambios de un punto de restauración. El primer archivo se denomina Change. log, el siguiente archivo se denomina Change. log. 1, etc. Cada archivo de registro de cambios contiene las siguientes estructuras:

-   [**\_encabezado de registro de cambios \_**](change-log-header.md)
-   [**Cambiar \_ \_Entrada de registro**](change-log-entry.md)1
-   [**Cambiar \_ \_Entrada de registro**](change-log-entry.md)2
-   ...
-   [**Cambiar \_ \_Entrada de registro**](change-log-entry.md)*n*

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Estructuras de restauración del sistema heredadas](legacy-system-restore-structures.md)
</dt> </dl>

 

 




