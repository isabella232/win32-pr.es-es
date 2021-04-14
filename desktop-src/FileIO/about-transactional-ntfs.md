---
description: NTFS transaccional (TxF) integra las transacciones en el sistema de archivos NTFS, lo que facilita que los desarrolladores y administradores de aplicaciones controlen correctamente los errores y conserven la integridad de los datos.
ms.assetid: 52341315-0412-4a87-aca0-9adea7aae62f
title: Acerca de NTFS transaccional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcf8cd99dfb1ff18ef7da88d3b3c7b0a647417e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360327"
---
# <a name="about-transactional-ntfs"></a>Acerca de NTFS transaccional

\[Microsoft recomienda encarecidamente que los desarrolladores usen medios alternativos para lograr las necesidades de las aplicaciones. Muchos escenarios para los que se desarrolló TxF se pueden lograr mediante técnicas más sencillas y más fáciles de usar. Además, es posible que TxF no esté disponible en versiones futuras de Microsoft Windows. Para obtener más información y alternativas a TxF, vea [alternativas al uso de NTFS transaccional](deprecation-of-txf.md).\]

NTFS transaccional (TxF) integra las transacciones en el sistema de archivos NTFS, lo que facilita que los desarrolladores y administradores de aplicaciones controlen correctamente los errores y conserven la integridad de los datos.

TxF puede participar en transacciones distribuidas que las coordenadas [Coordinador de transacciones distribuidas (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85)) , lo que le permite usar TxF para lo siguiente:

-   Transacciones que abarcan varios almacenes de datos, por ejemplo, una única transacción para operaciones de archivo y SQL
-   Transacciones que abarcan varios equipos, por ejemplo, una única transacción para las actualizaciones de archivos en varios equipos

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                 | Descripción                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [Cuándo usar NTFS transaccional](when-to-use-transactional-ntfs.md)<br/>                                       | Utilice NTFS transaccional para mantener la integridad de los datos.<br/>                                                                        |
| [Implementar NTFS transaccional](deploying-transactional-ntfs.md)<br/>                                           | Control de almacenamiento en caché en NTFS transaccional.<br/>                                                                                    |
| [Cómo usar NTFS transaccional](how-to-use-transactional-ntfs.md)<br/>                                         | Administrar identificadores de archivos de transacciones en NTFS transaccional.<br/>                                                                   |
| [Conceptos básicos de TxF](txf-basic-concepts.md)<br/>                                                               | Describe la coherencia de lectura confirmada, el aislamiento de lectura confirmada y los conceptos de bloqueo transaccional en NTFS transaccional.<br/> |
| [Consideraciones de programación para NTFS transaccional](programming-considerations-for-transacted-fileio-.md)<br/> | Describe diversas consideraciones de programación para NTFS transaccional.<br/>                                                      |
| [Consideraciones de rendimiento para NTFS transaccional](performance-considerations-for-transactional-ntfs.md)<br/> | Recomendaciones para las transacciones de sistema de archivos óptimas.<br/>                                                                     |



 

 

