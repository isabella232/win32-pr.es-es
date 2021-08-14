---
description: NTFS transaccional (TxF) permite realizar operaciones de archivo en un volumen del sistema de archivos NTFS en una transacción.
ms.assetid: e8c3ceed-d391-4934-b3f7-12c2123c8c23
title: NTFS transaccional (TxF)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a5b44a35e4f83c1389d1fc2e6bc3de4f97f5ad203bbdee4750c2fcd26d87f47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119431915"
---
# <a name="transactional-ntfs-txf"></a>NTFS transaccional (TxF)

\[Microsoft recomienda encarecidamente a los desarrolladores que utilicen medios alternativos para satisfacer las necesidades de la aplicación. Muchos de los escenarios para los que se desarrolló TxF se pueden lograr mediante técnicas más sencillas y disponibles. Además, es posible que TxF no esté disponible en versiones futuras de Microsoft Windows. Para obtener más información y alternativas a TxF, vea [Alternativas al uso de NTFS transaccional.](deprecation-of-txf.md)\]

## <a name="purpose"></a>Propósito

NTFS transaccional (TxF) permite realizar operaciones de archivo en un volumen del sistema de archivos NTFS en una transacción. Las transacciones txF aumentan la confiabilidad de la aplicación al proteger la integridad de los datos en los errores y simplifican el desarrollo de aplicaciones al reducir en gran medida la cantidad de código de control de errores.

TxF usa el marco de transacciones proporcionado por [kernel Transaction Manager](/windows/desktop/Ktm/kernel-transaction-manager-portal) (KTM). Esto permite que las operaciones de archivo TxF forman parte de una transacción que implica otros orígenes de datos, como SQL Server y transacted Registry (TxR).

## <a name="where-applicable"></a>Donde sea aplicable

Una aplicación puede usar TxF para conservar la integridad de los datos en disco causados por condiciones de error inesperadas y ayudar a resolver escenarios de usuario del sistema de archivos simultáneos mediante el aislamiento de los cambios de otros mientras se realizan los cambios.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Antes de usar TxF, debe tener conocimientos prácticos de las transacciones mediante KTM [o Coordinador de transacciones distribuidas (DTC).](/previous-versions/windows/desktop/ms684146(v=vs.85))

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

TxF está disponible a partir de Windows Vista.

## <a name="in-this-section"></a>En esta sección



| Tema                                                    | Descripción                                                                                                |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [Acerca de](about-transactional-ntfs.md)<br/>         | Información general sobre NTFS transaccional.<br/>                                                   |
| [Referencia](transactional-ntfs-reference.md)<br/> | Documentación de las funciones, estructuras de datos, enumeraciones y otros elementos de programación.<br/> |



 

 

