---
description: 'Más información sobre: referencia administrada del motor de almacenamiento extensible'
title: Referencia administrada del motor de almacenamiento extensible
TOCTitle: Extensible Storage Engine Managed Reference
ms:assetid: b6dc69d0-82be-478d-b47f-37d7569cd200
ms:mtpsurl: https://msdn.microsoft.com/library/Dn375980(v=EXCHG.10)
ms:contentKeyID: 56355772
ms.date: 09/02/2015
ms.topic: article
ms.openlocfilehash: a1323d662cc7252ff6bda1eda53108751d3aedfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082306"
---
# <a name="extensible-storage-engine-managed-reference"></a>Referencia administrada del motor de almacenamiento extensible

Busque información de referencia de la biblioteca ManagedESENT. La biblioteca ManagedESENT proporciona acceso administrado a ESENT, el motor de base de datos incrustable que está nativo en Windows.


_**Se aplica a:** Windows | Windows Server_

**En este artículo**  
¿En qué se diferencia la biblioteca ManagedESENT de ESENT?  
Requisitos  
En esta sección  

## <a name="how-is-the-managedesent-library-different-than-esent"></a>¿En qué se diferencia la biblioteca ManagedESENT de ESENT?

ESENT es un motor de base de datos transaccional incrustable que le permite crear aplicaciones personalizadas que necesitan un almacenamiento confiable, de alto rendimiento y de baja sobrecarga de datos. El motor ESENT puede ayudar con los datos que van desde algo tan sencillo como una tabla hash que es demasiado grande para almacenar en memoria, algo más complejo, como una aplicación con tablas, columnas e índices. Para crear una aplicación con ESENT, use el esent.dll DLL que forma parte del sistema operativo Windows y escriba el código con C/C++. Para obtener más información sobre ESENT, vea [Referencia del motor de almacenamiento extensible](./extensible-storage-engine-reference.md).

ManagedESENT se basa en esent.dll, que forma parte de Windows, por lo que no hay archivos binarios no administrados adicionales para descargar e instalar. Con la biblioteca ManagedESENT, puede crear la aplicación mediante un lenguaje administrado como C \# en lugar de c/C++. La biblioteca usa el mismo tipo y los mismos nombres de miembro para exponer la API de ESE, por lo que si ya está familiarizado con la estructura de esta API, puede pasar fácilmente a esta biblioteca administrada.

## <a name="requirements"></a>Requisitos

Esta biblioteca administrada requiere lo siguiente:

  - Un equipo que ejecuta una versión de Windows a partir de Windows Vista

  - Visual Studio 2012

  - .NET Framework 4.5

## <a name="in-this-section"></a>En esta sección

  - [Microsoft. ISAM. esent](./microsoft.isam.esent-namespace.md)

  - [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

  - [Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)

  - [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)

  - [Microsoft. ISAM. esent. Interop. Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)

  - [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
