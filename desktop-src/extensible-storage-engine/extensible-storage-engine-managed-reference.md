---
description: 'Más información sobre: Referencia administrada extensible Storage Engine'
title: Referencia administrada extensible Storage Engine
TOCTitle: Extensible Storage Engine Managed Reference
ms:assetid: b6dc69d0-82be-478d-b47f-37d7569cd200
ms:mtpsurl: https://msdn.microsoft.com/library/Dn375980(v=EXCHG.10)
ms:contentKeyID: 56355772
ms.date: 09/02/2015
ms.topic: article
ms.openlocfilehash: 38f7f09d441fa6f4158594caa8eda0b15bbe07fe909a73cd194f0886bb29914d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120093685"
---
# <a name="extensible-storage-engine-managed-reference"></a>Referencia administrada extensible Storage Engine

Busque información de referencia para la biblioteca ManagedESENT. La biblioteca ManagedESENT proporciona acceso administrado a ESENT, el motor de base de datos insertable que es nativo de Windows.


_**Se aplica a:** Windows | Windows Servidor_

**En este artículo**  
¿En qué se diferencia la biblioteca ManagedESENT de ESENT?  
Requisitos  
En esta sección  

## <a name="how-is-the-managedesent-library-different-than-esent"></a>¿En qué se diferencia la biblioteca ManagedESENT de ESENT?

ESENT es un motor de base de datos transaccional incrustable que permite crear aplicaciones personalizadas que necesitan almacenamiento de datos confiable, de alto rendimiento y de baja sobrecarga. El motor de ESENT puede ayudar con necesidades de datos que van desde algo tan simple como una tabla hash demasiado grande para almacenar en memoria, hasta algo más complejo, como una aplicación con tablas, columnas e índices. Para crear una aplicación con ESENT, use el archivo DLL de esent.dll que forma parte del sistema operativo Windows y escriba el código con C/C++. Para obtener más información sobre ESENT, vea [Extensible Storage Engine Reference](./extensible-storage-engine-reference.md).

ManagedESENT se basa en esent.dll, que forma parte de Windows, por lo que no hay archivos binarios no administrados adicionales para descargar e instalar. Con la biblioteca ManagedESENT, puede crear la aplicación mediante un lenguaje administrado como C en lugar \# de C/C++. La biblioteca usa el mismo tipo y los mismos nombres de miembro para exponer la API de ESE, por lo que si ya está familiarizado con la estructura de esta API, puede realizar fácilmente la transición a esta biblioteca administrada.

## <a name="requirements"></a>Requisitos

Esta biblioteca administrada requiere lo siguiente:

  - Un equipo que ejecuta una versión de Windows a partir de Windows Vista

  - Visual Studio 2012

  - .NET Framework 4.5

## <a name="in-this-section"></a>En esta sección

  - [Microsoft.Isam.Esent](./microsoft.isam.esent-namespace.md)

  - [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

  - [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)

  - [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)

  - [Microsoft.Isam.Esent.Interop.Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)

  - [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
