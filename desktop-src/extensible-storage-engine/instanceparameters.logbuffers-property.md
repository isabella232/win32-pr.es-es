---
description: 'Más información sobre: Propiedad InstanceParameters.LogBuffers'
title: Propiedad InstanceParameters.LogBuffers
TOCTitle: 'LogBuffers property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.logbuffers(v=EXCHG.10)
ms:contentKeyID: 55107472
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_LogBuffers
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_LogBuffers
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 60fbf06d13a8252051830c9a91dd348c2a7295a63212b587bfac9905b3b5903a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118255966"
---
# <a name="instanceparameterslogbuffers-property"></a>Propiedad InstanceParameters.LogBuffers

Obtiene o establece la cantidad de memoria usada para almacenar en caché las entradas de registro antes de que se escriban en el archivo de registro de transacciones. La unidad de este parámetro es el tamaño de sector del volumen que contiene los archivos de registro de transacciones. El tamaño del sector es casi siempre de 512 bytes, por lo que es seguro asumir ese tamaño para la unidad. Este parámetro afecta al rendimiento. Cuando el motor de base de datos está bajo una carga de actualización intensa, este búfer puede estar lleno muy rápidamente. Un tamaño de caché mayor para el archivo de registro de transacciones es fundamental para un buen rendimiento de actualización en una condición de carga tan alta. Se sabe que el valor predeterminado es demasiado pequeño para este caso. No establezca este parámetro en un número de búferes mayor (en bytes) que la mitad del tamaño de un archivo de registro de transacciones.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property LogBuffers As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.LogBuffers

instance.LogBuffers = value
```

``` csharp
public int LogBuffers { get; set; }
```

#### <a name="property-value"></a>Valor de propiedad

Tipo: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Clase InstanceParameters](./instanceparameters-class.md)

[Miembros InstanceParameters](./instanceparameters-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
