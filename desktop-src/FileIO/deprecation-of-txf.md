---
description: En este tema se de soluciones alternativas al uso de la API NTFS transaccional (TxF) en escenarios de uso comunes.
ms.assetid: 9ee26e7e-990e-4cd3-8180-f0fcaac2b752
title: Alternativas al uso de NTFS transaccional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ab924c5ee4204180b891b3aad13a5809fa07671ad0e18d6ddc9ce353122ac80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765975"
---
# <a name="alternatives-to-using-transactional-ntfs"></a>Alternativas al uso de NTFS transaccional

-   [Descripción breve](#abstract)
-   [Introducción](#introduction)
-   [Alternativas a TxF por escenario](#alternatives-to-txf-by-scenario)
-   [Aplicaciones que actualizan un único archivo con datos "similares a documentos"](#applications-updating-a-single-file-with-document-like-data)
-   [Aplicaciones que realizan actualizaciones en varios archivos o en el subárbol del Registro](#applications-performing-updates-to-multiple-files-andor-to-the-registry-hive)
-   [Aplicaciones que administran un conjunto de datos estructurados](#applications-managing-a-set-of-structured-data)
-   [Aplicaciones con transacciones que implican archivos en un volumen NTFS local y tablas en una base de datos SQL externa](#applications-with-transactions-involving-files-on-a-local-ntfs-volume-and-tables-in-an-external-sql-database)
-   [Acción & recomendada de cierre](/windows)

## <a name="abstract"></a>Descripción breve

Microsoft recomienda encarecidamente a los desarrolladores investigar el uso de las alternativas analizadas (o, en algunos casos, investigar otras alternativas) en lugar de adoptar una plataforma de API que podría no estar disponible en versiones futuras de Windows.

## <a name="introduction"></a>Introducción

TxF se introdujo con Windows Vista como medio para introducir transacciones de archivos atómicas en Windows. Permite a los desarrolladores de Windows tener atomicidad transaccional para las operaciones de archivos en transacciones con un solo archivo, en transacciones que implican varios archivos y en transacciones que abarcan varios orígenes, como el Registro (a través de TxR) y las bases de datos (como SQL). Aunque TxF es un conjunto eficaz de API, ha habido un interés de desarrollador muy limitado en esta plataforma de API desde Windows Vista principalmente debido a su complejidad y a los diversos matices que los desarrolladores deben tener en cuenta como parte del desarrollo de aplicaciones. Como resultado, Microsoft está considerando la posibilidad de desusar las API de TxF en una versión futura de Windows para centrar los esfuerzos de desarrollo y mantenimiento en otras características y API que tienen más valor para una mayor mayoría de los clientes. En la sección siguiente se describen métodos alternativos de ejemplo para lograr resultados similares a los de TxF para varios tipos de escenarios de aplicación.

## <a name="alternatives-to-txf-by-scenario"></a>Alternativas a TxF por escenario

Con las limitaciones descritas anteriormente, los desarrolladores deben investigar alternativas a TxF para cubrir escenarios de aplicación que TxF no cumple. Estas son algunas alternativas sugeridas a los usos comunes de TxF que los desarrolladores deben tener en cuenta. Tenga en cuenta que esta lista no es exhaustiva ni completa.

## <a name="applications-updating-a-single-file-with-document-like-data"></a>Aplicaciones que actualizan un único archivo con datos "similares a documentos"

Muchas aplicaciones que se tratan con datos "similares a documentos" tienden a cargar todo el documento en la memoria, a operar en él y, a continuación, a escribirlo de nuevo para guardar los cambios. La atomicidad necesaria aquí es que los cambios se aplican completamente o no se aplican en absoluto, ya que un estado incoherente haría que el archivo se dañara. Un enfoque común es escribir el documento en un archivo nuevo y, a continuación, reemplazar el archivo original por el nuevo. Un método para ello es con [**replaceFile**](/windows/desktop/api/WinBase/nf-winbase-replacefilea) API.

## <a name="applications-performing-updates-to-multiple-files-andor-to-the-registry-hive"></a>Aplicaciones que realizan actualizaciones en varios archivos o en el subárbol del Registro

Hay muchas aplicaciones que necesitan realizar de forma atómica una actualización en un conjunto de archivos y en el Registro. Este escenario se logra normalmente a través de una aplicación de instalador, como Windows Installer. Para obtener más información sobre Windows Installer, consulte Windows [Installer](/windows/desktop/Msi/windows-installer-portal).

## <a name="applications-managing-a-set-of-structured-data"></a>Aplicaciones que administran un conjunto de datos estructurados

Muchas aplicaciones administran algún conjunto de estructuras de datos propietarias de distintos tipos como medio para almacenar datos. Un desafío importante para estas aplicaciones es el proceso de mantener la integridad de punteros o referencias internos si se produce un error durante una operación de actualización. Crear el mecanismo para esto es realmente un "problema duro" y, por tanto, la mayoría de las aplicaciones se basarán en un servidor de bases de datos real para administrar su conjunto de datos.

Dos sugerencias para ayudar a administrar datos estructurados son:

-   Microsoft proporciona la bandeja de entrada Extensible Storage Engine (ESE) en Windows para permitir que las aplicaciones realicen operaciones de actualización y recuperación de datos con transacciones. Para obtener más información sobre el motor de Storage extensible (ESE), vea <https://msdn.microsoft.com/library/gg269259.aspx> .
-   En el caso de las aplicaciones que requieren un proveedor de bases de datos más eficaz, sólido y escalable, se recomienda que los clientes consideren la posibilidad de usar la característica Filestream disponible con Microsoft SQL Server. Para obtener más información sobre SQL Filestreams, vea <https://technet.microsoft.com/library/bb933993.aspx> .

## <a name="applications-with-transactions-involving-files-on-a-local-ntfs-volume-and-tables-in-an-external-sql-database"></a>Aplicaciones con transacciones que implican archivos en un volumen NTFS local y tablas en una base de datos SQL externa

Hay clases de aplicaciones que tienen grandes necesidades de conjunto de datos o necesitan tener atomicidad transaccional en una operación que implica una base de datos externa y un almacenamiento local. En este escenario, se recomienda encarecidamente que los desarrolladores consideren la posibilidad de usar SQL Filestreams para realizar operaciones de archivos transaccionales. Para obtener más información sobre SQL Filestreams, vea <https://technet.microsoft.com/library/bb933993.aspx> .

## <a name="closing--recommended-action"></a>Acción & de cierre

TxF es un conjunto complejo y matizado de API que no se usan normalmente en aplicaciones de terceros. Con la posibilidad de que estas API no estén disponibles en versiones futuras de Windows y el hecho de que haya medios alternativos más sencillos para lograr muchos de los escenarios para los que se desarrolló TxF, Microsoft recomienda encarecidamente a los desarrolladores que investiguen esos medios alternativos en lugar de crear una dependencia de TxF en sus aplicaciones.

 

 
