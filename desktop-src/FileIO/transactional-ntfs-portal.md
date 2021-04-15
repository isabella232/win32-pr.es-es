---
description: NTFS transaccional (TxF) permite realizar operaciones de archivo en un volumen del sistema de archivos NTFS en una transacción.
ms.assetid: e8c3ceed-d391-4934-b3f7-12c2123c8c23
title: NTFS transaccional (TxF)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7553bfc7cae0b5389762527f0ac726c674a6a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539926"
---
# <a name="transactional-ntfs-txf"></a>NTFS transaccional (TxF)

\[Microsoft recomienda encarecidamente que los desarrolladores usen medios alternativos para lograr las necesidades de las aplicaciones. Muchos escenarios para los que se desarrolló TxF se pueden lograr mediante técnicas más sencillas y más fáciles de usar. Además, es posible que TxF no esté disponible en versiones futuras de Microsoft Windows. Para obtener más información y alternativas a TxF, vea [alternativas al uso de NTFS transaccional](deprecation-of-txf.md).\]

## <a name="purpose"></a>Propósito

NTFS transaccional (TxF) permite realizar operaciones de archivo en un volumen del sistema de archivos NTFS en una transacción. Las transacciones de TxF aumentan la confiabilidad de la aplicación al proteger la integridad de los datos en los errores y simplificar el desarrollo de aplicaciones al reducir considerablemente la cantidad de código de control de errores.

TxF usa el marco de trabajo de transacciones proporcionado por el [Administrador de transacciones de kernel](/windows/desktop/Ktm/kernel-transaction-manager-portal) (KTM). Esto permite que las operaciones de archivo TxF formen parte de una transacción que implique otros orígenes de datos, como SQL Server y el registro de transacciones (TxR).

## <a name="where-applicable"></a>Donde sea aplicable

Una aplicación puede usar TxF para conservar la integridad de los datos en el disco causados por condiciones de error inesperadas y ayudar a resolver escenarios de usuario del sistema de archivos simultáneos aislando los cambios de otros mientras se realizan los cambios.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Antes de usar TxF, debe tener conocimientos prácticos de las transacciones mediante KTM o [Coordinador de transacciones distribuidas (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85)).

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

TxF está disponible a partir de Windows Vista.

## <a name="in-this-section"></a>En esta sección



| Tema                                                    | Descripción                                                                                                |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [Acerca de](about-transactional-ntfs.md)<br/>         | Información general acerca de NTFS transaccional.<br/>                                                   |
| [Referencia](transactional-ntfs-reference.md)<br/> | Documentación para las funciones, estructuras de datos, enumeraciones y otros elementos de programación.<br/> |



 

 

