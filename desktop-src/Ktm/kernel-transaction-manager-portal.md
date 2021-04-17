---
description: Implementar NTFS transaccional (TxF) y el registro transaccional (TxR). TxF permite operaciones del sistema de archivos transaccionales en NTFS. TxR permite operaciones del registro transaccionales. Coordine el sistema de archivos y las operaciones del registro con una transacción.
ms.assetid: 2f601994-db1e-4aac-8db1-9a36c702664b
title: Administrador de transacciones de kernel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281050461163d5fd0cde64af79e70569d613888e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652999"
---
# <a name="kernel-transaction-manager"></a>Administrador de transacciones de kernel

## <a name="purpose"></a>Propósito

El administrador de transacciones de kernel (KTM) permite el desarrollo de aplicaciones que utilizan transacciones. El propio motor de transacciones se encuentra dentro del kernel, pero las transacciones se pueden desarrollar para transacciones de modo de usuario o de kernel, y dentro de un solo host o entre hosts distribuidos.

El KTM se usa para implementar NTFS transaccional (TxF) y el registro transaccional (TxR). TxF permite operaciones del sistema de archivos transaccionales dentro del sistema de archivos NTFS. TxR permite operaciones del registro transaccionales. KTM permite a las aplicaciones cliente coordinar las operaciones del registro y del sistema de archivos con una transacción.

Para desarrollar una aplicación que coordine las transacciones con recursos distintos de TxF o TxR, primero debe desarrollar un servicio compatible con transacciones de Win32, también denominado administrador de recursos.

Las aplicaciones administradas y COM+ deben usar sus administradores de transacciones nativos.

## <a name="where-applicable"></a>Donde sea aplicable

KTM se puede usar con aplicaciones y administradores de recursos hospedados en Windows Vista o Windows Server 2008.

## <a name="developer-audience"></a>Audiencia de desarrolladores

La API de KTM está diseñada para que la usen los programadores de C y C++.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

KTM se admite a partir de Windows Vista.

## <a name="in-this-section"></a>En esta sección



| Tema                                     | Descripción                                                                                                       |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [Acerca de](about-ktm.md)<br/>         | Información general sobre las transacciones y las funciones proporcionadas por KTM.<br/>                           |
| [Referencia](ktm-reference.md)<br/> | Documentación para las funciones, estructuras de datos, enumeraciones y otros elementos de programación de KTM.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sistema de archivos de registro común](/previous-versions/windows/desktop/clfs/common-log-file-system-portal)
</dt> <dt>

[NTFS transaccional (TxF)](/windows/desktop/FileIO/transactional-ntfs-portal)
</dt> <dt>

[Coordinador de transacciones distribuidas](/previous-versions/windows/desktop/ms684146(v=vs.85))
</dt> </dl>

 

