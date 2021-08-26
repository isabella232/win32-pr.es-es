---
description: 'Más información sobre: Constructor de instancia (String, String)'
title: Constructor de instancia (String, String)
TOCTitle: Instance constructor (String, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.#ctor(System.String,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.instance(v=EXCHG.10)
ms:contentKeyID: 55103267
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2d93a5799a646a90688261bdd55bc9dfe929ef6bd074a51e15cabdcee768ffa2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120116445"
---
# <a name="instance-constructor-string-string"></a>Constructor de instancia (String, String)

Inicializa una nueva instancia de la clase Instance. El JET_INSTANCE subyacente está asignado, pero no inicializado.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Sub New ( _
    name As String, _
    displayName As String _
)
'Usage
Dim name As String
Dim displayName As String

Dim instance As New Instance(name, displayName)
```

``` csharp
public Instance(
    string name,
    string displayName
)
```

#### <a name="parameters"></a>Parámetros

  - name  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Nombre de la instancia. Esta cadena debe ser única dentro de un proceso determinado que hospeda el motor de base de datos.

<!-- end list -->

  - DisplayName  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Nombre para mostrar de la instancia. Se usará en las entradas del registro de eventos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase de instancia](./instance-class.md)

[Miembros de instancia](./instance-members.md)

[Sobrecarga de instancia](./instance-constructor.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
