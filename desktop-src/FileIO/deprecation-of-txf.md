---
description: En este tema se describen alternativas al uso de la API NTFS transaccional (TxF) en escenarios de uso comunes.
ms.assetid: 9ee26e7e-990e-4cd3-8180-f0fcaac2b752
title: Alternativas al uso de NTFS transaccional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc69974f27abfba0323ea4d3f16a720e5e99e69d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687278"
---
# <a name="alternatives-to-using-transactional-ntfs"></a>Alternativas al uso de NTFS transaccional

-   [Descripción](#abstract)
-   [Introducción](#introduction)
-   [Alternativas a TxF por escenario](#alternatives-to-txf-by-scenario)
-   [Aplicaciones que actualizan un solo archivo con datos de tipo "documento"](#applications-updating-a-single-file-with-document-like-data)
-   [Aplicaciones que realizan actualizaciones en varios archivos o en el subárbol del registro](#applications-performing-updates-to-multiple-files-andor-to-the-registry-hive)
-   [Aplicaciones que administran un conjunto de datos estructurados](#applications-managing-a-set-of-structured-data)
-   [Aplicaciones con transacciones que implican archivos en un volumen NTFS local y tablas en una base de datos SQL externa](#applications-with-transactions-involving-files-on-a-local-ntfs-volume-and-tables-in-an-external-sql-database)
-   [Cerrando & acción recomendada](/windows)

## <a name="abstract"></a>Descripción breve

Microsoft recomienda encarecidamente que los desarrolladores investiguen el uso de las alternativas descritas (o en algunos casos, investigue otras alternativas) en lugar de adoptar una plataforma de API que puede no estar disponible en versiones futuras de Windows.

## <a name="introduction"></a>Introducción

TxF se incorporó con Windows Vista como un medio para introducir transacciones de archivos atómicos en Windows. Permite a los desarrolladores de Windows tener atomicidad transaccional para las operaciones de archivo en las transacciones con un solo archivo, en las transacciones que implican varios archivos y en las transacciones que abarcan varios orígenes, como el registro (a través de TxR) y las bases de datos (como SQL). Aunque TxF es un conjunto eficaz de API, ha habido un interés muy limitado para desarrolladores en esta plataforma de API desde Windows Vista principalmente debido a su complejidad y a diferentes matices que los desarrolladores deben tener en cuenta como parte del desarrollo de aplicaciones. Como resultado, Microsoft está pensando en dejar de usar las API de TxF en una versión futura de Windows para centrar los esfuerzos de desarrollo y mantenimiento en otras características y API que tienen más valor para una mayoría mayor de clientes. En la siguiente sección se describen métodos alternativos de ejemplo para obtener resultados similares como TxF para varios tipos de escenarios de aplicación.

## <a name="alternatives-to-txf-by-scenario"></a>Alternativas a TxF por escenario

Con las limitaciones descritas anteriormente, los desarrolladores deben investigar alternativas a TxF para abarcar los escenarios de aplicación que no se cumplen con TxF. Aquí se describen algunas alternativas sugeridas a los usos comunes de TxF para que los desarrolladores tengan en cuenta. Tenga en cuenta que esta lista no es exhaustiva ni completa.

## <a name="applications-updating-a-single-file-with-document-like-data"></a>Aplicaciones que actualizan un solo archivo con datos de tipo "documento"

Muchas aplicaciones que se ocupan de los datos de tipo "documento" tienden a cargar todo el documento en la memoria, operar en él y, a continuación, escribirlo de nuevo para guardar los cambios. La atomicidad necesaria aquí es que los cambios se aplican completamente o no se aplican en absoluto, ya que un estado incoherente representaría el archivo dañado. Un enfoque común consiste en escribir el documento en un nuevo archivo y, a continuación, reemplazar el archivo original por el nuevo. Un método para hacerlo es con la API de [**ReplaceFile**](/windows/desktop/api/WinBase/nf-winbase-replacefilea) .

## <a name="applications-performing-updates-to-multiple-files-andor-to-the-registry-hive"></a>Aplicaciones que realizan actualizaciones en varios archivos o en el subárbol del registro

Hay muchas aplicaciones que necesitan realizar una actualización de forma atómica en un conjunto de archivos y en el registro. Este escenario se logra normalmente a través de una aplicación de instalador, como Windows Installer. Para obtener más información sobre Windows Installer, consulte [Windows Installer](/windows/desktop/Msi/windows-installer-portal).

## <a name="applications-managing-a-set-of-structured-data"></a>Aplicaciones que administran un conjunto de datos estructurados

Muchas aplicaciones administran algún conjunto de estructuras de datos de propiedad de tipos diferentes como un medio para almacenar datos. Un desafío importante para estas aplicaciones es el proceso de mantenimiento de la integridad de punteros o referencias internos si se produce un error durante una operación de actualización. Crear el mecanismo para esto es realmente un "problema" y, por lo tanto, la mayoría de las aplicaciones confiarán en un servidor de base de datos real para administrar su conjunto de datos.

Dos sugerencias para ayudar a administrar los datos estructurados son:

-   Microsoft proporciona la bandeja de entrada del motor de almacenamiento extensible (ESE) en Windows para permitir que las aplicaciones realicen operaciones de recuperación y actualización de datos con transacciones. Para obtener más información sobre el motor de almacenamiento extensible (ESE), vea <https://msdn.microsoft.com/library/gg269259.aspx> .
-   En el caso de las aplicaciones que requieren un proveedor de bases de datos más eficaz, sólido y escalable, se recomienda que los clientes consideren la posibilidad de usar la característica FileStream disponible con Microsoft SQL Server. Para obtener más información sobre las secuencias de FileStream de SQL, vea <https://technet.microsoft.com/library/bb933993.aspx> .

## <a name="applications-with-transactions-involving-files-on-a-local-ntfs-volume-and-tables-in-an-external-sql-database"></a>Aplicaciones con transacciones que implican archivos en un volumen NTFS local y tablas en una base de datos SQL externa

Hay clases de aplicaciones que tienen necesidades de conjunto de datos grandes, o deben tener atomicidad transaccional en una operación que implica una base de datos externa y un almacenamiento local. En este escenario, se recomienda encarecidamente que los desarrolladores consideren el uso de Filestreams de SQL para realizar operaciones de archivos transaccionales. Para obtener más información sobre las secuencias de FileStream de SQL, vea <https://technet.microsoft.com/library/bb933993.aspx> .

## <a name="closing--recommended-action"></a>Cerrando & acción recomendada

TxF es un conjunto complejo y de matices de API que no suelen usar las aplicaciones de terceros. Con la posibilidad de que estas API no estén disponibles en versiones futuras de Windows y el hecho de que haya más medios alternativos para lograr muchos de los escenarios para los que se desarrolló TxF, Microsoft recomienda encarecidamente a los desarrolladores que investiguen esos medios alternativos en lugar de crear una dependencia en TxF en sus aplicaciones.

 

 
