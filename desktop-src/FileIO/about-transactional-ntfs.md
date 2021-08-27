---
description: NTFS transaccional (TxF) integra las transacciones en el sistema de archivos NTFS, lo que facilita a los desarrolladores y administradores de aplicaciones controlar correctamente los errores y conservar la integridad de los datos.
ms.assetid: 52341315-0412-4a87-aca0-9adea7aae62f
title: Acerca de NTFS transaccional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 404dc966673eac9d61229ab127877941fe82354ddffcfd021ba76b9931c8e097
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102115"
---
# <a name="about-transactional-ntfs"></a>Acerca de NTFS transaccional

\[Microsoft recomienda encarecidamente a los desarrolladores que utilicen medios alternativos para satisfacer las necesidades de la aplicación. Muchos de los escenarios para los que se desarrolló TxF se pueden lograr mediante técnicas más sencillas y disponibles. Además, es posible que TxF no esté disponible en versiones futuras de Microsoft Windows. Para obtener más información y alternativas a TxF, vea [Alternativas al uso de NTFS transaccional.](deprecation-of-txf.md)\]

NTFS transaccional (TxF) integra las transacciones en el sistema de archivos NTFS, lo que facilita a los desarrolladores y administradores de aplicaciones controlar correctamente los errores y conservar la integridad de los datos.

TxF puede participar en transacciones distribuidas que coordina [Coordinador de transacciones distribuidas (DTC),](/previous-versions/windows/desktop/ms684146(v=vs.85)) lo que le permite usar TxF para lo siguiente:

-   Transacciones que abarcan varios almacenes de datos, por ejemplo, una única transacción para operaciones de archivos SQL datos
-   Transacciones que abarcan varios equipos, por ejemplo, una única transacción para las actualizaciones de archivos en varios equipos

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                 | Descripción                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [Cuándo usar NTFS transaccional](when-to-use-transactional-ntfs.md)<br/>                                       | Use NTFS transaccional para mantener la integridad de los datos.<br/>                                                                        |
| [Implementación de NTFS transaccional](deploying-transactional-ntfs.md)<br/>                                           | Control de almacenamiento en caché en NTFS transaccional.<br/>                                                                                    |
| [Uso de NTFS transaccional](how-to-use-transactional-ntfs.md)<br/>                                         | Administración de identificadores de archivos con transacciones en NTFS transaccional.<br/>                                                                   |
| [Conceptos básicos de TxF](txf-basic-concepts.md)<br/>                                                               | Describe los conceptos de coherencia de lectura confirmada, aislamiento de lectura confirmada y bloqueo transaccional en NTFS transaccional.<br/> |
| [Consideraciones de programación para NTFS transaccional](programming-considerations-for-transacted-fileio-.md)<br/> | Describe varias consideraciones de programación para NTFS transaccional.<br/>                                                      |
| [Consideraciones de rendimiento para NTFS transaccional](performance-considerations-for-transactional-ntfs.md)<br/> | Recomendaciones para transacciones óptimas del sistema de archivos.<br/>                                                                     |



 

 

