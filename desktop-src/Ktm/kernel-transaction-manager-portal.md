---
description: Implementar NTFS transaccional (TxF) y Registro transaccional (TxR). TxF permite operaciones del sistema de archivos con transacciones dentro de NTFS. TxR permite operaciones de registro con transacciones. Coordine las operaciones del registro y del sistema de archivos con una transacción.
ms.assetid: 2f601994-db1e-4aac-8db1-9a36c702664b
title: Administrador de transacciones de kernel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c446931fff4f119217a5f6e5f1b7ae8cf351cf94966a9da5abc4e4d2e88d787
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897535"
---
# <a name="kernel-transaction-manager"></a>Administrador de transacciones de kernel

## <a name="purpose"></a>Propósito

Kernel Transaction Manager (KTM) permite el desarrollo de aplicaciones que usan transacciones. El propio motor de transacciones está dentro del kernel, pero las transacciones se pueden desarrollar para transacciones en modo kernel o de usuario, y dentro de un único host o entre hosts distribuidos.

KTM se usa para implementar NTFS transaccional (TxF) y Registro transaccional (TxR). TxF permite operaciones del sistema de archivos con transacciones dentro del sistema de archivos NTFS. TxR permite operaciones de registro con transacciones. KTM permite que las aplicaciones cliente coordinen las operaciones del registro y del sistema de archivos con una transacción.

Para desarrollar una aplicación que coordina las transacciones con recursos distintos de TxF o TxR, primero debe desarrollar un servicio para transacciones win32, también denominado administrador de recursos.

Las aplicaciones administradas y COM+ deben usar sus administradores de transacciones nativos.

## <a name="where-applicable"></a>Donde sea aplicable

KTM se puede usar con aplicaciones y administradores de recursos hospedados en Windows Vista o Windows Server 2008.

## <a name="developer-audience"></a>Audiencia de desarrolladores

La API de KTM está diseñada para su uso por parte de programadores de C y C++.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

KTM se admite a partir de Windows Vista.

## <a name="in-this-section"></a>En esta sección



| Tema                                     | Descripción                                                                                                       |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [Acerca de](about-ktm.md)<br/>         | Información general sobre las transacciones y las funcionalidades proporcionadas por KTM.<br/>                           |
| [Referencia](ktm-reference.md)<br/> | Documentación de las funciones, estructuras de datos, enumeraciones y otros elementos de programación de KTM.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sistema de archivos de registro común](/previous-versions/windows/desktop/clfs/common-log-file-system-portal)
</dt> <dt>

[NTFS transaccional (TxF)](/windows/desktop/FileIO/transactional-ntfs-portal)
</dt> <dt>

[Coordinador de transacciones distribuidas](/previous-versions/windows/desktop/ms684146(v=vs.85))
</dt> </dl>

 

