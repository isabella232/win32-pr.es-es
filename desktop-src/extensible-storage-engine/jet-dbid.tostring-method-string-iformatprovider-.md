---
description: 'Más información acerca de: JET_DBID. Método ToString (String, IFormatProvider)'
title: JET_DBID. Método ToString (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_DBID.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbid.tostring(v=EXCHG.10)
ms:contentKeyID: 39513106
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBID.ToString
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f1f9c950c86e4f749c7889fcf6914b8294850f00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686778"
---
# <a name="jet_dbidtostring-method-string-iformatprovider"></a>JET_DBID. Método ToString (String, IFormatProvider)

Da formato al valor de la instancia actual usando el formato especificado.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Function ToString ( _
    format As String, _
    formatProvider As IFormatProvider _
) As String
'Usage
Dim instance As JET_DBID
Dim format As String
Dim formatProvider As IFormatProvider
Dim returnValue As String

returnValue = instance.ToString(format, _
    formatProvider)
```

``` csharp
public string ToString(
    string format,
    IFormatProvider formatProvider
)
```

#### <a name="parameters"></a>Parámetros

  - format  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    [Cadena](/dotnet/api/system.string) que especifica el formato que se va a utilizar. -o bien, null para usar el formato predeterminado definido para el tipo de la implementación de [IFormattable](/dotnet/api/system.iformattable) .

<!-- end list -->

  - FormatProvider (  
    Tipo: [System. IFormatProvider](/dotnet/api/system.iformatprovider)  
    
    [IFormatProvider](/dotnet/api/system.iformatprovider) que se va a usar para dar formato al valor. -o bien, null para obtener la información de formato numérico de la configuración regional actual del sistema operativo.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System. String](/dotnet/api/system.string)  
[Cadena](/dotnet/api/system.string) que contiene el valor de la instancia actual en el formato especificado.  

#### <a name="implements"></a>Implementaciones

[IFormattable. ToString (String, IFormatProvider)](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Estructura de JET_DBID](./jet-dbid-structure.md)

[Miembros de JET_DBID](./jet-dbid-members.md)

[Sobrecarga de ToString](./jet-dbid.tostring-method.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
