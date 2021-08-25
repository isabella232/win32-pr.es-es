---
description: 'Más información sobre: JET_DBID. Método ToString (String, IFormatProvider)'
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
ms.openlocfilehash: 7b6fca1494a31bc342d4f8ad2933968c58efacc5f5e115ff10fe92a8afbabca8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017263"
---
# <a name="jet_dbidtostring-method-string-iformatprovider"></a>JET_DBID. Método ToString (String, IFormatProvider)

Da formato al valor de la instancia actual usando el formato especificado.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

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
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Cadena [que](/dotnet/api/system.string) especifica el formato que se usará. -o bien- null para usar el formato predeterminado definido para el tipo de implementación [de IFormattable.](/dotnet/api/system.iformattable)

<!-- end list -->

  - formatProvider  
    Tipo: [System.IFormatProvider](/dotnet/api/system.iformatprovider)  
    
    [IFormatProvider que se](/dotnet/api/system.iformatprovider) usará para dar formato al valor. -o bien- null para obtener la información de formato numérico de la configuración regional actual del sistema operativo.

#### <a name="return-value"></a>Valor devuelto

Tipo: [System.String](/dotnet/api/system.string)  
Cadena [que](/dotnet/api/system.string) contiene el valor de la instancia actual en el formato especificado.  

#### <a name="implements"></a>Implementaciones

[IFormattable.ToString(String, IFormatProvider)](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_DBID estructura](./jet-dbid-structure.md)

[JET_DBID miembros](./jet-dbid-members.md)

[Sobrecarga de ToString](./jet-dbid.tostring-method.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
