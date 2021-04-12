---
description: 'Más información acerca de: JET_LS. Método ToString (String, IFormatProvider)'
title: JET_LS. Método ToString (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LS.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ls.tostring(v=EXCHG.10)
ms:contentKeyID: 39512228
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_LS.ToString
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e9979a10ea3afe41a995661f1af8eac8cba80cbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277870"
---
# <a name="jet_lstostring-method-string-iformatprovider"></a>JET_LS. Método ToString (String, IFormatProvider)

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
Dim instance As JET_LS
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

[Estructura de JET_LS](./jet-ls-structure.md)

[Miembros de JET_LS](./jet-ls-members.md)

[Sobrecarga de ToString](./jet-ls.tostring-method2.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
