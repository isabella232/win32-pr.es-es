---
description: 'Más información acerca de: VistaParam.Configcampo primario'
title: VistaParam.Configcampo primario (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: Configuration field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaParam.Configuration
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaparam.configuration(v=EXCHG.10)
ms:contentKeyID: 55104229
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.Configuration
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.Configuration
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b330afb7158c616ba7bb9683a7bbe226d8d63542
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808420"
---
# <a name="vistaparamconfiguration-field"></a>VistaParam.Configcampo primario

Este parámetro expone varios conjuntos de valores predeterminados para todo el conjunto de parámetros del sistema. Cuando este parámetro se establece en una configuración específica, se restablecen los valores predeterminados de todos los valores de los parámetros del sistema para esa configuración. Si se establece la configuración para una instancia específica de, los parámetros globales del sistema no se restablecerán a sus valores predeterminados. Configuración pequeña (0): el motor de base de datos está optimizado para el uso de memoria. Configuración heredada (1): el motor de base de datos tiene sus valores predeterminados tradicionales.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Const Configuration As JET_param
'Usage
Dim value As JET_param

value = VistaParam.Configuration
```

``` csharp
public const JET_param Configuration
```

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Clase VistaParam](./vistaparam-class.md)

[Miembros de VistaParam](./vistaparam-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)
